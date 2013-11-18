rust-curses
===========

Rust interface to terminal curses library / libraries.

Eventually the goal is to provide a Rust-ic API in
[ncurses.rs](blob/master/ncurses.rs), e.g. using RAII to ensure that
you setup and teardown an ncurses context, and that you thread access
to the terminal (or subwindows of it) via that context.

You can see a sample usage of the above in
[ncurses-intro.rs](blob/master/ncurses-intro.rs).

For now most functionality that you cannot access via that you can
still get at via [ncurses_core.rs](blob/master/ncurses_core.rs), which
is the (very thin) veneer over the `ncurses.h` header that pnkfelix
found on his Mac.  Sample uses of *that* module can be found in the
various `hello*.rs` source files.

----

The contents of hello3.rs and hello4.rs are adapted from the ncurses
tutorial, specifically
[helloworld](http://www.tldp.org/HOWTO/NCURSES-Programming-HOWTO/helloworld.html)
and
[init](http://www.tldp.org/HOWTO/NCURSES-Programming-HOWTO/init.html).

The contents of rust.rs are adapted from /usr/include/ncurses.h, which
have the following copyright notice:

/****************************************************************************
 * Copyright (c) 1998-2007,2008 Free Software Foundation, Inc.              *
 *                                                                          *
 * Permission is hereby granted, free of charge, to any person obtaining a  *
 * copy of this software and associated documentation files (the            *
 * "Software"), to deal in the Software without restriction, including      *
 * without limitation the rights to use, copy, modify, merge, publish,      *
 * distribute, distribute with modifications, sublicense, and/or sell       *
 * copies of the Software, and to permit persons to whom the Software is    *
 * furnished to do so, subject to the following conditions:                 *
 *                                                                          *
 * The above copyright notice and this permission notice shall be included  *
 * in all copies or substantial portions of the Software.                   *
 *                                                                          *
 * THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS  *
 * OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF               *
 * MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.   *
 * IN NO EVENT SHALL THE ABOVE COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,   *
 * DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR    *
 * OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR    *
 * THE USE OR OTHER DEALINGS IN THE SOFTWARE.                               *
 *                                                                          *
 * Except as contained in this notice, the name(s) of the above copyright   *
 * holders shall not be used in advertising or otherwise to promote the     *
 * sale, use or other dealings in this Software without prior written       *
 * authorization.                                                           *
 ****************************************************************************/

/****************************************************************************
 *  Author: Zeyd M. Ben-Halim <zmbenhal@netcom.com> 1992,1995               *
 *     and: Eric S. Raymond <esr@snark.thyrsus.com>                         *
 *     and: Thomas E. Dickey                        1996-on                 *
 ****************************************************************************/
