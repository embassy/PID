# PID
pid control c code



universal PIDD2 controller

uses Takahashi PID form http://bestune.50megs.com/typeABC.htm :
u(n) = u(n-1) + b0*e(n) + b1*e(n-1) + b2*e(n-2) + b3*e(n-3)

where
b0 = kp + ki + kd + kd2;
b1 = -kp -2*kd -3*kd2;
b2 = kd + 3*kd2;
b3 = -kd2;

antiwindup is implemented as u(n) limiter
there is also exponential error filter option


This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License



Author : Kenshin - Michal Chovanec, 5 February 2015




use fixed point math, where one is represented as PID_FRACTION value

#define PID_FIXED_POINT			1

use floating point math

#define PID_FLOATING_POINT		1

enable error filtering

#define PID_ERROR_FILTER_ENABLE	1

