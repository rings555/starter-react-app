function hexToRgb(e) {
    e = e.replace(/^#?([a-f\d])([a-f\d])([a-f\d])$/i, function(e, t, n, i) {
        return t + t + n + n + i + i
    });
    var t = /^#?([a-f\d]{2})([a-f\d]{2})([a-f\d]{2})$/i.exec(e);
    return t ? {
        r: parseInt(t[1], 16),
        g: parseInt(t[2], 16),
        b: parseInt(t[3], 16)
    } : null
}

function clamp(e, t, n) {
    return Math.min(Math.max(e, t), n)
}

function isInArray(e, t) {
    return t.indexOf(e) > -1
}! function(e, t) {
    "object" == typeof module && "object" == typeof module.exports ? module.exports = e.document ? t(e, !0) : function(e) {
        if (!e.document) throw new Error("jQuery requires a window with a document");
        return t(e)
    } : t(e)
}("undefined" != typeof window ? window : this, function(e, t) {
    var n = [],
        i = e.document,
        r = n.slice,
        o = n.concat,
        a = n.push,
        s = n.indexOf,
        l = {},
        c = l.toString,
        u = l.hasOwnProperty,
        d = {},
        p = "1.12.4",
        f = function(e, t) {
            return new f.fn.init(e, t)
        },
        h = /^[\s\uFEFF\xA0]+|[\s\uFEFF\xA0]+$/g,
        v = /^-ms-/,
        m = /-([\da-z])/gi,
        y = function(e, t) {
            return t.toUpperCase()
        };

    function g(e) {
        var t = !!e && "length" in e && e.length,
            n = f.type(e);
        return "function" !== n && !f.isWindow(e) && ("array" === n || 0 === t || "number" == typeof t && t > 0 && t - 1 in e)
    }
    f.fn = f.prototype = {
        jquery: p,
        constructor: f,
        selector: "",
        length: 0,
        toArray: function() {
            return r.call(this)
        },
        get: function(e) {
            return null != e ? 0 > e ? this[e + this.length] : this[e] : r.call(this)
        },
        pushStack: function(e) {
            var t = f.merge(this.constructor(), e);
            return t.prevObject = this, t.context = this.context, t
        },
        each: function(e) {
            return f.each(this, e)
        },
        map: function(e) {
            return this.pushStack(f.map(this, function(t, n) {
                return e.call(t, n, t)
            }))
        },
        slice: function() {
            return this.pushStack(r.apply(this, arguments))
        },
        first: function() {
            return this.eq(0)
        },
        last: function() {
            return this.eq(-1)
        },
        eq: function(e) {
            var t = this.length,
                n = +e + (0 > e ? t : 0);
            return this.pushStack(n >= 0 && t > n ? [this[n]] : [])
        },
        end: function() {
            return this.prevObject || this.constructor()
        },
        push: a,
        sort: n.sort,
        splice: n.splice
    }, f.extend = f.fn.extend = function() {
        var e, t, n, i, r, o, a = arguments[0] || {},
            s = 1,
            l = arguments.length,
            c = !1;
        for ("boolean" == typeof a && (c = a, a = arguments[s] || {}, s++), "object" == typeof a || f.isFunction(a) || (a = {}), s === l && (a = this, s--); l > s; s++)
            if (null != (r = arguments[s]))
                for (i in r) e = a[i], a !== (n = r[i]) && (c && n && (f.isPlainObject(n) || (t = f.isArray(n))) ? (t ? (t = !1, o = e && f.isArray(e) ? e : []) : o = e && f.isPlainObject(e) ? e : {}, a[i] = f.extend(c, o, n)) : void 0 !== n && (a[i] = n));
        return a
    }, f.extend({
        expando: "jQuery" + (p + Math.random()).replace(/\D/g, ""),
        isReady: !0,
        error: function(e) {
            throw new Error(e)
        },
        noop: function() {},
        isFunction: function(e) {
            return "function" === f.type(e)
        },
        isArray: Array.isArray || function(e) {
            return "array" === f.type(e)
        },
        isWindow: function(e) {
            return null != e && e == e.window
        },
        isNumeric: function(e) {
            var t = e && e.toString();
            return !f.isArray(e) && t - parseFloat(t) + 1 >= 0
        },
        isEmptyObject: function(e) {
            var t;
            for (t in e) return !1;
            return !0
        },
        isPlainObject: function(e) {
            var t;
            if (!e || "object" !== f.type(e) || e.nodeType || f.isWindow(e)) return !1;
            try {
                if (e.constructor && !u.call(e, "constructor") && !u.call(e.constructor.prototype, "isPrototypeOf")) return !1
            } catch (e) {
                return !1
            }
            if (!d.ownFirst)
                for (t in e) return u.call(e, t);
            for (t in e);
            return void 0 === t || u.call(e, t)
        },
        type: function(e) {
            return null == e ? e + "" : "object" == typeof e || "function" == typeof e ? l[c.call(e)] || "object" : typeof e
        },
        globalEval: function(t) {
            t && f.trim(t) && (e.execScript || function(t) {
                e.eval.call(e, t)
            })(t)
        },
        camelCase: function(e) {
            return e.replace(v, "ms-").replace(m, y)
        },
        nodeName: function(e, t) {
            return e.nodeName && e.nodeName.toLowerCase() === t.toLowerCase()
        },
        each: function(e, t) {
            var n, i = 0;
            if (g(e))
                for (n = e.length; n > i && !1 !== t.call(e[i], i, e[i]); i++);
            else
                for (i in e)
                    if (!1 === t.call(e[i], i, e[i])) break;
            return e
        },
        trim: function(e) {
            return null == e ? "" : (e + "").replace(h, "")
        },
        makeArray: function(e, t) {
            var n = t || [];
            return null != e && (g(Object(e)) ? f.merge(n, "string" == typeof e ? [e] : e) : a.call(n, e)), n
        },
        inArray: function(e, t, n) {
            var i;
            if (t) {
                if (s) return s.call(t, e, n);
                for (i = t.length, n = n ? 0 > n ? Math.max(0, i + n) : n : 0; i > n; n++)
                    if (n in t && t[n] === e) return n
            }
            return -1
        },
        merge: function(e, t) {
            for (var n = +t.length, i = 0, r = e.length; n > i;) e[r++] = t[i++];
            if (n != n)
                for (; void 0 !== t[i];) e[r++] = t[i++];
            return e.length = r, e
        },
        grep: function(e, t, n) {
            for (var i = [], r = 0, o = e.length, a = !n; o > r; r++) !t(e[r], r) !== a && i.push(e[r]);
            return i
        },
        map: function(e, t, n) {
            var i, r, a = 0,
                s = [];
            if (g(e))
                for (i = e.length; i > a; a++) null != (r = t(e[a], a, n)) && s.push(r);
            else
                for (a in e) null != (r = t(e[a], a, n)) && s.push(r);
            return o.apply([], s)
        },
        guid: 1,
        proxy: function(e, t) {
            var n, i, o;
            return "string" == typeof t && (o = e[t], t = e, e = o), f.isFunction(e) ? (n = r.call(arguments, 2), (i = function() {
                return e.apply(t || this, n.concat(r.call(arguments)))
            }).guid = e.guid = e.guid || f.guid++, i) : void 0
        },
        now: function() {
            return +new Date
        },
        support: d
    }), "function" == typeof Symbol && (f.fn[Symbol.iterator] = n[Symbol.iterator]), f.each("Boolean Number String Function Array Date RegExp Object Error Symbol".split(" "), function(e, t) {
        l["[object " + t + "]"] = t.toLowerCase()
    });
    var b = function(e) {
        var t, n, i, r, o, a, s, l, c, u, d, p, f, h, v, m, y, g, b, x = "sizzle" + 1 * new Date,
            w = e.document,
            k = 0,
            _ = 0,
            T = oe(),
            C = oe(),
            E = oe(),
            S = function(e, t) {
                return e === t && (d = !0), 0
            },
            A = 1 << 31,
            N = {}.hasOwnProperty,
            j = [],
            D = j.pop,
            L = j.push,
            q = j.push,
            M = j.slice,
            H = function(e, t) {
                for (var n = 0, i = e.length; i > n; n++)
                    if (e[n] === t) return n;
                return -1
            },
            F = "checked|selected|async|autofocus|autoplay|controls|defer|disabled|hidden|ismap|loop|multiple|open|readonly|required|scoped",
            P = "[\\x20\\t\\r\\n\\f]",
            O = "(?:\\\\.|[\\w-]|[^\\x00-\\xa0])+",
            z = "\\[" + P + "*(" + O + ")(?:" + P + "*([*^$|!~]?=)" + P + "*(?:'((?:\\\\.|[^\\\\'])*)'|\"((?:\\\\.|[^\\\\\"])*)\"|(" + O + "))|)" + P + "*\\]",
            R = ":(" + O + ")(?:\\((('((?:\\\\.|[^\\\\'])*)'|\"((?:\\\\.|[^\\\\\"])*)\")|((?:\\\\.|[^\\\\()[\\]]|" + z + ")*)|.*)\\)|)",
            I = new RegExp(P + "+", "g"),
            W = new RegExp("^" + P + "+|((?:^|[^\\\\])(?:\\\\.)*)" + P + "+$", "g"),
            B = new RegExp("^" + P + "*," + P + "*"),
            $ = new RegExp("^" + P + "*([>+~]|" + P + ")" + P + "*"),
            X = new RegExp("=" + P + "*([^\\]'\"]*?)" + P + "*\\]", "g"),
            J = new RegExp(R),
            U = new RegExp("^" + O + "$"),
            V = {
                ID: new RegExp("^#(" + O + ")"),
                CLASS: new RegExp("^\\.(" + O + ")"),
                TAG: new RegExp("^(" + O + "|[*])"),
                ATTR: new RegExp("^" + z),
                PSEUDO: new RegExp("^" + R),
                CHILD: new RegExp("^:(only|first|last|nth|nth-last)-(child|of-type)(?:\\(" + P + "*(even|odd|(([+-]|)(\\d*)n|)" + P + "*(?:([+-]|)" + P + "*(\\d+)|))" + P + "*\\)|)", "i"),
                bool: new RegExp("^(?:" + F + ")$", "i"),
                needsContext: new RegExp("^" + P + "*[>+~]|:(even|odd|eq|gt|lt|nth|first|last)(?:\\(" + P + "*((?:-\\d)?\\d*)" + P + "*\\)|)(?=[^-]|$)", "i")
            },
            Y = /^(?:input|select|textarea|button)$/i,
            G = /^h\d$/i,
            Q = /^[^{]+\{\s*\[native \w/,
            K = /^(?:#([\w-]+)|(\w+)|\.([\w-]+))$/,
            Z = /[+~]/,
            ee = /'|\\/g,
            te = new RegExp("\\\\([\\da-f]{1,6}" + P + "?|(" + P + ")|.)", "ig"),
            ne = function(e, t, n) {
                var i = "0x" + t - 65536;
                return i != i || n ? t : 0 > i ? String.fromCharCode(i + 65536) : String.fromCharCode(i >> 10 | 55296, 1023 & i | 56320)
            },
            ie = function() {
                p()
            };
        try {
            q.apply(j = M.call(w.childNodes), w.childNodes), j[w.childNodes.length].nodeType
        } catch (e) {
            q = {
                apply: j.length ? function(e, t) {
                    L.apply(e, M.call(t))
                } : function(e, t) {
                    for (var n = e.length, i = 0; e[n++] = t[i++];);
                    e.length = n - 1
                }
            }
        }

        function re(e, t, i, r) {
            var o, s, c, u, d, h, y, g, k = t && t.ownerDocument,
                _ = t ? t.nodeType : 9;
            if (i = i || [], "string" != typeof e || !e || 1 !== _ && 9 !== _ && 11 !== _) return i;
            if (!r && ((t ? t.ownerDocument || t : w) !== f && p(t), t = t || f, v)) {
                if (11 !== _ && (h = K.exec(e)))
                    if (o = h[1]) {
                        if (9 === _) {
                            if (!(c = t.getElementById(o))) return i;
                            if (c.id === o) return i.push(c), i
                        } else if (k && (c = k.getElementById(o)) && b(t, c) && c.id === o) return i.push(c), i
                    } else {
                        if (h[2]) return q.apply(i, t.getElementsByTagName(e)), i;
                        if ((o = h[3]) && n.getElementsByClassName && t.getElementsByClassName) return q.apply(i, t.getElementsByClassName(o)), i
                    } if (n.qsa && !E[e + " "] && (!m || !m.test(e))) {
                    if (1 !== _) k = t, g = e;
                    else if ("object" !== t.nodeName.toLowerCase()) {
                        for ((u = t.getAttribute("id")) ? u = u.replace(ee, "\\$&") : t.setAttribute("id", u = x), s = (y = a(e)).length, d = U.test(u) ? "#" + u : "[id='" + u + "']"; s--;) y[s] = d + " " + ve(y[s]);
                        g = y.join(","), k = Z.test(e) && fe(t.parentNode) || t
                    }
                    if (g) try {
                        return q.apply(i, k.querySelectorAll(g)), i
                    } catch (e) {} finally {
                        u === x && t.removeAttribute("id")
                    }
                }
            }
            return l(e.replace(W, "$1"), t, i, r)
        }

        function oe() {
            var e = [];
            return function t(n, r) {
                return e.push(n + " ") > i.cacheLength && delete t[e.shift()], t[n + " "] = r
            }
        }

        function ae(e) {
            return e[x] = !0, e
        }

        function se(e) {
            var t = f.createElement("div");
            try {
                return !!e(t)
            } catch (e) {
                return !1
            } finally {
                t.parentNode && t.parentNode.removeChild(t), t = null
            }
        }

        function le(e, t) {
            for (var n = e.split("|"), r = n.length; r--;) i.attrHandle[n[r]] = t
        }

        function ce(e, t) {
            var n = t && e,
                i = n && 1 === e.nodeType && 1 === t.nodeType && (~t.sourceIndex || A) - (~e.sourceIndex || A);
            if (i) return i;
            if (n)
                for (; n = n.nextSibling;)
                    if (n === t) return -1;
            return e ? 1 : -1
        }

        function ue(e) {
            return function(t) {
                return "input" === t.nodeName.toLowerCase() && t.type === e
            }
        }

        function de(e) {
            return function(t) {
                var n = t.nodeName.toLowerCase();
                return ("input" === n || "button" === n) && t.type === e
            }
        }

        function pe(e) {
            return ae(function(t) {
                return t = +t, ae(function(n, i) {
                    for (var r, o = e([], n.length, t), a = o.length; a--;) n[r = o[a]] && (n[r] = !(i[r] = n[r]))
                })
            })
        }

        function fe(e) {
            return e && void 0 !== e.getElementsByTagName && e
        }
        for (t in n = re.support = {}, o = re.isXML = function(e) {
                var t = e && (e.ownerDocument || e).documentElement;
                return !!t && "HTML" !== t.nodeName
            }, p = re.setDocument = function(e) {
                var t, r, a = e ? e.ownerDocument || e : w;
                return a !== f && 9 === a.nodeType && a.documentElement ? (h = (f = a).documentElement, v = !o(f), (r = f.defaultView) && r.top !== r && (r.addEventListener ? r.addEventListener("unload", ie, !1) : r.attachEvent && r.attachEvent("onunload", ie)), n.attributes = se(function(e) {
                    return e.className = "i", !e.getAttribute("className")
                }), n.getElementsByTagName = se(function(e) {
                    return e.appendChild(f.createComment("")), !e.getElementsByTagName("*").length
                }), n.getElementsByClassName = Q.test(f.getElementsByClassName), n.getById = se(function(e) {
                    return h.appendChild(e).id = x, !f.getElementsByName || !f.getElementsByName(x).length
                }), n.getById ? (i.find.ID = function(e, t) {
                    if (void 0 !== t.getElementById && v) {
                        var n = t.getElementById(e);
                        return n ? [n] : []
                    }
                }, i.filter.ID = function(e) {
                    var t = e.replace(te, ne);
                    return function(e) {
                        return e.getAttribute("id") === t
                    }
                }) : (delete i.find.ID, i.filter.ID = function(e) {
                    var t = e.replace(te, ne);
                    return function(e) {
                        var n = void 0 !== e.getAttributeNode && e.getAttributeNode("id");
                        return n && n.value === t
                    }
                }), i.find.TAG = n.getElementsByTagName ? function(e, t) {
                    return void 0 !== t.getElementsByTagName ? t.getElementsByTagName(e) : n.qsa ? t.querySelectorAll(e) : void 0
                } : function(e, t) {
                    var n, i = [],
                        r = 0,
                        o = t.getElementsByTagName(e);
                    if ("*" === e) {
                        for (; n = o[r++];) 1 === n.nodeType && i.push(n);
                        return i
                    }
                    return o
                }, i.find.CLASS = n.getElementsByClassName && function(e, t) {
                    return void 0 !== t.getElementsByClassName && v ? t.getElementsByClassName(e) : void 0
                }, y = [], m = [], (n.qsa = Q.test(f.querySelectorAll)) && (se(function(e) {
                    h.appendChild(e).innerHTML = "<a id='" + x + "'></a><select id='" + x + "-\r\\' msallowcapture=''><option selected=''></option></select>", e.querySelectorAll("[msallowcapture^='']").length && m.push("[*^$]=" + P + "*(?:''|\"\")"), e.querySelectorAll("[selected]").length || m.push("\\[" + P + "*(?:value|" + F + ")"), e.querySelectorAll("[id~=" + x + "-]").length || m.push("~="), e.querySelectorAll(":checked").length || m.push(":checked"), e.querySelectorAll("a#" + x + "+*").length || m.push(".#.+[+~]")
                }), se(function(e) {
                    var t = f.createElement("input");
                    t.setAttribute("type", "hidden"), e.appendChild(t).setAttribute("name", "D"), e.querySelectorAll("[name=d]").length && m.push("name" + P + "*[*^$|!~]?="), e.querySelectorAll(":enabled").length || m.push(":enabled", ":disabled"), e.querySelectorAll("*,:x"), m.push(",.*:")
                })), (n.matchesSelector = Q.test(g = h.matches || h.webkitMatchesSelector || h.mozMatchesSelector || h.oMatchesSelector || h.msMatchesSelector)) && se(function(e) {
                    n.disconnectedMatch = g.call(e, "div"), g.call(e, "[s!='']:x"), y.push("!=", R)
                }), m = m.length && new RegExp(m.join("|")), y = y.length && new RegExp(y.join("|")), t = Q.test(h.compareDocumentPosition), b = t || Q.test(h.contains) ? function(e, t) {
                    var n = 9 === e.nodeType ? e.documentElement : e,
                        i = t && t.parentNode;
                    return e === i || !(!i || 1 !== i.nodeType || !(n.contains ? n.contains(i) : e.compareDocumentPosition && 16 & e.compareDocumentPosition(i)))
                } : function(e, t) {
                    if (t)
                        for (; t = t.parentNode;)
                            if (t === e) return !0;
                    return !1
                }, S = t ? function(e, t) {
                    if (e === t) return d = !0, 0;
                    var i = !e.compareDocumentPosition - !t.compareDocumentPosition;
                    return i || (1 & (i = (e.ownerDocument || e) === (t.ownerDocument || t) ? e.compareDocumentPosition(t) : 1) || !n.sortDetached && t.compareDocumentPosition(e) === i ? e === f || e.ownerDocument === w && b(w, e) ? -1 : t === f || t.ownerDocument === w && b(w, t) ? 1 : u ? H(u, e) - H(u, t) : 0 : 4 & i ? -1 : 1)
                } : function(e, t) {
                    if (e === t) return d = !0, 0;
                    var n, i = 0,
                        r = e.parentNode,
                        o = t.parentNode,
                        a = [e],
                        s = [t];
                    if (!r || !o) return e === f ? -1 : t === f ? 1 : r ? -1 : o ? 1 : u ? H(u, e) - H(u, t) : 0;
                    if (r === o) return ce(e, t);
                    for (n = e; n = n.parentNode;) a.unshift(n);
                    for (n = t; n = n.parentNode;) s.unshift(n);
                    for (; a[i] === s[i];) i++;
                    return i ? ce(a[i], s[i]) : a[i] === w ? -1 : s[i] === w ? 1 : 0
                }, f) : f
            }, re.matches = function(e, t) {
                return re(e, null, null, t)
            }, re.matchesSelector = function(e, t) {
                if ((e.ownerDocument || e) !== f && p(e), t = t.replace(X, "='$1']"), n.matchesSelector && v && !E[t + " "] && (!y || !y.test(t)) && (!m || !m.test(t))) try {
                    var i = g.call(e, t);
                    if (i || n.disconnectedMatch || e.document && 11 !== e.document.nodeType) return i
                } catch (e) {}
                return re(t, f, null, [e]).length > 0
            }, re.contains = function(e, t) {
                return (e.ownerDocument || e) !== f && p(e), b(e, t)
            }, re.attr = function(e, t) {
                (e.ownerDocument || e) !== f && p(e);
                var r = i.attrHandle[t.toLowerCase()],
                    o = r && N.call(i.attrHandle, t.toLowerCase()) ? r(e, t, !v) : void 0;
                return void 0 !== o ? o : n.attributes || !v ? e.getAttribute(t) : (o = e.getAttributeNode(t)) && o.specified ? o.value : null
            }, re.error = function(e) {
                throw new Error("Syntax error, unrecognized expression: " + e)
            }, re.uniqueSort = function(e) {
                var t, i = [],
                    r = 0,
                    o = 0;
                if (d = !n.detectDuplicates, u = !n.sortStable && e.slice(0), e.sort(S), d) {
                    for (; t = e[o++];) t === e[o] && (r = i.push(o));
                    for (; r--;) e.splice(i[r], 1)
                }
                return u = null, e
            }, r = re.getText = function(e) {
                var t, n = "",
                    i = 0,
                    o = e.nodeType;
                if (o) {
                    if (1 === o || 9 === o || 11 === o) {
                        if ("string" == typeof e.textContent) return e.textContent;
                        for (e = e.firstChild; e; e = e.nextSibling) n += r(e)
                    } else if (3 === o || 4 === o) return e.nodeValue
                } else
                    for (; t = e[i++];) n += r(t);
                return n
            }, (i = re.selectors = {
                cacheLength: 50,
                createPseudo: ae,
                match: V,
                attrHandle: {},
                find: {},
                relative: {
                    ">": {
                        dir: "parentNode",
                        first: !0
                    },
                    " ": {
                        dir: "parentNode"
                    },
                    "+": {
                        dir: "previousSibling",
                        first: !0
                    },
                    "~": {
                        dir: "previousSibling"
                    }
                },
                preFilter: {
                    ATTR: function(e) {
                        return e[1] = e[1].replace(te, ne), e[3] = (e[3] || e[4] || e[5] || "").replace(te, ne), "~=" === e[2] && (e[3] = " " + e[3] + " "), e.slice(0, 4)
                    },
                    CHILD: function(e) {
                        return e[1] = e[1].toLowerCase(), "nth" === e[1].slice(0, 3) ? (e[3] || re.error(e[0]), e[4] = +(e[4] ? e[5] + (e[6] || 1) : 2 * ("even" === e[3] || "odd" === e[3])), e[5] = +(e[7] + e[8] || "odd" === e[3])) : e[3] && re.error(e[0]), e
                    },
                    PSEUDO: function(e) {
                        var t, n = !e[6] && e[2];
                        return V.CHILD.test(e[0]) ? null : (e[3] ? e[2] = e[4] || e[5] || "" : n && J.test(n) && (t = a(n, !0)) && (t = n.indexOf(")", n.length - t) - n.length) && (e[0] = e[0].slice(0, t), e[2] = n.slice(0, t)), e.slice(0, 3))
                    }
                },
                filter: {
                    TAG: function(e) {
                        var t = e.replace(te, ne).toLowerCase();
                        return "*" === e ? function() {
                            return !0
                        } : function(e) {
                            return e.nodeName && e.nodeName.toLowerCase() === t
                        }
                    },
                    CLASS: function(e) {
                        var t = T[e + " "];
                        return t || (t = new RegExp("(^|" + P + ")" + e + "(" + P + "|$)")) && T(e, function(e) {
                            return t.test("string" == typeof e.className && e.className || void 0 !== e.getAttribute && e.getAttribute("class") || "")
                        })
                    },
                    ATTR: function(e, t, n) {
                        return function(i) {
                            var r = re.attr(i, e);
                            return null == r ? "!=" === t : !t || (r += "", "=" === t ? r === n : "!=" === t ? r !== n : "^=" === t ? n && 0 === r.indexOf(n) : "*=" === t ? n && r.indexOf(n) > -1 : "$=" === t ? n && r.slice(-n.length) === n : "~=" === t ? (" " + r.replace(I, " ") + " ").indexOf(n) > -1 : "|=" === t && (r === n || r.slice(0, n.length + 1) === n + "-"))
                        }
                    },
                    CHILD: function(e, t, n, i, r) {
                        var o = "nth" !== e.slice(0, 3),
                            a = "last" !== e.slice(-4),
                            s = "of-type" === t;
                        return 1 === i && 0 === r ? function(e) {
                            return !!e.parentNode
                        } : function(t, n, l) {
                            var c, u, d, p, f, h, v = o !== a ? "nextSibling" : "previousSibling",
                                m = t.parentNode,
                                y = s && t.nodeName.toLowerCase(),
                                g = !l && !s,
                                b = !1;
                            if (m) {
                                if (o) {
                                    for (; v;) {
                                        for (p = t; p = p[v];)
                                            if (s ? p.nodeName.toLowerCase() === y : 1 === p.nodeType) return !1;
                                        h = v = "only" === e && !h && "nextSibling"
                                    }
                                    return !0
                                }
                                if (h = [a ? m.firstChild : m.lastChild], a && g) {
                                    for (b = (f = (c = (u = (d = (p = m)[x] || (p[x] = {}))[p.uniqueID] || (d[p.uniqueID] = {}))[e] || [])[0] === k && c[1]) && c[2], p = f && m.childNodes[f]; p = ++f && p && p[v] || (b = f = 0) || h.pop();)
                                        if (1 === p.nodeType && ++b && p === t) {
                                            u[e] = [k, f, b];
                                            break
                                        }
                                } else if (g && (b = f = (c = (u = (d = (p = t)[x] || (p[x] = {}))[p.uniqueID] || (d[p.uniqueID] = {}))[e] || [])[0] === k && c[1]), !1 === b)
                                    for (;
                                        (p = ++f && p && p[v] || (b = f = 0) || h.pop()) && ((s ? p.nodeName.toLowerCase() !== y : 1 !== p.nodeType) || !++b || (g && ((u = (d = p[x] || (p[x] = {}))[p.uniqueID] || (d[p.uniqueID] = {}))[e] = [k, b]), p !== t)););
                                return (b -= r) === i || b % i == 0 && b / i >= 0
                            }
                        }
                    },
                    PSEUDO: function(e, t) {
                        var n, r = i.pseudos[e] || i.setFilters[e.toLowerCase()] || re.error("unsupported pseudo: " + e);
                        return r[x] ? r(t) : r.length > 1 ? (n = [e, e, "", t], i.setFilters.hasOwnProperty(e.toLowerCase()) ? ae(function(e, n) {
                            for (var i, o = r(e, t), a = o.length; a--;) e[i = H(e, o[a])] = !(n[i] = o[a])
                        }) : function(e) {
                            return r(e, 0, n)
                        }) : r
                    }
                },
                pseudos: {
                    not: ae(function(e) {
                        var t = [],
                            n = [],
                            i = s(e.replace(W, "$1"));
                        return i[x] ? ae(function(e, t, n, r) {
                            for (var o, a = i(e, null, r, []), s = e.length; s--;)(o = a[s]) && (e[s] = !(t[s] = o))
                        }) : function(e, r, o) {
                            return t[0] = e, i(t, null, o, n), t[0] = null, !n.pop()
                        }
                    }),
                    has: ae(function(e) {
                        return function(t) {
                            return re(e, t).length > 0
                        }
                    }),
                    contains: ae(function(e) {
                        return e = e.replace(te, ne),
                            function(t) {
                                return (t.textContent || t.innerText || r(t)).indexOf(e) > -1
                            }
                    }),
                    lang: ae(function(e) {
                        return U.test(e || "") || re.error("unsupported lang: " + e), e = e.replace(te, ne).toLowerCase(),
                            function(t) {
                                var n;
                                do {
                                    if (n = v ? t.lang : t.getAttribute("xml:lang") || t.getAttribute("lang")) return (n = n.toLowerCase()) === e || 0 === n.indexOf(e + "-")
                                } while ((t = t.parentNode) && 1 === t.nodeType);
                                return !1
                            }
                    }),
                    target: function(t) {
                        var n = e.location && e.location.hash;
                        return n && n.slice(1) === t.id
                    },
                    root: function(e) {
                        return e === h
                    },
                    focus: function(e) {
                        return e === f.activeElement && (!f.hasFocus || f.hasFocus()) && !!(e.type || e.href || ~e.tabIndex)
                    },
                    enabled: function(e) {
                        return !1 === e.disabled
                    },
                    disabled: function(e) {
                        return !0 === e.disabled
                    },
                    checked: function(e) {
                        var t = e.nodeName.toLowerCase();
                        return "input" === t && !!e.checked || "option" === t && !!e.selected
                    },
                    selected: function(e) {
                        return e.parentNode && e.parentNode.selectedIndex, !0 === e.selected
                    },
                    empty: function(e) {
                        for (e = e.firstChild; e; e = e.nextSibling)
                            if (e.nodeType < 6) return !1;
                        return !0
                    },
                    parent: function(e) {
                        return !i.pseudos.empty(e)
                    },
                    header: function(e) {
                        return G.test(e.nodeName)
                    },
                    input: function(e) {
                        return Y.test(e.nodeName)
                    },
                    button: function(e) {
                        var t = e.nodeName.toLowerCase();
                        return "input" === t && "button" === e.type || "button" === t
                    },
                    text: function(e) {
                        var t;
                        return "input" === e.nodeName.toLowerCase() && "text" === e.type && (null == (t = e.getAttribute("type")) || "text" === t.toLowerCase())
                    },
                    first: pe(function() {
                        return [0]
                    }),
                    last: pe(function(e, t) {
                        return [t - 1]
                    }),
                    eq: pe(function(e, t, n) {
                        return [0 > n ? n + t : n]
                    }),
                    even: pe(function(e, t) {
                        for (var n = 0; t > n; n += 2) e.push(n);
                        return e
                    }),
                    odd: pe(function(e, t) {
                        for (var n = 1; t > n; n += 2) e.push(n);
                        return e
                    }),
                    lt: pe(function(e, t, n) {
                        for (var i = 0 > n ? n + t : n; --i >= 0;) e.push(i);
                        return e
                    }),
                    gt: pe(function(e, t, n) {
                        for (var i = 0 > n ? n + t : n; ++i < t;) e.push(i);
                        return e
                    })
                }
            }).pseudos.nth = i.pseudos.eq, {
                radio: !0,
                checkbox: !0,
                file: !0,
                password: !0,
                image: !0
            }) i.pseudos[t] = ue(t);
        for (t in {
                submit: !0,
                reset: !0
            }) i.pseudos[t] = de(t);

        function he() {}

        function ve(e) {
            for (var t = 0, n = e.length, i = ""; n > t; t++) i += e[t].value;
            return i
        }

        function me(e, t, n) {
            var i = t.dir,
                r = n && "parentNode" === i,
                o = _++;
            return t.first ? function(t, n, o) {
                for (; t = t[i];)
                    if (1 === t.nodeType || r) return e(t, n, o)
            } : function(t, n, a) {
                var s, l, c, u = [k, o];
                if (a) {
                    for (; t = t[i];)
                        if ((1 === t.nodeType || r) && e(t, n, a)) return !0
                } else
                    for (; t = t[i];)
                        if (1 === t.nodeType || r) {
                            if ((s = (l = (c = t[x] || (t[x] = {}))[t.uniqueID] || (c[t.uniqueID] = {}))[i]) && s[0] === k && s[1] === o) return u[2] = s[2];
                            if (l[i] = u, u[2] = e(t, n, a)) return !0
                        }
            }
        }

        function ye(e) {
            return e.length > 1 ? function(t, n, i) {
                for (var r = e.length; r--;)
                    if (!e[r](t, n, i)) return !1;
                return !0
            } : e[0]
        }

        function ge(e, t, n, i, r) {
            for (var o, a = [], s = 0, l = e.length, c = null != t; l > s; s++)(o = e[s]) && (n && !n(o, i, r) || (a.push(o), c && t.push(s)));
            return a
        }

        function be(e, t, n, i, r, o) {
            return i && !i[x] && (i = be(i)), r && !r[x] && (r = be(r, o)), ae(function(o, a, s, l) {
                var c, u, d, p = [],
                    f = [],
                    h = a.length,
                    v = o || function(e, t, n) {
                        for (var i = 0, r = t.length; r > i; i++) re(e, t[i], n);
                        return n
                    }(t || "*", s.nodeType ? [s] : s, []),
                    m = !e || !o && t ? v : ge(v, p, e, s, l),
                    y = n ? r || (o ? e : h || i) ? [] : a : m;
                if (n && n(m, y, s, l), i)
                    for (c = ge(y, f), i(c, [], s, l), u = c.length; u--;)(d = c[u]) && (y[f[u]] = !(m[f[u]] = d));
                if (o) {
                    if (r || e) {
                        if (r) {
                            for (c = [], u = y.length; u--;)(d = y[u]) && c.push(m[u] = d);
                            r(null, y = [], c, l)
                        }
                        for (u = y.length; u--;)(d = y[u]) && (c = r ? H(o, d) : p[u]) > -1 && (o[c] = !(a[c] = d))
                    }
                } else y = ge(y === a ? y.splice(h, y.length) : y), r ? r(null, a, y, l) : q.apply(a, y)
            })
        }

        function xe(e) {
            for (var t, n, r, o = e.length, a = i.relative[e[0].type], s = a || i.relative[" "], l = a ? 1 : 0, u = me(function(e) {
                    return e === t
                }, s, !0), d = me(function(e) {
                    return H(t, e) > -1
                }, s, !0), p = [function(e, n, i) {
                    var r = !a && (i || n !== c) || ((t = n).nodeType ? u(e, n, i) : d(e, n, i));
                    return t = null, r
                }]; o > l; l++)
                if (n = i.relative[e[l].type]) p = [me(ye(p), n)];
                else {
                    if ((n = i.filter[e[l].type].apply(null, e[l].matches))[x]) {
                        for (r = ++l; o > r && !i.relative[e[r].type]; r++);
                        return be(l > 1 && ye(p), l > 1 && ve(e.slice(0, l - 1).concat({
                            value: " " === e[l - 2].type ? "*" : ""
                        })).replace(W, "$1"), n, r > l && xe(e.slice(l, r)), o > r && xe(e = e.slice(r)), o > r && ve(e))
                    }
                    p.push(n)
                } return ye(p)
        }

        function we(e, t) {
            var n = t.length > 0,
                r = e.length > 0,
                o = function(o, a, s, l, u) {
                    var d, h, m, y = 0,
                        g = "0",
                        b = o && [],
                        x = [],
                        w = c,
                        _ = o || r && i.find.TAG("*", u),
                        T = k += null == w ? 1 : Math.random() || .1,
                        C = _.length;
                    for (u && (c = a === f || a || u); g !== C && null != (d = _[g]); g++) {
                        if (r && d) {
                            for (h = 0, a || d.ownerDocument === f || (p(d), s = !v); m = e[h++];)
                                if (m(d, a || f, s)) {
                                    l.push(d);
                                    break
                                } u && (k = T)
                        }
                        n && ((d = !m && d) && y--, o && b.push(d))
                    }
                    if (y += g, n && g !== y) {
                        for (h = 0; m = t[h++];) m(b, x, a, s);
                        if (o) {
                            if (y > 0)
                                for (; g--;) b[g] || x[g] || (x[g] = D.call(l));
                            x = ge(x)
                        }
                        q.apply(l, x), u && !o && x.length > 0 && y + t.length > 1 && re.uniqueSort(l)
                    }
                    return u && (k = T, c = w), b
                };
            return n ? ae(o) : o
        }
        return he.prototype = i.filters = i.pseudos, i.setFilters = new he, a = re.tokenize = function(e, t) {
            var n, r, o, a, s, l, c, u = C[e + " "];
            if (u) return t ? 0 : u.slice(0);
            for (s = e, l = [], c = i.preFilter; s;) {
                for (a in n && !(r = B.exec(s)) || (r && (s = s.slice(r[0].length) || s), l.push(o = [])), n = !1, (r = $.exec(s)) && (n = r.shift(), o.push({
                        value: n,
                        type: r[0].replace(W, " ")
                    }), s = s.slice(n.length)), i.filter) !(r = V[a].exec(s)) || c[a] && !(r = c[a](r)) || (n = r.shift(), o.push({
                    value: n,
                    type: a,
                    matches: r
                }), s = s.slice(n.length));
                if (!n) break
            }
            return t ? s.length : s ? re.error(e) : C(e, l).slice(0)
        }, s = re.compile = function(e, t) {
            var n, i = [],
                r = [],
                o = E[e + " "];
            if (!o) {
                for (t || (t = a(e)), n = t.length; n--;)(o = xe(t[n]))[x] ? i.push(o) : r.push(o);
                (o = E(e, we(r, i))).selector = e
            }
            return o
        }, l = re.select = function(e, t, r, o) {
            var l, c, u, d, p, f = "function" == typeof e && e,
                h = !o && a(e = f.selector || e);
            if (r = r || [], 1 === h.length) {
                if ((c = h[0] = h[0].slice(0)).length > 2 && "ID" === (u = c[0]).type && n.getById && 9 === t.nodeType && v && i.relative[c[1].type]) {
                    if (!(t = (i.find.ID(u.matches[0].replace(te, ne), t) || [])[0])) return r;
                    f && (t = t.parentNode), e = e.slice(c.shift().value.length)
                }
                for (l = V.needsContext.test(e) ? 0 : c.length; l-- && (u = c[l], !i.relative[d = u.type]);)
                    if ((p = i.find[d]) && (o = p(u.matches[0].replace(te, ne), Z.test(c[0].type) && fe(t.parentNode) || t))) {
                        if (c.splice(l, 1), !(e = o.length && ve(c))) return q.apply(r, o), r;
                        break
                    }
            }
            return (f || s(e, h))(o, t, !v, r, !t || Z.test(e) && fe(t.parentNode) || t), r
        }, n.sortStable = x.split("").sort(S).join("") === x, n.detectDuplicates = !!d, p(), n.sortDetached = se(function(e) {
            return 1 & e.compareDocumentPosition(f.createElement("div"))
        }), se(function(e) {
            return e.innerHTML = "<a href='#'></a>", "#" === e.firstChild.getAttribute("href")
        }) || le("type|href|height|width", function(e, t, n) {
            return n ? void 0 : e.getAttribute(t, "type" === t.toLowerCase() ? 1 : 2)
        }), n.attributes && se(function(e) {
            return e.innerHTML = "<input/>", e.firstChild.setAttribute("value", ""), "" === e.firstChild.getAttribute("value")
        }) || le("value", function(e, t, n) {
            return n || "input" !== e.nodeName.toLowerCase() ? void 0 : e.defaultValue
        }), se(function(e) {
            return null == e.getAttribute("disabled")
        }) || le(F, function(e, t, n) {
            var i;
            return n ? void 0 : !0 === e[t] ? t.toLowerCase() : (i = e.getAttributeNode(t)) && i.specified ? i.value : null
        }), re
    }(e);
    f.find = b, f.expr = b.selectors, f.expr[":"] = f.expr.pseudos, f.uniqueSort = f.unique = b.uniqueSort, f.text = b.getText, f.isXMLDoc = b.isXML, f.contains = b.contains;
    var x = function(e, t, n) {
            for (var i = [], r = void 0 !== n;
                (e = e[t]) && 9 !== e.nodeType;)
                if (1 === e.nodeType) {
                    if (r && f(e).is(n)) break;
                    i.push(e)
                } return i
        },
        w = function(e, t) {
            for (var n = []; e; e = e.nextSibling) 1 === e.nodeType && e !== t && n.push(e);
            return n
        },
        k = f.expr.match.needsContext,
        _ = /^<([\w-]+)\s*\/?>(?:<\/\1>|)$/,
        T = /^.[^:#\[\.,]*$/;

    function C(e, t, n) {
        if (f.isFunction(t)) return f.grep(e, function(e, i) {
            return !!t.call(e, i, e) !== n
        });
        if (t.nodeType) return f.grep(e, function(e) {
            return e === t !== n
        });
        if ("string" == typeof t) {
            if (T.test(t)) return f.filter(t, e, n);
            t = f.filter(t, e)
        }
        return f.grep(e, function(e) {
            return f.inArray(e, t) > -1 !== n
        })
    }
    f.filter = function(e, t, n) {
        var i = t[0];
        return n && (e = ":not(" + e + ")"), 1 === t.length && 1 === i.nodeType ? f.find.matchesSelector(i, e) ? [i] : [] : f.find.matches(e, f.grep(t, function(e) {
            return 1 === e.nodeType
        }))
    }, f.fn.extend({
        find: function(e) {
            var t, n = [],
                i = this,
                r = i.length;
            if ("string" != typeof e) return this.pushStack(f(e).filter(function() {
                for (t = 0; r > t; t++)
                    if (f.contains(i[t], this)) return !0
            }));
            for (t = 0; r > t; t++) f.find(e, i[t], n);
            return (n = this.pushStack(r > 1 ? f.unique(n) : n)).selector = this.selector ? this.selector + " " + e : e, n
        },
        filter: function(e) {
            return this.pushStack(C(this, e || [], !1))
        },
        not: function(e) {
            return this.pushStack(C(this, e || [], !0))
        },
        is: function(e) {
            return !!C(this, "string" == typeof e && k.test(e) ? f(e) : e || [], !1).length
        }
    });
    var E, S = /^(?:\s*(<[\w\W]+>)[^>]*|#([\w-]*))$/;
    (f.fn.init = function(e, t, n) {
        var r, o;
        if (!e) return this;
        if (n = n || E, "string" == typeof e) {
            if (!(r = "<" === e.charAt(0) && ">" === e.charAt(e.length - 1) && e.length >= 3 ? [null, e, null] : S.exec(e)) || !r[1] && t) return !t || t.jquery ? (t || n).find(e) : this.constructor(t).find(e);
            if (r[1]) {
                if (t = t instanceof f ? t[0] : t, f.merge(this, f.parseHTML(r[1], t && t.nodeType ? t.ownerDocument || t : i, !0)), _.test(r[1]) && f.isPlainObject(t))
                    for (r in t) f.isFunction(this[r]) ? this[r](t[r]) : this.attr(r, t[r]);
                return this
            }
            if ((o = i.getElementById(r[2])) && o.parentNode) {
                if (o.id !== r[2]) return E.find(e);
                this.length = 1, this[0] = o
            }
            return this.context = i, this.selector = e, this
        }
        return e.nodeType ? (this.context = this[0] = e, this.length = 1, this) : f.isFunction(e) ? void 0 !== n.ready ? n.ready(e) : e(f) : (void 0 !== e.selector && (this.selector = e.selector, this.context = e.context), f.makeArray(e, this))
    }).prototype = f.fn, E = f(i);
    var A = /^(?:parents|prev(?:Until|All))/,
        N = {
            children: !0,
            contents: !0,
            next: !0,
            prev: !0
        };

    function j(e, t) {
        do {
            e = e[t]
        } while (e && 1 !== e.nodeType);
        return e
    }
    f.fn.extend({
        has: function(e) {
            var t, n = f(e, this),
                i = n.length;
            return this.filter(function() {
                for (t = 0; i > t; t++)
                    if (f.contains(this, n[t])) return !0
            })
        },
        closest: function(e, t) {
            for (var n, i = 0, r = this.length, o = [], a = k.test(e) || "string" != typeof e ? f(e, t || this.context) : 0; r > i; i++)
                for (n = this[i]; n && n !== t; n = n.parentNode)
                    if (n.nodeType < 11 && (a ? a.index(n) > -1 : 1 === n.nodeType && f.find.matchesSelector(n, e))) {
                        o.push(n);
                        break
                    } return this.pushStack(o.length > 1 ? f.uniqueSort(o) : o)
        },
        index: function(e) {
            return e ? "string" == typeof e ? f.inArray(this[0], f(e)) : f.inArray(e.jquery ? e[0] : e, this) : this[0] && this[0].parentNode ? this.first().prevAll().length : -1
        },
        add: function(e, t) {
            return this.pushStack(f.uniqueSort(f.merge(this.get(), f(e, t))))
        },
        addBack: function(e) {
            return this.add(null == e ? this.prevObject : this.prevObject.filter(e))
        }
    }), f.each({
        parent: function(e) {
            var t = e.parentNode;
            return t && 11 !== t.nodeType ? t : null
        },
        parents: function(e) {
            return x(e, "parentNode")
        },
        parentsUntil: function(e, t, n) {
            return x(e, "parentNode", n)
        },
        next: function(e) {
            return j(e, "nextSibling")
        },
        prev: function(e) {
            return j(e, "previousSibling")
        },
        nextAll: function(e) {
            return x(e, "nextSibling")
        },
        prevAll: function(e) {
            return x(e, "previousSibling")
        },
        nextUntil: function(e, t, n) {
            return x(e, "nextSibling", n)
        },
        prevUntil: function(e, t, n) {
            return x(e, "previousSibling", n)
        },
        siblings: function(e) {
            return w((e.parentNode || {}).firstChild, e)
        },
        children: function(e) {
            return w(e.firstChild)
        },
        contents: function(e) {
            return f.nodeName(e, "iframe") ? e.contentDocument || e.contentWindow.document : f.merge([], e.childNodes)
        }
    }, function(e, t) {
        f.fn[e] = function(n, i) {
            var r = f.map(this, t, n);
            return "Until" !== e.slice(-5) && (i = n), i && "string" == typeof i && (r = f.filter(i, r)), this.length > 1 && (N[e] || (r = f.uniqueSort(r)), A.test(e) && (r = r.reverse())), this.pushStack(r)
        }
    });
    var D, L, q = /\S+/g;

    function M() {
        i.addEventListener ? (i.removeEventListener("DOMContentLoaded", H), e.removeEventListener("load", H)) : (i.detachEvent("onreadystatechange", H), e.detachEvent("onload", H))
    }

    function H() {
        (i.addEventListener || "load" === e.event.type || "complete" === i.readyState) && (M(), f.ready())
    }
    for (L in f.Callbacks = function(e) {
            e = "string" == typeof e ? function(e) {
                var t = {};
                return f.each(e.match(q) || [], function(e, n) {
                    t[n] = !0
                }), t
            }(e) : f.extend({}, e);
            var t, n, i, r, o = [],
                a = [],
                s = -1,
                l = function() {
                    for (r = e.once, i = t = !0; a.length; s = -1)
                        for (n = a.shift(); ++s < o.length;) !1 === o[s].apply(n[0], n[1]) && e.stopOnFalse && (s = o.length, n = !1);
                    e.memory || (n = !1), t = !1, r && (o = n ? [] : "")
                },
                c = {
                    add: function() {
                        return o && (n && !t && (s = o.length - 1, a.push(n)), function t(n) {
                            f.each(n, function(n, i) {
                                f.isFunction(i) ? e.unique && c.has(i) || o.push(i) : i && i.length && "string" !== f.type(i) && t(i)
                            })
                        }(arguments), n && !t && l()), this
                    },
                    remove: function() {
                        return f.each(arguments, function(e, t) {
                            for (var n;
                                (n = f.inArray(t, o, n)) > -1;) o.splice(n, 1), s >= n && s--
                        }), this
                    },
                    has: function(e) {
                        return e ? f.inArray(e, o) > -1 : o.length > 0
                    },
                    empty: function() {
                        return o && (o = []), this
                    },
                    disable: function() {
                        return r = a = [], o = n = "", this
                    },
                    disabled: function() {
                        return !o
                    },
                    lock: function() {
                        return r = !0, n || c.disable(), this
                    },
                    locked: function() {
                        return !!r
                    },
                    fireWith: function(e, n) {
                        return r || (n = [e, (n = n || []).slice ? n.slice() : n], a.push(n), t || l()), this
                    },
                    fire: function() {
                        return c.fireWith(this, arguments), this
                    },
                    fired: function() {
                        return !!i
                    }
                };
            return c
        }, f.extend({
            Deferred: function(e) {
                var t = [
                        ["resolve", "done", f.Callbacks("once memory"), "resolved"],
                        ["reject", "fail", f.Callbacks("once memory"), "rejected"],
                        ["notify", "progress", f.Callbacks("memory")]
                    ],
                    n = "pending",
                    i = {
                        state: function() {
                            return n
                        },
                        always: function() {
                            return r.done(arguments).fail(arguments), this
                        },
                        then: function() {
                            var e = arguments;
                            return f.Deferred(function(n) {
                                f.each(t, function(t, o) {
                                    var a = f.isFunction(e[t]) && e[t];
                                    r[o[1]](function() {
                                        var e = a && a.apply(this, arguments);
                                        e && f.isFunction(e.promise) ? e.promise().progress(n.notify).done(n.resolve).fail(n.reject) : n[o[0] + "With"](this === i ? n.promise() : this, a ? [e] : arguments)
                                    })
                                }), e = null
                            }).promise()
                        },
                        promise: function(e) {
                            return null != e ? f.extend(e, i) : i
                        }
                    },
                    r = {};
                return i.pipe = i.then, f.each(t, function(e, o) {
                    var a = o[2],
                        s = o[3];
                    i[o[1]] = a.add, s && a.add(function() {
                        n = s
                    }, t[1 ^ e][2].disable, t[2][2].lock), r[o[0]] = function() {
                        return r[o[0] + "With"](this === r ? i : this, arguments), this
                    }, r[o[0] + "With"] = a.fireWith
                }), i.promise(r), e && e.call(r, r), r
            },
            when: function(e) {
                var t, n, i, o = 0,
                    a = r.call(arguments),
                    s = a.length,
                    l = 1 !== s || e && f.isFunction(e.promise) ? s : 0,
                    c = 1 === l ? e : f.Deferred(),
                    u = function(e, n, i) {
                        return function(o) {
                            n[e] = this, i[e] = arguments.length > 1 ? r.call(arguments) : o, i === t ? c.notifyWith(n, i) : --l || c.resolveWith(n, i)
                        }
                    };
                if (s > 1)
                    for (t = new Array(s), n = new Array(s), i = new Array(s); s > o; o++) a[o] && f.isFunction(a[o].promise) ? a[o].promise().progress(u(o, n, t)).done(u(o, i, a)).fail(c.reject) : --l;
                return l || c.resolveWith(i, a), c.promise()
            }
        }), f.fn.ready = function(e) {
            return f.ready.promise().done(e), this
        }, f.extend({
            isReady: !1,
            readyWait: 1,
            holdReady: function(e) {
                e ? f.readyWait++ : f.ready(!0)
            },
            ready: function(e) {
                (!0 === e ? --f.readyWait : f.isReady) || (f.isReady = !0, !0 !== e && --f.readyWait > 0 || (D.resolveWith(i, [f]), f.fn.triggerHandler && (f(i).triggerHandler("ready"), f(i).off("ready"))))
            }
        }), f.ready.promise = function(t) {
            if (!D)
                if (D = f.Deferred(), "complete" === i.readyState || "loading" !== i.readyState && !i.documentElement.doScroll) e.setTimeout(f.ready);
                else if (i.addEventListener) i.addEventListener("DOMContentLoaded", H), e.addEventListener("load", H);
            else {
                i.attachEvent("onreadystatechange", H), e.attachEvent("onload", H);
                var n = !1;
                try {
                    n = null == e.frameElement && i.documentElement
                } catch (e) {}
                n && n.doScroll && function t() {
                    if (!f.isReady) {
                        try {
                            n.doScroll("left")
                        } catch (n) {
                            return e.setTimeout(t, 50)
                        }
                        M(), f.ready()
                    }
                }()
            }
            return D.promise(t)
        }, f.ready.promise(), f(d)) break;
    d.ownFirst = "0" === L, d.inlineBlockNeedsLayout = !1, f(function() {
            var e, t, n, r;
            (n = i.getElementsByTagName("body")[0]) && n.style && (t = i.createElement("div"), (r = i.createElement("div")).style.cssText = "position:absolute;border:0;width:0;height:0;top:0;left:-9999px", n.appendChild(r).appendChild(t), void 0 !== t.style.zoom && (t.style.cssText = "display:inline;margin:0;border:0;padding:1px;width:1px;zoom:1", d.inlineBlockNeedsLayout = e = 3 === t.offsetWidth, e && (n.style.zoom = 1)), n.removeChild(r))
        }),
        function() {
            var e = i.createElement("div");
            d.deleteExpando = !0;
            try {
                delete e.test
            } catch (e) {
                d.deleteExpando = !1
            }
            e = null
        }();
    var F = function(e) {
            var t = f.noData[(e.nodeName + " ").toLowerCase()],
                n = +e.nodeType || 1;
            return (1 === n || 9 === n) && (!t || !0 !== t && e.getAttribute("classid") === t)
        },
        P = /^(?:\{[\w\W]*\}|\[[\w\W]*\])$/,
        O = /([A-Z])/g;

    function z(e, t, n) {
        if (void 0 === n && 1 === e.nodeType) {
            var i = "data-" + t.replace(O, "-$1").toLowerCase();
            if ("string" == typeof(n = e.getAttribute(i))) {
                try {
                    n = "true" === n || "false" !== n && ("null" === n ? null : +n + "" === n ? +n : P.test(n) ? f.parseJSON(n) : n)
                } catch (e) {}
                f.data(e, t, n)
            } else n = void 0
        }
        return n
    }

    function R(e) {
        var t;
        for (t in e)
            if (("data" !== t || !f.isEmptyObject(e[t])) && "toJSON" !== t) return !1;
        return !0
    }

    function I(e, t, i, r) {
        if (F(e)) {
            var o, a, s = f.expando,
                l = e.nodeType,
                c = l ? f.cache : e,
                u = l ? e[s] : e[s] && s;
            if (u && c[u] && (r || c[u].data) || void 0 !== i || "string" != typeof t) return u || (u = l ? e[s] = n.pop() || f.guid++ : s), c[u] || (c[u] = l ? {} : {
                toJSON: f.noop
            }), "object" != typeof t && "function" != typeof t || (r ? c[u] = f.extend(c[u], t) : c[u].data = f.extend(c[u].data, t)), a = c[u], r || (a.data || (a.data = {}), a = a.data), void 0 !== i && (a[f.camelCase(t)] = i), "string" == typeof t ? null == (o = a[t]) && (o = a[f.camelCase(t)]) : o = a, o
        }
    }

    function W(e, t, n) {
        if (F(e)) {
            var i, r, o = e.nodeType,
                a = o ? f.cache : e,
                s = o ? e[f.expando] : f.expando;
            if (a[s]) {
                if (t && (i = n ? a[s] : a[s].data)) {
                    f.isArray(t) ? t = t.concat(f.map(t, f.camelCase)) : t in i ? t = [t] : t = (t = f.camelCase(t)) in i ? [t] : t.split(" "), r = t.length;
                    for (; r--;) delete i[t[r]];
                    if (n ? !R(i) : !f.isEmptyObject(i)) return
                }(n || (delete a[s].data, R(a[s]))) && (o ? f.cleanData([e], !0) : d.deleteExpando || a != a.window ? delete a[s] : a[s] = void 0)
            }
        }
    }
    f.extend({
            cache: {},
            noData: {
                "applet ": !0,
                "embed ": !0,
                "object ": "clsid:D27CDB6E-AE6D-11cf-96B8-444553540000"
            },
            hasData: function(e) {
                return !!(e = e.nodeType ? f.cache[e[f.expando]] : e[f.expando]) && !R(e)
            },
            data: function(e, t, n) {
                return I(e, t, n)
            },
            removeData: function(e, t) {
                return W(e, t)
            },
            _data: function(e, t, n) {
                return I(e, t, n, !0)
            },
            _removeData: function(e, t) {
                return W(e, t, !0)
            }
        }), f.fn.extend({
            data: function(e, t) {
                var n, i, r, o = this[0],
                    a = o && o.attributes;
                if (void 0 === e) {
                    if (this.length && (r = f.data(o), 1 === o.nodeType && !f._data(o, "parsedAttrs"))) {
                        for (n = a.length; n--;) a[n] && (0 === (i = a[n].name).indexOf("data-") && z(o, i = f.camelCase(i.slice(5)), r[i]));
                        f._data(o, "parsedAttrs", !0)
                    }
                    return r
                }
                return "object" == typeof e ? this.each(function() {
                    f.data(this, e)
                }) : arguments.length > 1 ? this.each(function() {
                    f.data(this, e, t)
                }) : o ? z(o, e, f.data(o, e)) : void 0
            },
            removeData: function(e) {
                return this.each(function() {
                    f.removeData(this, e)
                })
            }
        }), f.extend({
            queue: function(e, t, n) {
                var i;
                return e ? (t = (t || "fx") + "queue", i = f._data(e, t), n && (!i || f.isArray(n) ? i = f._data(e, t, f.makeArray(n)) : i.push(n)), i || []) : void 0
            },
            dequeue: function(e, t) {
                t = t || "fx";
                var n = f.queue(e, t),
                    i = n.length,
                    r = n.shift(),
                    o = f._queueHooks(e, t);
                "inprogress" === r && (r = n.shift(), i--), r && ("fx" === t && n.unshift("inprogress"), delete o.stop, r.call(e, function() {
                    f.dequeue(e, t)
                }, o)), !i && o && o.empty.fire()
            },
            _queueHooks: function(e, t) {
                var n = t + "queueHooks";
                return f._data(e, n) || f._data(e, n, {
                    empty: f.Callbacks("once memory").add(function() {
                        f._removeData(e, t + "queue"), f._removeData(e, n)
                    })
                })
            }
        }), f.fn.extend({
            queue: function(e, t) {
                var n = 2;
                return "string" != typeof e && (t = e, e = "fx", n--), arguments.length < n ? f.queue(this[0], e) : void 0 === t ? this : this.each(function() {
                    var n = f.queue(this, e, t);
                    f._queueHooks(this, e), "fx" === e && "inprogress" !== n[0] && f.dequeue(this, e)
                })
            },
            dequeue: function(e) {
                return this.each(function() {
                    f.dequeue(this, e)
                })
            },
            clearQueue: function(e) {
                return this.queue(e || "fx", [])
            },
            promise: function(e, t) {
                var n, i = 1,
                    r = f.Deferred(),
                    o = this,
                    a = this.length,
                    s = function() {
                        --i || r.resolveWith(o, [o])
                    };
                for ("string" != typeof e && (t = e, e = void 0), e = e || "fx"; a--;)(n = f._data(o[a], e + "queueHooks")) && n.empty && (i++, n.empty.add(s));
                return s(), r.promise(t)
            }
        }),
        function() {
            var e;
            d.shrinkWrapBlocks = function() {
                return null != e ? e : (e = !1, (n = i.getElementsByTagName("body")[0]) && n.style ? (t = i.createElement("div"), (r = i.createElement("div")).style.cssText = "position:absolute;border:0;width:0;height:0;top:0;left:-9999px", n.appendChild(r).appendChild(t), void 0 !== t.style.zoom && (t.style.cssText = "-webkit-box-sizing:content-box;-moz-box-sizing:content-box;box-sizing:content-box;display:block;margin:0;border:0;padding:1px;width:1px;zoom:1", t.appendChild(i.createElement("div")).style.width = "5px", e = 3 !== t.offsetWidth), n.removeChild(r), e) : void 0);
                var t, n, r
            }
        }();
    var B = /[+-]?(?:\d*\.|)\d+(?:[eE][+-]?\d+|)/.source,
        $ = new RegExp("^(?:([+-])=|)(" + B + ")([a-z%]*)$", "i"),
        X = ["Top", "Right", "Bottom", "Left"],
        J = function(e, t) {
            return e = t || e, "none" === f.css(e, "display") || !f.contains(e.ownerDocument, e)
        };

    function U(e, t, n, i) {
        var r, o = 1,
            a = 20,
            s = i ? function() {
                return i.cur()
            } : function() {
                return f.css(e, t, "")
            },
            l = s(),
            c = n && n[3] || (f.cssNumber[t] ? "" : "px"),
            u = (f.cssNumber[t] || "px" !== c && +l) && $.exec(f.css(e, t));
        if (u && u[3] !== c) {
            c = c || u[3], n = n || [], u = +l || 1;
            do {
                u /= o = o || ".5", f.style(e, t, u + c)
            } while (o !== (o = s() / l) && 1 !== o && --a)
        }
        return n && (u = +u || +l || 0, r = n[1] ? u + (n[1] + 1) * n[2] : +n[2], i && (i.unit = c, i.start = u, i.end = r)), r
    }
    var V = function(e, t, n, i, r, o, a) {
            var s = 0,
                l = e.length,
                c = null == n;
            if ("object" === f.type(n))
                for (s in r = !0, n) V(e, t, s, n[s], !0, o, a);
            else if (void 0 !== i && (r = !0, f.isFunction(i) || (a = !0), c && (a ? (t.call(e, i), t = null) : (c = t, t = function(e, t, n) {
                    return c.call(f(e), n)
                })), t))
                for (; l > s; s++) t(e[s], n, a ? i : i.call(e[s], s, t(e[s], n)));
            return r ? e : c ? t.call(e) : l ? t(e[0], n) : o
        },
        Y = /^(?:checkbox|radio)$/i,
        G = /<([\w:-]+)/,
        Q = /^$|\/(?:java|ecma)script/i,
        K = /^\s+/,
        Z = "abbr|article|aside|audio|bdi|canvas|data|datalist|details|dialog|figcaption|figure|footer|header|hgroup|main|mark|meter|nav|output|picture|progress|section|summary|template|time|video";

    function ee(e) {
        var t = Z.split("|"),
            n = e.createDocumentFragment();
        if (n.createElement)
            for (; t.length;) n.createElement(t.pop());
        return n
    }! function() {
        var e = i.createElement("div"),
            t = i.createDocumentFragment(),
            n = i.createElement("input");
        e.innerHTML = "  <link/><table></table><a href='/a'>a</a><input type='checkbox'/>", d.leadingWhitespace = 3 === e.firstChild.nodeType, d.tbody = !e.getElementsByTagName("tbody").length, d.htmlSerialize = !!e.getElementsByTagName("link").length, d.html5Clone = "<:nav></:nav>" !== i.createElement("nav").cloneNode(!0).outerHTML, n.type = "checkbox", n.checked = !0, t.appendChild(n), d.appendChecked = n.checked, e.innerHTML = "<textarea>x</textarea>", d.noCloneChecked = !!e.cloneNode(!0).lastChild.defaultValue, t.appendChild(e), (n = i.createElement("input")).setAttribute("type", "radio"), n.setAttribute("checked", "checked"), n.setAttribute("name", "t"), e.appendChild(n), d.checkClone = e.cloneNode(!0).cloneNode(!0).lastChild.checked, d.noCloneEvent = !!e.addEventListener, e[f.expando] = 1, d.attributes = !e.getAttribute(f.expando)
    }();
    var te = {
        option: [1, "<select multiple='multiple'>", "</select>"],
        legend: [1, "<fieldset>", "</fieldset>"],
        area: [1, "<map>", "</map>"],
        param: [1, "<object>", "</object>"],
        thead: [1, "<table>", "</table>"],
        tr: [2, "<table><tbody>", "</tbody></table>"],
        col: [2, "<table><tbody></tbody><colgroup>", "</colgroup></table>"],
        td: [3, "<table><tbody><tr>", "</tr></tbody></table>"],
        _default: d.htmlSerialize ? [0, "", ""] : [1, "X<div>", "</div>"]
    };

    function ne(e, t) {
        var n, i, r = 0,
            o = void 0 !== e.getElementsByTagName ? e.getElementsByTagName(t || "*") : void 0 !== e.querySelectorAll ? e.querySelectorAll(t || "*") : void 0;
        if (!o)
            for (o = [], n = e.childNodes || e; null != (i = n[r]); r++) !t || f.nodeName(i, t) ? o.push(i) : f.merge(o, ne(i, t));
        return void 0 === t || t && f.nodeName(e, t) ? f.merge([e], o) : o
    }

    function ie(e, t) {
        for (var n, i = 0; null != (n = e[i]); i++) f._data(n, "globalEval", !t || f._data(t[i], "globalEval"))
    }
    te.optgroup = te.option, te.tbody = te.tfoot = te.colgroup = te.caption = te.thead, te.th = te.td;
    var re = /<|&#?\w+;/,
        oe = /<tbody/i;

    function ae(e) {
        Y.test(e.type) && (e.defaultChecked = e.checked)
    }

    function se(e, t, n, i, r) {
        for (var o, a, s, l, c, u, p, h = e.length, v = ee(t), m = [], y = 0; h > y; y++)
            if ((a = e[y]) || 0 === a)
                if ("object" === f.type(a)) f.merge(m, a.nodeType ? [a] : a);
                else if (re.test(a)) {
            for (l = l || v.appendChild(t.createElement("div")), c = (G.exec(a) || ["", ""])[1].toLowerCase(), p = te[c] || te._default, l.innerHTML = p[1] + f.htmlPrefilter(a) + p[2], o = p[0]; o--;) l = l.lastChild;
            if (!d.leadingWhitespace && K.test(a) && m.push(t.createTextNode(K.exec(a)[0])), !d.tbody)
                for (o = (a = "table" !== c || oe.test(a) ? "<table>" !== p[1] || oe.test(a) ? 0 : l : l.firstChild) && a.childNodes.length; o--;) f.nodeName(u = a.childNodes[o], "tbody") && !u.childNodes.length && a.removeChild(u);
            for (f.merge(m, l.childNodes), l.textContent = ""; l.firstChild;) l.removeChild(l.firstChild);
            l = v.lastChild
        } else m.push(t.createTextNode(a));
        for (l && v.removeChild(l), d.appendChecked || f.grep(ne(m, "input"), ae), y = 0; a = m[y++];)
            if (i && f.inArray(a, i) > -1) r && r.push(a);
            else if (s = f.contains(a.ownerDocument, a), l = ne(v.appendChild(a), "script"), s && ie(l), n)
            for (o = 0; a = l[o++];) Q.test(a.type || "") && n.push(a);
        return l = null, v
    }! function() {
        var t, n, r = i.createElement("div");
        for (t in {
                submit: !0,
                change: !0,
                focusin: !0
            }) n = "on" + t, (d[t] = n in e) || (r.setAttribute(n, "t"), d[t] = !1 === r.attributes[n].expando);
        r = null
    }();
    var le = /^(?:input|select|textarea)$/i,
        ce = /^key/,
        ue = /^(?:mouse|pointer|contextmenu|drag|drop)|click/,
        de = /^(?:focusinfocus|focusoutblur)$/,
        pe = /^([^.]*)(?:\.(.+)|)/;

    function fe() {
        return !0
    }

    function he() {
        return !1
    }

    function ve() {
        try {
            return i.activeElement
        } catch (e) {}
    }

    function me(e, t, n, i, r, o) {
        var a, s;
        if ("object" == typeof t) {
            for (s in "string" != typeof n && (i = i || n, n = void 0), t) me(e, s, n, i, t[s], o);
            return e
        }
        if (null == i && null == r ? (r = n, i = n = void 0) : null == r && ("string" == typeof n ? (r = i, i = void 0) : (r = i, i = n, n = void 0)), !1 === r) r = he;
        else if (!r) return e;
        return 1 === o && (a = r, (r = function(e) {
            return f().off(e), a.apply(this, arguments)
        }).guid = a.guid || (a.guid = f.guid++)), e.each(function() {
            f.event.add(this, t, r, i, n)
        })
    }
    f.event = {
        global: {},
        add: function(e, t, n, i, r) {
            var o, a, s, l, c, u, d, p, h, v, m, y = f._data(e);
            if (y) {
                for (n.handler && (n = (l = n).handler, r = l.selector), n.guid || (n.guid = f.guid++), (a = y.events) || (a = y.events = {}), (u = y.handle) || ((u = y.handle = function(e) {
                        return void 0 === f || e && f.event.triggered === e.type ? void 0 : f.event.dispatch.apply(u.elem, arguments)
                    }).elem = e), s = (t = (t || "").match(q) || [""]).length; s--;) h = m = (o = pe.exec(t[s]) || [])[1], v = (o[2] || "").split(".").sort(), h && (c = f.event.special[h] || {}, h = (r ? c.delegateType : c.bindType) || h, c = f.event.special[h] || {}, d = f.extend({
                    type: h,
                    origType: m,
                    data: i,
                    handler: n,
                    guid: n.guid,
                    selector: r,
                    needsContext: r && f.expr.match.needsContext.test(r),
                    namespace: v.join(".")
                }, l), (p = a[h]) || ((p = a[h] = []).delegateCount = 0, c.setup && !1 !== c.setup.call(e, i, v, u) || (e.addEventListener ? e.addEventListener(h, u, !1) : e.attachEvent && e.attachEvent("on" + h, u))), c.add && (c.add.call(e, d), d.handler.guid || (d.handler.guid = n.guid)), r ? p.splice(p.delegateCount++, 0, d) : p.push(d), f.event.global[h] = !0);
                e = null
            }
        },
        remove: function(e, t, n, i, r) {
            var o, a, s, l, c, u, d, p, h, v, m, y = f.hasData(e) && f._data(e);
            if (y && (u = y.events)) {
                for (c = (t = (t || "").match(q) || [""]).length; c--;)
                    if (h = m = (s = pe.exec(t[c]) || [])[1], v = (s[2] || "").split(".").sort(), h) {
                        for (d = f.event.special[h] || {}, p = u[h = (i ? d.delegateType : d.bindType) || h] || [], s = s[2] && new RegExp("(^|\\.)" + v.join("\\.(?:.*\\.|)") + "(\\.|$)"), l = o = p.length; o--;) a = p[o], !r && m !== a.origType || n && n.guid !== a.guid || s && !s.test(a.namespace) || i && i !== a.selector && ("**" !== i || !a.selector) || (p.splice(o, 1), a.selector && p.delegateCount--, d.remove && d.remove.call(e, a));
                        l && !p.length && (d.teardown && !1 !== d.teardown.call(e, v, y.handle) || f.removeEvent(e, h, y.handle), delete u[h])
                    } else
                        for (h in u) f.event.remove(e, h + t[c], n, i, !0);
                f.isEmptyObject(u) && (delete y.handle, f._removeData(e, "events"))
            }
        },
        trigger: function(t, n, r, o) {
            var a, s, l, c, d, p, h, v = [r || i],
                m = u.call(t, "type") ? t.type : t,
                y = u.call(t, "namespace") ? t.namespace.split(".") : [];
            if (l = p = r = r || i, 3 !== r.nodeType && 8 !== r.nodeType && !de.test(m + f.event.triggered) && (m.indexOf(".") > -1 && (y = m.split("."), m = y.shift(), y.sort()), s = m.indexOf(":") < 0 && "on" + m, (t = t[f.expando] ? t : new f.Event(m, "object" == typeof t && t)).isTrigger = o ? 2 : 3, t.namespace = y.join("."), t.rnamespace = t.namespace ? new RegExp("(^|\\.)" + y.join("\\.(?:.*\\.|)") + "(\\.|$)") : null, t.result = void 0, t.target || (t.target = r), n = null == n ? [t] : f.makeArray(n, [t]), d = f.event.special[m] || {}, o || !d.trigger || !1 !== d.trigger.apply(r, n))) {
                if (!o && !d.noBubble && !f.isWindow(r)) {
                    for (c = d.delegateType || m, de.test(c + m) || (l = l.parentNode); l; l = l.parentNode) v.push(l), p = l;
                    p === (r.ownerDocument || i) && v.push(p.defaultView || p.parentWindow || e)
                }
                for (h = 0;
                    (l = v[h++]) && !t.isPropagationStopped();) t.type = h > 1 ? c : d.bindType || m, (a = (f._data(l, "events") || {})[t.type] && f._data(l, "handle")) && a.apply(l, n), (a = s && l[s]) && a.apply && F(l) && (t.result = a.apply(l, n), !1 === t.result && t.preventDefault());
                if (t.type = m, !o && !t.isDefaultPrevented() && (!d._default || !1 === d._default.apply(v.pop(), n)) && F(r) && s && r[m] && !f.isWindow(r)) {
                    (p = r[s]) && (r[s] = null), f.event.triggered = m;
                    try {
                        r[m]()
                    } catch (e) {}
                    f.event.triggered = void 0, p && (r[s] = p)
                }
                return t.result
            }
        },
        dispatch: function(e) {
            e = f.event.fix(e);
            var t, n, i, o, a, s = [],
                l = r.call(arguments),
                c = (f._data(this, "events") || {})[e.type] || [],
                u = f.event.special[e.type] || {};
            if (l[0] = e, e.delegateTarget = this, !u.preDispatch || !1 !== u.preDispatch.call(this, e)) {
                for (s = f.event.handlers.call(this, e, c), t = 0;
                    (o = s[t++]) && !e.isPropagationStopped();)
                    for (e.currentTarget = o.elem, n = 0;
                        (a = o.handlers[n++]) && !e.isImmediatePropagationStopped();) e.rnamespace && !e.rnamespace.test(a.namespace) || (e.handleObj = a, e.data = a.data, void 0 !== (i = ((f.event.special[a.origType] || {}).handle || a.handler).apply(o.elem, l)) && !1 === (e.result = i) && (e.preventDefault(), e.stopPropagation()));
                return u.postDispatch && u.postDispatch.call(this, e), e.result
            }
        },
        handlers: function(e, t) {
            var n, i, r, o, a = [],
                s = t.delegateCount,
                l = e.target;
            if (s && l.nodeType && ("click" !== e.type || isNaN(e.button) || e.button < 1))
                for (; l != this; l = l.parentNode || this)
                    if (1 === l.nodeType && (!0 !== l.disabled || "click" !== e.type)) {
                        for (i = [], n = 0; s > n; n++) void 0 === i[r = (o = t[n]).selector + " "] && (i[r] = o.needsContext ? f(r, this).index(l) > -1 : f.find(r, this, null, [l]).length), i[r] && i.push(o);
                        i.length && a.push({
                            elem: l,
                            handlers: i
                        })
                    } return s < t.length && a.push({
                elem: this,
                handlers: t.slice(s)
            }), a
        },
        fix: function(e) {
            if (e[f.expando]) return e;
            var t, n, r, o = e.type,
                a = e,
                s = this.fixHooks[o];
            for (s || (this.fixHooks[o] = s = ue.test(o) ? this.mouseHooks : ce.test(o) ? this.keyHooks : {}), r = s.props ? this.props.concat(s.props) : this.props, e = new f.Event(a), t = r.length; t--;) e[n = r[t]] = a[n];
            return e.target || (e.target = a.srcElement || i), 3 === e.target.nodeType && (e.target = e.target.parentNode), e.metaKey = !!e.metaKey, s.filter ? s.filter(e, a) : e
        },
        props: "altKey bubbles cancelable ctrlKey currentTarget detail eventPhase metaKey relatedTarget shiftKey target timeStamp view which".split(" "),
        fixHooks: {},
        keyHooks: {
            props: "char charCode key keyCode".split(" "),
            filter: function(e, t) {
                return null == e.which && (e.which = null != t.charCode ? t.charCode : t.keyCode), e
            }
        },
        mouseHooks: {
            props: "button buttons clientX clientY fromElement offsetX offsetY pageX pageY screenX screenY toElement".split(" "),
            filter: function(e, t) {
                var n, r, o, a = t.button,
                    s = t.fromElement;
                return null == e.pageX && null != t.clientX && (o = (r = e.target.ownerDocument || i).documentElement, n = r.body, e.pageX = t.clientX + (o && o.scrollLeft || n && n.scrollLeft || 0) - (o && o.clientLeft || n && n.clientLeft || 0), e.pageY = t.clientY + (o && o.scrollTop || n && n.scrollTop || 0) - (o && o.clientTop || n && n.clientTop || 0)), !e.relatedTarget && s && (e.relatedTarget = s === e.target ? t.toElement : s), e.which || void 0 === a || (e.which = 1 & a ? 1 : 2 & a ? 3 : 4 & a ? 2 : 0), e
            }
        },
        special: {
            load: {
                noBubble: !0
            },
            focus: {
                trigger: function() {
                    if (this !== ve() && this.focus) try {
                        return this.focus(), !1
                    } catch (e) {}
                },
                delegateType: "focusin"
            },
            blur: {
                trigger: function() {
                    return this === ve() && this.blur ? (this.blur(), !1) : void 0
                },
                delegateType: "focusout"
            },
            click: {
                trigger: function() {
                    return f.nodeName(this, "input") && "checkbox" === this.type && this.click ? (this.click(), !1) : void 0
                },
                _default: function(e) {
                    return f.nodeName(e.target, "a")
                }
            },
            beforeunload: {
                postDispatch: function(e) {
                    void 0 !== e.result && e.originalEvent && (e.originalEvent.returnValue = e.result)
                }
            }
        },
        simulate: function(e, t, n) {
            var i = f.extend(new f.Event, n, {
                type: e,
                isSimulated: !0
            });
            f.event.trigger(i, null, t), i.isDefaultPrevented() && n.preventDefault()
        }
    }, f.removeEvent = i.removeEventListener ? function(e, t, n) {
        e.removeEventListener && e.removeEventListener(t, n)
    } : function(e, t, n) {
        var i = "on" + t;
        e.detachEvent && (void 0 === e[i] && (e[i] = null), e.detachEvent(i, n))
    }, f.Event = function(e, t) {
        return this instanceof f.Event ? (e && e.type ? (this.originalEvent = e, this.type = e.type, this.isDefaultPrevented = e.defaultPrevented || void 0 === e.defaultPrevented && !1 === e.returnValue ? fe : he) : this.type = e, t && f.extend(this, t), this.timeStamp = e && e.timeStamp || f.now(), void(this[f.expando] = !0)) : new f.Event(e, t)
    }, f.Event.prototype = {
        constructor: f.Event,
        isDefaultPrevented: he,
        isPropagationStopped: he,
        isImmediatePropagationStopped: he,
        preventDefault: function() {
            var e = this.originalEvent;
            this.isDefaultPrevented = fe, e && (e.preventDefault ? e.preventDefault() : e.returnValue = !1)
        },
        stopPropagation: function() {
            var e = this.originalEvent;
            this.isPropagationStopped = fe, e && !this.isSimulated && (e.stopPropagation && e.stopPropagation(), e.cancelBubble = !0)
        },
        stopImmediatePropagation: function() {
            var e = this.originalEvent;
            this.isImmediatePropagationStopped = fe, e && e.stopImmediatePropagation && e.stopImmediatePropagation(), this.stopPropagation()
        }
    }, f.each({
        mouseenter: "mouseover",
        mouseleave: "mouseout",
        pointerenter: "pointerover",
        pointerleave: "pointerout"
    }, function(e, t) {
        f.event.special[e] = {
            delegateType: t,
            bindType: t,
            handle: function(e) {
                var n, i = e.relatedTarget,
                    r = e.handleObj;
                return i && (i === this || f.contains(this, i)) || (e.type = r.origType, n = r.handler.apply(this, arguments), e.type = t), n
            }
        }
    }), d.submit || (f.event.special.submit = {
        setup: function() {
            return !f.nodeName(this, "form") && void f.event.add(this, "click._submit keypress._submit", function(e) {
                var t = e.target,
                    n = f.nodeName(t, "input") || f.nodeName(t, "button") ? f.prop(t, "form") : void 0;
                n && !f._data(n, "submit") && (f.event.add(n, "submit._submit", function(e) {
                    e._submitBubble = !0
                }), f._data(n, "submit", !0))
            })
        },
        postDispatch: function(e) {
            e._submitBubble && (delete e._submitBubble, this.parentNode && !e.isTrigger && f.event.simulate("submit", this.parentNode, e))
        },
        teardown: function() {
            return !f.nodeName(this, "form") && void f.event.remove(this, "._submit")
        }
    }), d.change || (f.event.special.change = {
        setup: function() {
            return le.test(this.nodeName) ? ("checkbox" !== this.type && "radio" !== this.type || (f.event.add(this, "propertychange._change", function(e) {
                "checked" === e.originalEvent.propertyName && (this._justChanged = !0)
            }), f.event.add(this, "click._change", function(e) {
                this._justChanged && !e.isTrigger && (this._justChanged = !1), f.event.simulate("change", this, e)
            })), !1) : void f.event.add(this, "beforeactivate._change", function(e) {
                var t = e.target;
                le.test(t.nodeName) && !f._data(t, "change") && (f.event.add(t, "change._change", function(e) {
                    !this.parentNode || e.isSimulated || e.isTrigger || f.event.simulate("change", this.parentNode, e)
                }), f._data(t, "change", !0))
            })
        },
        handle: function(e) {
            var t = e.target;
            return this !== t || e.isSimulated || e.isTrigger || "radio" !== t.type && "checkbox" !== t.type ? e.handleObj.handler.apply(this, arguments) : void 0
        },
        teardown: function() {
            return f.event.remove(this, "._change"), !le.test(this.nodeName)
        }
    }), d.focusin || f.each({
        focus: "focusin",
        blur: "focusout"
    }, function(e, t) {
        var n = function(e) {
            f.event.simulate(t, e.target, f.event.fix(e))
        };
        f.event.special[t] = {
            setup: function() {
                var i = this.ownerDocument || this,
                    r = f._data(i, t);
                r || i.addEventListener(e, n, !0), f._data(i, t, (r || 0) + 1)
            },
            teardown: function() {
                var i = this.ownerDocument || this,
                    r = f._data(i, t) - 1;
                r ? f._data(i, t, r) : (i.removeEventListener(e, n, !0), f._removeData(i, t))
            }
        }
    }), f.fn.extend({
        on: function(e, t, n, i) {
            return me(this, e, t, n, i)
        },
        one: function(e, t, n, i) {
            return me(this, e, t, n, i, 1)
        },
        off: function(e, t, n) {
            var i, r;
            if (e && e.preventDefault && e.handleObj) return i = e.handleObj, f(e.delegateTarget).off(i.namespace ? i.origType + "." + i.namespace : i.origType, i.selector, i.handler), this;
            if ("object" == typeof e) {
                for (r in e) this.off(r, t, e[r]);
                return this
            }
            return !1 !== t && "function" != typeof t || (n = t, t = void 0), !1 === n && (n = he), this.each(function() {
                f.event.remove(this, e, n, t)
            })
        },
        trigger: function(e, t) {
            return this.each(function() {
                f.event.trigger(e, t, this)
            })
        },
        triggerHandler: function(e, t) {
            var n = this[0];
            return n ? f.event.trigger(e, t, n, !0) : void 0
        }
    });
    var ye = / jQuery\d+="(?:null|\d+)"/g,
        ge = new RegExp("<(?:" + Z + ")[\\s/>]", "i"),
        be = /<(?!area|br|col|embed|hr|img|input|link|meta|param)(([\w:-]+)[^>]*)\/>/gi,
        xe = /<script|<style|<link/i,
        we = /checked\s*(?:[^=]|=\s*.checked.)/i,
        ke = /^true\/(.*)/,
        _e = /^\s*<!(?:\[CDATA\[|--)|(?:\]\]|--)>\s*$/g,
        Te = ee(i).appendChild(i.createElement("div"));

    function Ce(e, t) {
        return f.nodeName(e, "table") && f.nodeName(11 !== t.nodeType ? t : t.firstChild, "tr") ? e.getElementsByTagName("tbody")[0] || e.appendChild(e.ownerDocument.createElement("tbody")) : e
    }

    function Ee(e) {
        return e.type = (null !== f.find.attr(e, "type")) + "/" + e.type, e
    }

    function Se(e) {
        var t = ke.exec(e.type);
        return t ? e.type = t[1] : e.removeAttribute("type"), e
    }

    function Ae(e, t) {
        if (1 === t.nodeType && f.hasData(e)) {
            var n, i, r, o = f._data(e),
                a = f._data(t, o),
                s = o.events;
            if (s)
                for (n in delete a.handle, a.events = {}, s)
                    for (i = 0, r = s[n].length; r > i; i++) f.event.add(t, n, s[n][i]);
            a.data && (a.data = f.extend({}, a.data))
        }
    }

    function Ne(e, t) {
        var n, i, r;
        if (1 === t.nodeType) {
            if (n = t.nodeName.toLowerCase(), !d.noCloneEvent && t[f.expando]) {
                for (i in (r = f._data(t)).events) f.removeEvent(t, i, r.handle);
                t.removeAttribute(f.expando)
            }
            "script" === n && t.text !== e.text ? (Ee(t).text = e.text, Se(t)) : "object" === n ? (t.parentNode && (t.outerHTML = e.outerHTML), d.html5Clone && e.innerHTML && !f.trim(t.innerHTML) && (t.innerHTML = e.innerHTML)) : "input" === n && Y.test(e.type) ? (t.defaultChecked = t.checked = e.checked, t.value !== e.value && (t.value = e.value)) : "option" === n ? t.defaultSelected = t.selected = e.defaultSelected : "input" !== n && "textarea" !== n || (t.defaultValue = e.defaultValue)
        }
    }

    function je(e, t, n, i) {
        t = o.apply([], t);
        var r, a, s, l, c, u, p = 0,
            h = e.length,
            v = h - 1,
            m = t[0],
            y = f.isFunction(m);
        if (y || h > 1 && "string" == typeof m && !d.checkClone && we.test(m)) return e.each(function(r) {
            var o = e.eq(r);
            y && (t[0] = m.call(this, r, o.html())), je(o, t, n, i)
        });
        if (h && (r = (u = se(t, e[0].ownerDocument, !1, e, i)).firstChild, 1 === u.childNodes.length && (u = r), r || i)) {
            for (s = (l = f.map(ne(u, "script"), Ee)).length; h > p; p++) a = u, p !== v && (a = f.clone(a, !0, !0), s && f.merge(l, ne(a, "script"))), n.call(e[p], a, p);
            if (s)
                for (c = l[l.length - 1].ownerDocument, f.map(l, Se), p = 0; s > p; p++) a = l[p], Q.test(a.type || "") && !f._data(a, "globalEval") && f.contains(c, a) && (a.src ? f._evalUrl && f._evalUrl(a.src) : f.globalEval((a.text || a.textContent || a.innerHTML || "").replace(_e, "")));
            u = r = null
        }
        return e
    }

    function De(e, t, n) {
        for (var i, r = t ? f.filter(t, e) : e, o = 0; null != (i = r[o]); o++) n || 1 !== i.nodeType || f.cleanData(ne(i)), i.parentNode && (n && f.contains(i.ownerDocument, i) && ie(ne(i, "script")), i.parentNode.removeChild(i));
        return e
    }
    f.extend({
        htmlPrefilter: function(e) {
            return e.replace(be, "<$1></$2>")
        },
        clone: function(e, t, n) {
            var i, r, o, a, s, l = f.contains(e.ownerDocument, e);
            if (d.html5Clone || f.isXMLDoc(e) || !ge.test("<" + e.nodeName + ">") ? o = e.cloneNode(!0) : (Te.innerHTML = e.outerHTML, Te.removeChild(o = Te.firstChild)), !(d.noCloneEvent && d.noCloneChecked || 1 !== e.nodeType && 11 !== e.nodeType || f.isXMLDoc(e)))
                for (i = ne(o), s = ne(e), a = 0; null != (r = s[a]); ++a) i[a] && Ne(r, i[a]);
            if (t)
                if (n)
                    for (s = s || ne(e), i = i || ne(o), a = 0; null != (r = s[a]); a++) Ae(r, i[a]);
                else Ae(e, o);
            return (i = ne(o, "script")).length > 0 && ie(i, !l && ne(e, "script")), i = s = r = null, o
        },
        cleanData: function(e, t) {
            for (var i, r, o, a, s = 0, l = f.expando, c = f.cache, u = d.attributes, p = f.event.special; null != (i = e[s]); s++)
                if ((t || F(i)) && (a = (o = i[l]) && c[o])) {
                    if (a.events)
                        for (r in a.events) p[r] ? f.event.remove(i, r) : f.removeEvent(i, r, a.handle);
                    c[o] && (delete c[o], u || void 0 === i.removeAttribute ? i[l] = void 0 : i.removeAttribute(l), n.push(o))
                }
        }
    }), f.fn.extend({
        domManip: je,
        detach: function(e) {
            return De(this, e, !0)
        },
        remove: function(e) {
            return De(this, e)
        },
        text: function(e) {
            return V(this, function(e) {
                return void 0 === e ? f.text(this) : this.empty().append((this[0] && this[0].ownerDocument || i).createTextNode(e))
            }, null, e, arguments.length)
        },
        append: function() {
            return je(this, arguments, function(e) {
                1 !== this.nodeType && 11 !== this.nodeType && 9 !== this.nodeType || Ce(this, e).appendChild(e)
            })
        },
        prepend: function() {
            return je(this, arguments, function(e) {
                if (1 === this.nodeType || 11 === this.nodeType || 9 === this.nodeType) {
                    var t = Ce(this, e);
                    t.insertBefore(e, t.firstChild)
                }
            })
        },
        before: function() {
            return je(this, arguments, function(e) {
                this.parentNode && this.parentNode.insertBefore(e, this)
            })
        },
        after: function() {
            return je(this, arguments, function(e) {
                this.parentNode && this.parentNode.insertBefore(e, this.nextSibling)
            })
        },
        empty: function() {
            for (var e, t = 0; null != (e = this[t]); t++) {
                for (1 === e.nodeType && f.cleanData(ne(e, !1)); e.firstChild;) e.removeChild(e.firstChild);
                e.options && f.nodeName(e, "select") && (e.options.length = 0)
            }
            return this
        },
        clone: function(e, t) {
            return e = null != e && e, t = null == t ? e : t, this.map(function() {
                return f.clone(this, e, t)
            })
        },
        html: function(e) {
            return V(this, function(e) {
                var t = this[0] || {},
                    n = 0,
                    i = this.length;
                if (void 0 === e) return 1 === t.nodeType ? t.innerHTML.replace(ye, "") : void 0;
                if ("string" == typeof e && !xe.test(e) && (d.htmlSerialize || !ge.test(e)) && (d.leadingWhitespace || !K.test(e)) && !te[(G.exec(e) || ["", ""])[1].toLowerCase()]) {
                    e = f.htmlPrefilter(e);
                    try {
                        for (; i > n; n++) 1 === (t = this[n] || {}).nodeType && (f.cleanData(ne(t, !1)), t.innerHTML = e);
                        t = 0
                    } catch (e) {}
                }
                t && this.empty().append(e)
            }, null, e, arguments.length)
        },
        replaceWith: function() {
            var e = [];
            return je(this, arguments, function(t) {
                var n = this.parentNode;
                f.inArray(this, e) < 0 && (f.cleanData(ne(this)), n && n.replaceChild(t, this))
            }, e)
        }
    }), f.each({
        appendTo: "append",
        prependTo: "prepend",
        insertBefore: "before",
        insertAfter: "after",
        replaceAll: "replaceWith"
    }, function(e, t) {
        f.fn[e] = function(e) {
            for (var n, i = 0, r = [], o = f(e), s = o.length - 1; s >= i; i++) n = i === s ? this : this.clone(!0), f(o[i])[t](n), a.apply(r, n.get());
            return this.pushStack(r)
        }
    });
    var Le, qe = {
        HTML: "block",
        BODY: "block"
    };

    function Me(e, t) {
        var n = f(t.createElement(e)).appendTo(t.body),
            i = f.css(n[0], "display");
        return n.detach(), i
    }

    function He(e) {
        var t = i,
            n = qe[e];
        return n || ("none" !== (n = Me(e, t)) && n || ((t = ((Le = (Le || f("<iframe frameborder='0' width='0' height='0'/>")).appendTo(t.documentElement))[0].contentWindow || Le[0].contentDocument).document).write(), t.close(), n = Me(e, t), Le.detach()), qe[e] = n), n
    }
    var Fe = /^margin/,
        Pe = new RegExp("^(" + B + ")(?!px)[a-z%]+$", "i"),
        Oe = function(e, t, n, i) {
            var r, o, a = {};
            for (o in t) a[o] = e.style[o], e.style[o] = t[o];
            for (o in r = n.apply(e, i || []), t) e.style[o] = a[o];
            return r
        },
        ze = i.documentElement;
    ! function() {
        var t, n, r, o, a, s, l = i.createElement("div"),
            c = i.createElement("div");
        if (c.style) {
            function u() {
                var u, d, p = i.documentElement;
                p.appendChild(l), c.style.cssText = "-webkit-box-sizing:border-box;box-sizing:border-box;position:relative;display:block;margin:auto;border:1px;padding:1px;top:1%;width:50%", t = r = s = !1, n = a = !0, e.getComputedStyle && (d = e.getComputedStyle(c), t = "1%" !== (d || {}).top, s = "2px" === (d || {}).marginLeft, r = "4px" === (d || {
                    width: "4px"
                }).width, c.style.marginRight = "50%", n = "4px" === (d || {
                    marginRight: "4px"
                }).marginRight, (u = c.appendChild(i.createElement("div"))).style.cssText = c.style.cssText = "-webkit-box-sizing:content-box;-moz-box-sizing:content-box;box-sizing:content-box;display:block;margin:0;border:0;padding:0", u.style.marginRight = u.style.width = "0", c.style.width = "1px", a = !parseFloat((e.getComputedStyle(u) || {}).marginRight), c.removeChild(u)), c.style.display = "none", (o = 0 === c.getClientRects().length) && (c.style.display = "", c.innerHTML = "<table><tr><td></td><td>t</td></tr></table>", c.childNodes[0].style.borderCollapse = "separate", (u = c.getElementsByTagName("td"))[0].style.cssText = "margin:0;border:0;padding:0;display:none", (o = 0 === u[0].offsetHeight) && (u[0].style.display = "", u[1].style.display = "none", o = 0 === u[0].offsetHeight)), p.removeChild(l)
            }
            c.style.cssText = "float:left;opacity:.5", d.opacity = "0.5" === c.style.opacity, d.cssFloat = !!c.style.cssFloat, c.style.backgroundClip = "content-box", c.cloneNode(!0).style.backgroundClip = "", d.clearCloneStyle = "content-box" === c.style.backgroundClip, (l = i.createElement("div")).style.cssText = "border:0;width:8px;height:0;top:0;left:-9999px;padding:0;margin-top:1px;position:absolute", c.innerHTML = "", l.appendChild(c), d.boxSizing = "" === c.style.boxSizing || "" === c.style.MozBoxSizing || "" === c.style.WebkitBoxSizing, f.extend(d, {
                reliableHiddenOffsets: function() {
                    return null == t && u(), o
                },
                boxSizingReliable: function() {
                    return null == t && u(), r
                },
                pixelMarginRight: function() {
                    return null == t && u(), n
                },
                pixelPosition: function() {
                    return null == t && u(), t
                },
                reliableMarginRight: function() {
                    return null == t && u(), a
                },
                reliableMarginLeft: function() {
                    return null == t && u(), s
                }
            })
        }
    }();
    var Re, Ie, We = /^(top|right|bottom|left)$/;

    function Be(e, t) {
        return {
            get: function() {
                return e() ? void delete this.get : (this.get = t).apply(this, arguments)
            }
        }
    }
    e.getComputedStyle ? (Re = function(t) {
        var n = t.ownerDocument.defaultView;
        return n && n.opener || (n = e), n.getComputedStyle(t)
    }, Ie = function(e, t, n) {
        var i, r, o, a, s = e.style;
        return "" !== (a = (n = n || Re(e)) ? n.getPropertyValue(t) || n[t] : void 0) && void 0 !== a || f.contains(e.ownerDocument, e) || (a = f.style(e, t)), n && !d.pixelMarginRight() && Pe.test(a) && Fe.test(t) && (i = s.width, r = s.minWidth, o = s.maxWidth, s.minWidth = s.maxWidth = s.width = a, a = n.width, s.width = i, s.minWidth = r, s.maxWidth = o), void 0 === a ? a : a + ""
    }) : ze.currentStyle && (Re = function(e) {
        return e.currentStyle
    }, Ie = function(e, t, n) {
        var i, r, o, a, s = e.style;
        return null == (a = (n = n || Re(e)) ? n[t] : void 0) && s && s[t] && (a = s[t]), Pe.test(a) && !We.test(t) && (i = s.left, (o = (r = e.runtimeStyle) && r.left) && (r.left = e.currentStyle.left), s.left = "fontSize" === t ? "1em" : a, a = s.pixelLeft + "px", s.left = i, o && (r.left = o)), void 0 === a ? a : a + "" || "auto"
    });
    var $e = /alpha\([^)]*\)/i,
        Xe = /opacity\s*=\s*([^)]*)/i,
        Je = /^(none|table(?!-c[ea]).+)/,
        Ue = new RegExp("^(" + B + ")(.*)$", "i"),
        Ve = {
            position: "absolute",
            visibility: "hidden",
            display: "block"
        },
        Ye = {
            letterSpacing: "0",
            fontWeight: "400"
        },
        Ge = ["Webkit", "O", "Moz", "ms"],
        Qe = i.createElement("div").style;

    function Ke(e) {
        if (e in Qe) return e;
        for (var t = e.charAt(0).toUpperCase() + e.slice(1), n = Ge.length; n--;)
            if ((e = Ge[n] + t) in Qe) return e
    }

    function Ze(e, t) {
        for (var n, i, r, o = [], a = 0, s = e.length; s > a; a++)(i = e[a]).style && (o[a] = f._data(i, "olddisplay"), n = i.style.display, t ? (o[a] || "none" !== n || (i.style.display = ""), "" === i.style.display && J(i) && (o[a] = f._data(i, "olddisplay", He(i.nodeName)))) : (r = J(i), (n && "none" !== n || !r) && f._data(i, "olddisplay", r ? n : f.css(i, "display"))));
        for (a = 0; s > a; a++)(i = e[a]).style && (t && "none" !== i.style.display && "" !== i.style.display || (i.style.display = t ? o[a] || "" : "none"));
        return e
    }

    function et(e, t, n) {
        var i = Ue.exec(t);
        return i ? Math.max(0, i[1] - (n || 0)) + (i[2] || "px") : t
    }

    function tt(e, t, n, i, r) {
        for (var o = n === (i ? "border" : "content") ? 4 : "width" === t ? 1 : 0, a = 0; 4 > o; o += 2) "margin" === n && (a += f.css(e, n + X[o], !0, r)), i ? ("content" === n && (a -= f.css(e, "padding" + X[o], !0, r)), "margin" !== n && (a -= f.css(e, "border" + X[o] + "Width", !0, r))) : (a += f.css(e, "padding" + X[o], !0, r), "padding" !== n && (a += f.css(e, "border" + X[o] + "Width", !0, r)));
        return a
    }

    function nt(e, t, n) {
        var i = !0,
            r = "width" === t ? e.offsetWidth : e.offsetHeight,
            o = Re(e),
            a = d.boxSizing && "border-box" === f.css(e, "boxSizing", !1, o);
        if (0 >= r || null == r) {
            if ((0 > (r = Ie(e, t, o)) || null == r) && (r = e.style[t]), Pe.test(r)) return r;
            i = a && (d.boxSizingReliable() || r === e.style[t]), r = parseFloat(r) || 0
        }
        return r + tt(e, t, n || (a ? "border" : "content"), i, o) + "px"
    }

    function it(e, t, n, i, r) {
        return new it.prototype.init(e, t, n, i, r)
    }
    f.extend({
        cssHooks: {
            opacity: {
                get: function(e, t) {
                    if (t) {
                        var n = Ie(e, "opacity");
                        return "" === n ? "1" : n
                    }
                }
            }
        },
        cssNumber: {
            animationIterationCount: !0,
            columnCount: !0,
            fillOpacity: !0,
            flexGrow: !0,
            flexShrink: !0,
            fontWeight: !0,
            lineHeight: !0,
            opacity: !0,
            order: !0,
            orphans: !0,
            widows: !0,
            zIndex: !0,
            zoom: !0
        },
        cssProps: {
            float: d.cssFloat ? "cssFloat" : "styleFloat"
        },
        style: function(e, t, n, i) {
            if (e && 3 !== e.nodeType && 8 !== e.nodeType && e.style) {
                var r, o, a, s = f.camelCase(t),
                    l = e.style;
                if (t = f.cssProps[s] || (f.cssProps[s] = Ke(s) || s), a = f.cssHooks[t] || f.cssHooks[s], void 0 === n) return a && "get" in a && void 0 !== (r = a.get(e, !1, i)) ? r : l[t];
                if ("string" === (o = typeof n) && (r = $.exec(n)) && r[1] && (n = U(e, t, r), o = "number"), null != n && n == n && ("number" === o && (n += r && r[3] || (f.cssNumber[s] ? "" : "px")), d.clearCloneStyle || "" !== n || 0 !== t.indexOf("background") || (l[t] = "inherit"), !(a && "set" in a && void 0 === (n = a.set(e, n, i))))) try {
                    l[t] = n
                } catch (e) {}
            }
        },
        css: function(e, t, n, i) {
            var r, o, a, s = f.camelCase(t);
            return t = f.cssProps[s] || (f.cssProps[s] = Ke(s) || s), (a = f.cssHooks[t] || f.cssHooks[s]) && "get" in a && (o = a.get(e, !0, n)), void 0 === o && (o = Ie(e, t, i)), "normal" === o && t in Ye && (o = Ye[t]), "" === n || n ? (r = parseFloat(o), !0 === n || isFinite(r) ? r || 0 : o) : o
        }
    }), f.each(["height", "width"], function(e, t) {
        f.cssHooks[t] = {
            get: function(e, n, i) {
                return n ? Je.test(f.css(e, "display")) && 0 === e.offsetWidth ? Oe(e, Ve, function() {
                    return nt(e, t, i)
                }) : nt(e, t, i) : void 0
            },
            set: function(e, n, i) {
                var r = i && Re(e);
                return et(0, n, i ? tt(e, t, i, d.boxSizing && "border-box" === f.css(e, "boxSizing", !1, r), r) : 0)
            }
        }
    }), d.opacity || (f.cssHooks.opacity = {
        get: function(e, t) {
            return Xe.test((t && e.currentStyle ? e.currentStyle.filter : e.style.filter) || "") ? .01 * parseFloat(RegExp.$1) + "" : t ? "1" : ""
        },
        set: function(e, t) {
            var n = e.style,
                i = e.currentStyle,
                r = f.isNumeric(t) ? "alpha(opacity=" + 100 * t + ")" : "",
                o = i && i.filter || n.filter || "";
            n.zoom = 1, (t >= 1 || "" === t) && "" === f.trim(o.replace($e, "")) && n.removeAttribute && (n.removeAttribute("filter"), "" === t || i && !i.filter) || (n.filter = $e.test(o) ? o.replace($e, r) : o + " " + r)
        }
    }), f.cssHooks.marginRight = Be(d.reliableMarginRight, function(e, t) {
        return t ? Oe(e, {
            display: "inline-block"
        }, Ie, [e, "marginRight"]) : void 0
    }), f.cssHooks.marginLeft = Be(d.reliableMarginLeft, function(e, t) {
        return t ? (parseFloat(Ie(e, "marginLeft")) || (f.contains(e.ownerDocument, e) ? e.getBoundingClientRect().left - Oe(e, {
            marginLeft: 0
        }, function() {
            return e.getBoundingClientRect().left
        }) : 0)) + "px" : void 0
    }), f.each({
        margin: "",
        padding: "",
        border: "Width"
    }, function(e, t) {
        f.cssHooks[e + t] = {
            expand: function(n) {
                for (var i = 0, r = {}, o = "string" == typeof n ? n.split(" ") : [n]; 4 > i; i++) r[e + X[i] + t] = o[i] || o[i - 2] || o[0];
                return r
            }
        }, Fe.test(e) || (f.cssHooks[e + t].set = et)
    }), f.fn.extend({
        css: function(e, t) {
            return V(this, function(e, t, n) {
                var i, r, o = {},
                    a = 0;
                if (f.isArray(t)) {
                    for (i = Re(e), r = t.length; r > a; a++) o[t[a]] = f.css(e, t[a], !1, i);
                    return o
                }
                return void 0 !== n ? f.style(e, t, n) : f.css(e, t)
            }, e, t, arguments.length > 1)
        },
        show: function() {
            return Ze(this, !0)
        },
        hide: function() {
            return Ze(this)
        },
        toggle: function(e) {
            return "boolean" == typeof e ? e ? this.show() : this.hide() : this.each(function() {
                J(this) ? f(this).show() : f(this).hide()
            })
        }
    }), f.Tween = it, it.prototype = {
        constructor: it,
        init: function(e, t, n, i, r, o) {
            this.elem = e, this.prop = n, this.easing = r || f.easing._default, this.options = t, this.start = this.now = this.cur(), this.end = i, this.unit = o || (f.cssNumber[n] ? "" : "px")
        },
        cur: function() {
            var e = it.propHooks[this.prop];
            return e && e.get ? e.get(this) : it.propHooks._default.get(this)
        },
        run: function(e) {
            var t, n = it.propHooks[this.prop];
            return this.options.duration ? this.pos = t = f.easing[this.easing](e, this.options.duration * e, 0, 1, this.options.duration) : this.pos = t = e, this.now = (this.end - this.start) * t + this.start, this.options.step && this.options.step.call(this.elem, this.now, this), n && n.set ? n.set(this) : it.propHooks._default.set(this), this
        }
    }, it.prototype.init.prototype = it.prototype, it.propHooks = {
        _default: {
            get: function(e) {
                var t;
                return 1 !== e.elem.nodeType || null != e.elem[e.prop] && null == e.elem.style[e.prop] ? e.elem[e.prop] : (t = f.css(e.elem, e.prop, "")) && "auto" !== t ? t : 0
            },
            set: function(e) {
                f.fx.step[e.prop] ? f.fx.step[e.prop](e) : 1 !== e.elem.nodeType || null == e.elem.style[f.cssProps[e.prop]] && !f.cssHooks[e.prop] ? e.elem[e.prop] = e.now : f.style(e.elem, e.prop, e.now + e.unit)
            }
        }
    }, it.propHooks.scrollTop = it.propHooks.scrollLeft = {
        set: function(e) {
            e.elem.nodeType && e.elem.parentNode && (e.elem[e.prop] = e.now)
        }
    }, f.easing = {
        linear: function(e) {
            return e
        },
        swing: function(e) {
            return .5 - Math.cos(e * Math.PI) / 2
        },
        _default: "swing"
    }, f.fx = it.prototype.init, f.fx.step = {};
    var rt, ot, at = /^(?:toggle|show|hide)$/,
        st = /queueHooks$/;

    function lt() {
        return e.setTimeout(function() {
            rt = void 0
        }), rt = f.now()
    }

    function ct(e, t) {
        var n, i = {
                height: e
            },
            r = 0;
        for (t = t ? 1 : 0; 4 > r; r += 2 - t) i["margin" + (n = X[r])] = i["padding" + n] = e;
        return t && (i.opacity = i.width = e), i
    }

    function ut(e, t, n) {
        for (var i, r = (dt.tweeners[t] || []).concat(dt.tweeners["*"]), o = 0, a = r.length; a > o; o++)
            if (i = r[o].call(n, t, e)) return i
    }

    function dt(e, t, n) {
        var i, r, o = 0,
            a = dt.prefilters.length,
            s = f.Deferred().always(function() {
                delete l.elem
            }),
            l = function() {
                if (r) return !1;
                for (var t = rt || lt(), n = Math.max(0, c.startTime + c.duration - t), i = 1 - (n / c.duration || 0), o = 0, a = c.tweens.length; a > o; o++) c.tweens[o].run(i);
                return s.notifyWith(e, [c, i, n]), 1 > i && a ? n : (s.resolveWith(e, [c]), !1)
            },
            c = s.promise({
                elem: e,
                props: f.extend({}, t),
                opts: f.extend(!0, {
                    specialEasing: {},
                    easing: f.easing._default
                }, n),
                originalProperties: t,
                originalOptions: n,
                startTime: rt || lt(),
                duration: n.duration,
                tweens: [],
                createTween: function(t, n) {
                    var i = f.Tween(e, c.opts, t, n, c.opts.specialEasing[t] || c.opts.easing);
                    return c.tweens.push(i), i
                },
                stop: function(t) {
                    var n = 0,
                        i = t ? c.tweens.length : 0;
                    if (r) return this;
                    for (r = !0; i > n; n++) c.tweens[n].run(1);
                    return t ? (s.notifyWith(e, [c, 1, 0]), s.resolveWith(e, [c, t])) : s.rejectWith(e, [c, t]), this
                }
            }),
            u = c.props;
        for (function(e, t) {
                var n, i, r, o, a;
                for (n in e)
                    if (r = t[i = f.camelCase(n)], o = e[n], f.isArray(o) && (r = o[1], o = e[n] = o[0]), n !== i && (e[i] = o, delete e[n]), (a = f.cssHooks[i]) && "expand" in a)
                        for (n in o = a.expand(o), delete e[i], o) n in e || (e[n] = o[n], t[n] = r);
                    else t[i] = r
            }(u, c.opts.specialEasing); a > o; o++)
            if (i = dt.prefilters[o].call(c, e, u, c.opts)) return f.isFunction(i.stop) && (f._queueHooks(c.elem, c.opts.queue).stop = f.proxy(i.stop, i)), i;
        return f.map(u, ut, c), f.isFunction(c.opts.start) && c.opts.start.call(e, c), f.fx.timer(f.extend(l, {
            elem: e,
            anim: c,
            queue: c.opts.queue
        })), c.progress(c.opts.progress).done(c.opts.done, c.opts.complete).fail(c.opts.fail).always(c.opts.always)
    }
    f.Animation = f.extend(dt, {
            tweeners: {
                "*": [function(e, t) {
                    var n = this.createTween(e, t);
                    return U(n.elem, e, $.exec(t), n), n
                }]
            },
            tweener: function(e, t) {
                f.isFunction(e) ? (t = e, e = ["*"]) : e = e.match(q);
                for (var n, i = 0, r = e.length; r > i; i++) n = e[i], dt.tweeners[n] = dt.tweeners[n] || [], dt.tweeners[n].unshift(t)
            },
            prefilters: [function(e, t, n) {
                var i, r, o, a, s, l, c, u = this,
                    p = {},
                    h = e.style,
                    v = e.nodeType && J(e),
                    m = f._data(e, "fxshow");
                for (i in n.queue || (null == (s = f._queueHooks(e, "fx")).unqueued && (s.unqueued = 0, l = s.empty.fire, s.empty.fire = function() {
                        s.unqueued || l()
                    }), s.unqueued++, u.always(function() {
                        u.always(function() {
                            s.unqueued--, f.queue(e, "fx").length || s.empty.fire()
                        })
                    })), 1 === e.nodeType && ("height" in t || "width" in t) && (n.overflow = [h.overflow, h.overflowX, h.overflowY], "inline" === ("none" === (c = f.css(e, "display")) ? f._data(e, "olddisplay") || He(e.nodeName) : c) && "none" === f.css(e, "float") && (d.inlineBlockNeedsLayout && "inline" !== He(e.nodeName) ? h.zoom = 1 : h.display = "inline-block")), n.overflow && (h.overflow = "hidden", d.shrinkWrapBlocks() || u.always(function() {
                        h.overflow = n.overflow[0], h.overflowX = n.overflow[1], h.overflowY = n.overflow[2]
                    })), t)
                    if (r = t[i], at.exec(r)) {
                        if (delete t[i], o = o || "toggle" === r, r === (v ? "hide" : "show")) {
                            if ("show" !== r || !m || void 0 === m[i]) continue;
                            v = !0
                        }
                        p[i] = m && m[i] || f.style(e, i)
                    } else c = void 0;
                if (f.isEmptyObject(p)) "inline" === ("none" === c ? He(e.nodeName) : c) && (h.display = c);
                else
                    for (i in m ? "hidden" in m && (v = m.hidden) : m = f._data(e, "fxshow", {}), o && (m.hidden = !v), v ? f(e).show() : u.done(function() {
                            f(e).hide()
                        }), u.done(function() {
                            var t;
                            for (t in f._removeData(e, "fxshow"), p) f.style(e, t, p[t])
                        }), p) a = ut(v ? m[i] : 0, i, u), i in m || (m[i] = a.start, v && (a.end = a.start, a.start = "width" === i || "height" === i ? 1 : 0))
            }],
            prefilter: function(e, t) {
                t ? dt.prefilters.unshift(e) : dt.prefilters.push(e)
            }
        }), f.speed = function(e, t, n) {
            var i = e && "object" == typeof e ? f.extend({}, e) : {
                complete: n || !n && t || f.isFunction(e) && e,
                duration: e,
                easing: n && t || t && !f.isFunction(t) && t
            };
            return i.duration = f.fx.off ? 0 : "number" == typeof i.duration ? i.duration : i.duration in f.fx.speeds ? f.fx.speeds[i.duration] : f.fx.speeds._default, null != i.queue && !0 !== i.queue || (i.queue = "fx"), i.old = i.complete, i.complete = function() {
                f.isFunction(i.old) && i.old.call(this), i.queue && f.dequeue(this, i.queue)
            }, i
        }, f.fn.extend({
            fadeTo: function(e, t, n, i) {
                return this.filter(J).css("opacity", 0).show().end().animate({
                    opacity: t
                }, e, n, i)
            },
            animate: function(e, t, n, i) {
                var r = f.isEmptyObject(e),
                    o = f.speed(t, n, i),
                    a = function() {
                        var t = dt(this, f.extend({}, e), o);
                        (r || f._data(this, "finish")) && t.stop(!0)
                    };
                return a.finish = a, r || !1 === o.queue ? this.each(a) : this.queue(o.queue, a)
            },
            stop: function(e, t, n) {
                var i = function(e) {
                    var t = e.stop;
                    delete e.stop, t(n)
                };
                return "string" != typeof e && (n = t, t = e, e = void 0), t && !1 !== e && this.queue(e || "fx", []), this.each(function() {
                    var t = !0,
                        r = null != e && e + "queueHooks",
                        o = f.timers,
                        a = f._data(this);
                    if (r) a[r] && a[r].stop && i(a[r]);
                    else
                        for (r in a) a[r] && a[r].stop && st.test(r) && i(a[r]);
                    for (r = o.length; r--;) o[r].elem !== this || null != e && o[r].queue !== e || (o[r].anim.stop(n), t = !1, o.splice(r, 1));
                    !t && n || f.dequeue(this, e)
                })
            },
            finish: function(e) {
                return !1 !== e && (e = e || "fx"), this.each(function() {
                    var t, n = f._data(this),
                        i = n[e + "queue"],
                        r = n[e + "queueHooks"],
                        o = f.timers,
                        a = i ? i.length : 0;
                    for (n.finish = !0, f.queue(this, e, []), r && r.stop && r.stop.call(this, !0), t = o.length; t--;) o[t].elem === this && o[t].queue === e && (o[t].anim.stop(!0), o.splice(t, 1));
                    for (t = 0; a > t; t++) i[t] && i[t].finish && i[t].finish.call(this);
                    delete n.finish
                })
            }
        }), f.each(["toggle", "show", "hide"], function(e, t) {
            var n = f.fn[t];
            f.fn[t] = function(e, i, r) {
                return null == e || "boolean" == typeof e ? n.apply(this, arguments) : this.animate(ct(t, !0), e, i, r)
            }
        }), f.each({
            slideDown: ct("show"),
            slideUp: ct("hide"),
            slideToggle: ct("toggle"),
            fadeIn: {
                opacity: "show"
            },
            fadeOut: {
                opacity: "hide"
            },
            fadeToggle: {
                opacity: "toggle"
            }
        }, function(e, t) {
            f.fn[e] = function(e, n, i) {
                return this.animate(t, e, n, i)
            }
        }), f.timers = [], f.fx.tick = function() {
            var e, t = f.timers,
                n = 0;
            for (rt = f.now(); n < t.length; n++)(e = t[n])() || t[n] !== e || t.splice(n--, 1);
            t.length || f.fx.stop(), rt = void 0
        }, f.fx.timer = function(e) {
            f.timers.push(e), e() ? f.fx.start() : f.timers.pop()
        }, f.fx.interval = 13, f.fx.start = function() {
            ot || (ot = e.setInterval(f.fx.tick, f.fx.interval))
        }, f.fx.stop = function() {
            e.clearInterval(ot), ot = null
        }, f.fx.speeds = {
            slow: 600,
            fast: 200,
            _default: 400
        }, f.fn.delay = function(t, n) {
            return t = f.fx && f.fx.speeds[t] || t, n = n || "fx", this.queue(n, function(n, i) {
                var r = e.setTimeout(n, t);
                i.stop = function() {
                    e.clearTimeout(r)
                }
            })
        },
        function() {
            var e, t = i.createElement("input"),
                n = i.createElement("div"),
                r = i.createElement("select"),
                o = r.appendChild(i.createElement("option"));
            (n = i.createElement("div")).setAttribute("className", "t"), n.innerHTML = "  <link/><table></table><a href='/a'>a</a><input type='checkbox'/>", e = n.getElementsByTagName("a")[0], t.setAttribute("type", "checkbox"), n.appendChild(t), (e = n.getElementsByTagName("a")[0]).style.cssText = "top:1px", d.getSetAttribute = "t" !== n.className, d.style = /top/.test(e.getAttribute("style")), d.hrefNormalized = "/a" === e.getAttribute("href"), d.checkOn = !!t.value, d.optSelected = o.selected, d.enctype = !!i.createElement("form").enctype, r.disabled = !0, d.optDisabled = !o.disabled, (t = i.createElement("input")).setAttribute("value", ""), d.input = "" === t.getAttribute("value"), t.value = "t", t.setAttribute("type", "radio"), d.radioValue = "t" === t.value
        }();
    var pt = /\r/g,
        ft = /[\x20\t\r\n\f]+/g;
    f.fn.extend({
        val: function(e) {
            var t, n, i, r = this[0];
            return arguments.length ? (i = f.isFunction(e), this.each(function(n) {
                var r;
                1 === this.nodeType && (null == (r = i ? e.call(this, n, f(this).val()) : e) ? r = "" : "number" == typeof r ? r += "" : f.isArray(r) && (r = f.map(r, function(e) {
                    return null == e ? "" : e + ""
                })), (t = f.valHooks[this.type] || f.valHooks[this.nodeName.toLowerCase()]) && "set" in t && void 0 !== t.set(this, r, "value") || (this.value = r))
            })) : r ? (t = f.valHooks[r.type] || f.valHooks[r.nodeName.toLowerCase()]) && "get" in t && void 0 !== (n = t.get(r, "value")) ? n : "string" == typeof(n = r.value) ? n.replace(pt, "") : null == n ? "" : n : void 0
        }
    }), f.extend({
        valHooks: {
            option: {
                get: function(e) {
                    var t = f.find.attr(e, "value");
                    return null != t ? t : f.trim(f.text(e)).replace(ft, " ")
                }
            },
            select: {
                get: function(e) {
                    for (var t, n, i = e.options, r = e.selectedIndex, o = "select-one" === e.type || 0 > r, a = o ? null : [], s = o ? r + 1 : i.length, l = 0 > r ? s : o ? r : 0; s > l; l++)
                        if (((n = i[l]).selected || l === r) && (d.optDisabled ? !n.disabled : null === n.getAttribute("disabled")) && (!n.parentNode.disabled || !f.nodeName(n.parentNode, "optgroup"))) {
                            if (t = f(n).val(), o) return t;
                            a.push(t)
                        } return a
                },
                set: function(e, t) {
                    for (var n, i, r = e.options, o = f.makeArray(t), a = r.length; a--;)
                        if (i = r[a], f.inArray(f.valHooks.option.get(i), o) > -1) try {
                            i.selected = n = !0
                        } catch (e) {
                            i.scrollHeight
                        } else i.selected = !1;
                    return n || (e.selectedIndex = -1), r
                }
            }
        }
    }), f.each(["radio", "checkbox"], function() {
        f.valHooks[this] = {
            set: function(e, t) {
                return f.isArray(t) ? e.checked = f.inArray(f(e).val(), t) > -1 : void 0
            }
        }, d.checkOn || (f.valHooks[this].get = function(e) {
            return null === e.getAttribute("value") ? "on" : e.value
        })
    });
    var ht, vt, mt = f.expr.attrHandle,
        yt = /^(?:checked|selected)$/i,
        gt = d.getSetAttribute,
        bt = d.input;
    f.fn.extend({
        attr: function(e, t) {
            return V(this, f.attr, e, t, arguments.length > 1)
        },
        removeAttr: function(e) {
            return this.each(function() {
                f.removeAttr(this, e)
            })
        }
    }), f.extend({
        attr: function(e, t, n) {
            var i, r, o = e.nodeType;
            if (3 !== o && 8 !== o && 2 !== o) return void 0 === e.getAttribute ? f.prop(e, t, n) : (1 === o && f.isXMLDoc(e) || (t = t.toLowerCase(), r = f.attrHooks[t] || (f.expr.match.bool.test(t) ? vt : ht)), void 0 !== n ? null === n ? void f.removeAttr(e, t) : r && "set" in r && void 0 !== (i = r.set(e, n, t)) ? i : (e.setAttribute(t, n + ""), n) : r && "get" in r && null !== (i = r.get(e, t)) ? i : null == (i = f.find.attr(e, t)) ? void 0 : i)
        },
        attrHooks: {
            type: {
                set: function(e, t) {
                    if (!d.radioValue && "radio" === t && f.nodeName(e, "input")) {
                        var n = e.value;
                        return e.setAttribute("type", t), n && (e.value = n), t
                    }
                }
            }
        },
        removeAttr: function(e, t) {
            var n, i, r = 0,
                o = t && t.match(q);
            if (o && 1 === e.nodeType)
                for (; n = o[r++];) i = f.propFix[n] || n, f.expr.match.bool.test(n) ? bt && gt || !yt.test(n) ? e[i] = !1 : e[f.camelCase("default-" + n)] = e[i] = !1 : f.attr(e, n, ""), e.removeAttribute(gt ? n : i)
        }
    }), vt = {
        set: function(e, t, n) {
            return !1 === t ? f.removeAttr(e, n) : bt && gt || !yt.test(n) ? e.setAttribute(!gt && f.propFix[n] || n, n) : e[f.camelCase("default-" + n)] = e[n] = !0, n
        }
    }, f.each(f.expr.match.bool.source.match(/\w+/g), function(e, t) {
        var n = mt[t] || f.find.attr;
        bt && gt || !yt.test(t) ? mt[t] = function(e, t, i) {
            var r, o;
            return i || (o = mt[t], mt[t] = r, r = null != n(e, t, i) ? t.toLowerCase() : null, mt[t] = o), r
        } : mt[t] = function(e, t, n) {
            return n ? void 0 : e[f.camelCase("default-" + t)] ? t.toLowerCase() : null
        }
    }), bt && gt || (f.attrHooks.value = {
        set: function(e, t, n) {
            return f.nodeName(e, "input") ? void(e.defaultValue = t) : ht && ht.set(e, t, n)
        }
    }), gt || (ht = {
        set: function(e, t, n) {
            var i = e.getAttributeNode(n);
            return i || e.setAttributeNode(i = e.ownerDocument.createAttribute(n)), i.value = t += "", "value" === n || t === e.getAttribute(n) ? t : void 0
        }
    }, mt.id = mt.name = mt.coords = function(e, t, n) {
        var i;
        return n ? void 0 : (i = e.getAttributeNode(t)) && "" !== i.value ? i.value : null
    }, f.valHooks.button = {
        get: function(e, t) {
            var n = e.getAttributeNode(t);
            return n && n.specified ? n.value : void 0
        },
        set: ht.set
    }, f.attrHooks.contenteditable = {
        set: function(e, t, n) {
            ht.set(e, "" !== t && t, n)
        }
    }, f.each(["width", "height"], function(e, t) {
        f.attrHooks[t] = {
            set: function(e, n) {
                return "" === n ? (e.setAttribute(t, "auto"), n) : void 0
            }
        }
    })), d.style || (f.attrHooks.style = {
        get: function(e) {
            return e.style.cssText || void 0
        },
        set: function(e, t) {
            return e.style.cssText = t + ""
        }
    });
    var xt = /^(?:input|select|textarea|button|object)$/i,
        wt = /^(?:a|area)$/i;
    f.fn.extend({
        prop: function(e, t) {
            return V(this, f.prop, e, t, arguments.length > 1)
        },
        removeProp: function(e) {
            return e = f.propFix[e] || e, this.each(function() {
                try {
                    this[e] = void 0, delete this[e]
                } catch (e) {}
            })
        }
    }), f.extend({
        prop: function(e, t, n) {
            var i, r, o = e.nodeType;
            if (3 !== o && 8 !== o && 2 !== o) return 1 === o && f.isXMLDoc(e) || (t = f.propFix[t] || t, r = f.propHooks[t]), void 0 !== n ? r && "set" in r && void 0 !== (i = r.set(e, n, t)) ? i : e[t] = n : r && "get" in r && null !== (i = r.get(e, t)) ? i : e[t]
        },
        propHooks: {
            tabIndex: {
                get: function(e) {
                    var t = f.find.attr(e, "tabindex");
                    return t ? parseInt(t, 10) : xt.test(e.nodeName) || wt.test(e.nodeName) && e.href ? 0 : -1
                }
            }
        },
        propFix: {
            for: "htmlFor",
            class: "className"
        }
    }), d.hrefNormalized || f.each(["href", "src"], function(e, t) {
        f.propHooks[t] = {
            get: function(e) {
                return e.getAttribute(t, 4)
            }
        }
    }), d.optSelected || (f.propHooks.selected = {
        get: function(e) {
            var t = e.parentNode;
            return t && (t.selectedIndex, t.parentNode && t.parentNode.selectedIndex), null
        },
        set: function(e) {
            var t = e.parentNode;
            t && (t.selectedIndex, t.parentNode && t.parentNode.selectedIndex)
        }
    }), f.each(["tabIndex", "readOnly", "maxLength", "cellSpacing", "cellPadding", "rowSpan", "colSpan", "useMap", "frameBorder", "contentEditable"], function() {
        f.propFix[this.toLowerCase()] = this
    }), d.enctype || (f.propFix.enctype = "encoding");
    var kt = /[\t\r\n\f]/g;

    function _t(e) {
        return f.attr(e, "class") || ""
    }
    f.fn.extend({
        addClass: function(e) {
            var t, n, i, r, o, a, s, l = 0;
            if (f.isFunction(e)) return this.each(function(t) {
                f(this).addClass(e.call(this, t, _t(this)))
            });
            if ("string" == typeof e && e)
                for (t = e.match(q) || []; n = this[l++];)
                    if (r = _t(n), i = 1 === n.nodeType && (" " + r + " ").replace(kt, " ")) {
                        for (a = 0; o = t[a++];) i.indexOf(" " + o + " ") < 0 && (i += o + " ");
                        r !== (s = f.trim(i)) && f.attr(n, "class", s)
                    } return this
        },
        removeClass: function(e) {
            var t, n, i, r, o, a, s, l = 0;
            if (f.isFunction(e)) return this.each(function(t) {
                f(this).removeClass(e.call(this, t, _t(this)))
            });
            if (!arguments.length) return this.attr("class", "");
            if ("string" == typeof e && e)
                for (t = e.match(q) || []; n = this[l++];)
                    if (r = _t(n), i = 1 === n.nodeType && (" " + r + " ").replace(kt, " ")) {
                        for (a = 0; o = t[a++];)
                            for (; i.indexOf(" " + o + " ") > -1;) i = i.replace(" " + o + " ", " ");
                        r !== (s = f.trim(i)) && f.attr(n, "class", s)
                    } return this
        },
        toggleClass: function(e, t) {
            var n = typeof e;
            return "boolean" == typeof t && "string" === n ? t ? this.addClass(e) : this.removeClass(e) : f.isFunction(e) ? this.each(function(n) {
                f(this).toggleClass(e.call(this, n, _t(this), t), t)
            }) : this.each(function() {
                var t, i, r, o;
                if ("string" === n)
                    for (i = 0, r = f(this), o = e.match(q) || []; t = o[i++];) r.hasClass(t) ? r.removeClass(t) : r.addClass(t);
                else void 0 !== e && "boolean" !== n || ((t = _t(this)) && f._data(this, "__className__", t), f.attr(this, "class", t || !1 === e ? "" : f._data(this, "__className__") || ""))
            })
        },
        hasClass: function(e) {
            var t, n, i = 0;
            for (t = " " + e + " "; n = this[i++];)
                if (1 === n.nodeType && (" " + _t(n) + " ").replace(kt, " ").indexOf(t) > -1) return !0;
            return !1
        }
    }), f.each("blur focus focusin focusout load resize scroll unload click dblclick mousedown mouseup mousemove mouseover mouseout mouseenter mouseleave change select submit keydown keypress keyup error contextmenu".split(" "), function(e, t) {
        f.fn[t] = function(e, n) {
            return arguments.length > 0 ? this.on(t, null, e, n) : this.trigger(t)
        }
    }), f.fn.extend({
        hover: function(e, t) {
            return this.mouseenter(e).mouseleave(t || e)
        }
    });
    var Tt = e.location,
        Ct = f.now(),
        Et = /\?/,
        St = /(,)|(\[|{)|(}|])|"(?:[^"\\\r\n]|\\["\\\/bfnrt]|\\u[\da-fA-F]{4})*"\s*:?|true|false|null|-?(?!0\d)\d+(?:\.\d+|)(?:[eE][+-]?\d+|)/g;
    f.parseJSON = function(t) {
        if (e.JSON && e.JSON.parse) return e.JSON.parse(t + "");
        var n, i = null,
            r = f.trim(t + "");
        return r && !f.trim(r.replace(St, function(e, t, r, o) {
            return n && t && (i = 0), 0 === i ? e : (n = r || t, i += !o - !r, "")
        })) ? Function("return " + r)() : f.error("Invalid JSON: " + t)
    }, f.parseXML = function(t) {
        var n;
        if (!t || "string" != typeof t) return null;
        try {
            e.DOMParser ? n = (new e.DOMParser).parseFromString(t, "text/xml") : ((n = new e.ActiveXObject("Microsoft.XMLDOM")).async = "false", n.loadXML(t))
        } catch (e) {
            n = void 0
        }
        return n && n.documentElement && !n.getElementsByTagName("parsererror").length || f.error("Invalid XML: " + t), n
    };
    var At = /#.*$/,
        Nt = /([?&])_=[^&]*/,
        jt = /^(.*?):[ \t]*([^\r\n]*)\r?$/gm,
        Dt = /^(?:GET|HEAD)$/,
        Lt = /^\/\//,
        qt = /^([\w.+-]+:)(?:\/\/(?:[^\/?#]*@|)([^\/?#:]*)(?::(\d+)|)|)/,
        Mt = {},
        Ht = {},
        Ft = "*/".concat("*"),
        Pt = Tt.href,
        Ot = qt.exec(Pt.toLowerCase()) || [];

    function zt(e) {
        return function(t, n) {
            "string" != typeof t && (n = t, t = "*");
            var i, r = 0,
                o = t.toLowerCase().match(q) || [];
            if (f.isFunction(n))
                for (; i = o[r++];) "+" === i.charAt(0) ? (i = i.slice(1) || "*", (e[i] = e[i] || []).unshift(n)) : (e[i] = e[i] || []).push(n)
        }
    }

    function Rt(e, t, n, i) {
        var r = {},
            o = e === Ht;

        function a(s) {
            var l;
            return r[s] = !0, f.each(e[s] || [], function(e, s) {
                var c = s(t, n, i);
                return "string" != typeof c || o || r[c] ? o ? !(l = c) : void 0 : (t.dataTypes.unshift(c), a(c), !1)
            }), l
        }
        return a(t.dataTypes[0]) || !r["*"] && a("*")
    }

    function It(e, t) {
        var n, i, r = f.ajaxSettings.flatOptions || {};
        for (i in t) void 0 !== t[i] && ((r[i] ? e : n || (n = {}))[i] = t[i]);
        return n && f.extend(!0, e, n), e
    }

    function Wt(e) {
        return e.style && e.style.display || f.css(e, "display")
    }
    f.extend({
        active: 0,
        lastModified: {},
        etag: {},
        ajaxSettings: {
            url: Pt,
            type: "GET",
            isLocal: /^(?:about|app|app-storage|.+-extension|file|res|widget):$/.test(Ot[1]),
            global: !0,
            processData: !0,
            async: !0,
            contentType: "application/x-www-form-urlencoded; charset=UTF-8",
            accepts: {
                "*": Ft,
                text: "text/plain",
                html: "text/html",
                xml: "application/xml, text/xml",
                json: "application/json, text/javascript"
            },
            contents: {
                xml: /\bxml\b/,
                html: /\bhtml/,
                json: /\bjson\b/
            },
            responseFields: {
                xml: "responseXML",
                text: "responseText",
                json: "responseJSON"
            },
            converters: {
                "* text": String,
                "text html": !0,
                "text json": f.parseJSON,
                "text xml": f.parseXML
            },
            flatOptions: {
                url: !0,
                context: !0
            }
        },
        ajaxSetup: function(e, t) {
            return t ? It(It(e, f.ajaxSettings), t) : It(f.ajaxSettings, e)
        },
        ajaxPrefilter: zt(Mt),
        ajaxTransport: zt(Ht),
        ajax: function(t, n) {
            "object" == typeof t && (n = t, t = void 0), n = n || {};
            var i, r, o, a, s, l, c, u, d = f.ajaxSetup({}, n),
                p = d.context || d,
                h = d.context && (p.nodeType || p.jquery) ? f(p) : f.event,
                v = f.Deferred(),
                m = f.Callbacks("once memory"),
                y = d.statusCode || {},
                g = {},
                b = {},
                x = 0,
                w = "canceled",
                k = {
                    readyState: 0,
                    getResponseHeader: function(e) {
                        var t;
                        if (2 === x) {
                            if (!u)
                                for (u = {}; t = jt.exec(a);) u[t[1].toLowerCase()] = t[2];
                            t = u[e.toLowerCase()]
                        }
                        return null == t ? null : t
                    },
                    getAllResponseHeaders: function() {
                        return 2 === x ? a : null
                    },
                    setRequestHeader: function(e, t) {
                        var n = e.toLowerCase();
                        return x || (e = b[n] = b[n] || e, g[e] = t), this
                    },
                    overrideMimeType: function(e) {
                        return x || (d.mimeType = e), this
                    },
                    statusCode: function(e) {
                        var t;
                        if (e)
                            if (2 > x)
                                for (t in e) y[t] = [y[t], e[t]];
                            else k.always(e[k.status]);
                        return this
                    },
                    abort: function(e) {
                        var t = e || w;
                        return c && c.abort(t), _(0, t), this
                    }
                };
            if (v.promise(k).complete = m.add, k.success = k.done, k.error = k.fail, d.url = ((t || d.url || Pt) + "").replace(At, "").replace(Lt, Ot[1] + "//"), d.type = n.method || n.type || d.method || d.type, d.dataTypes = f.trim(d.dataType || "*").toLowerCase().match(q) || [""], null == d.crossDomain && (i = qt.exec(d.url.toLowerCase()), d.crossDomain = !(!i || i[1] === Ot[1] && i[2] === Ot[2] && (i[3] || ("http:" === i[1] ? "80" : "443")) === (Ot[3] || ("http:" === Ot[1] ? "80" : "443")))), d.data && d.processData && "string" != typeof d.data && (d.data = f.param(d.data, d.traditional)), Rt(Mt, d, n, k), 2 === x) return k;
            for (r in (l = f.event && d.global) && 0 == f.active++ && f.event.trigger("ajaxStart"), d.type = d.type.toUpperCase(), d.hasContent = !Dt.test(d.type), o = d.url, d.hasContent || (d.data && (o = d.url += (Et.test(o) ? "&" : "?") + d.data, delete d.data), !1 === d.cache && (d.url = Nt.test(o) ? o.replace(Nt, "$1_=" + Ct++) : o + (Et.test(o) ? "&" : "?") + "_=" + Ct++)), d.ifModified && (f.lastModified[o] && k.setRequestHeader("If-Modified-Since", f.lastModified[o]), f.etag[o] && k.setRequestHeader("If-None-Match", f.etag[o])), (d.data && d.hasContent && !1 !== d.contentType || n.contentType) && k.setRequestHeader("Content-Type", d.contentType), k.setRequestHeader("Accept", d.dataTypes[0] && d.accepts[d.dataTypes[0]] ? d.accepts[d.dataTypes[0]] + ("*" !== d.dataTypes[0] ? ", " + Ft + "; q=0.01" : "") : d.accepts["*"]), d.headers) k.setRequestHeader(r, d.headers[r]);
            if (d.beforeSend && (!1 === d.beforeSend.call(p, k, d) || 2 === x)) return k.abort();
            for (r in w = "abort", {
                    success: 1,
                    error: 1,
                    complete: 1
                }) k[r](d[r]);
            if (c = Rt(Ht, d, n, k)) {
                if (k.readyState = 1, l && h.trigger("ajaxSend", [k, d]), 2 === x) return k;
                d.async && d.timeout > 0 && (s = e.setTimeout(function() {
                    k.abort("timeout")
                }, d.timeout));
                try {
                    x = 1, c.send(g, _)
                } catch (e) {
                    if (!(2 > x)) throw e;
                    _(-1, e)
                }
            } else _(-1, "No Transport");

            function _(t, n, i, r) {
                var u, g, b, w, _, T = n;
                2 !== x && (x = 2, s && e.clearTimeout(s), c = void 0, a = r || "", k.readyState = t > 0 ? 4 : 0, u = t >= 200 && 300 > t || 304 === t, i && (w = function(e, t, n) {
                    for (var i, r, o, a, s = e.contents, l = e.dataTypes;
                        "*" === l[0];) l.shift(), void 0 === r && (r = e.mimeType || t.getResponseHeader("Content-Type"));
                    if (r)
                        for (a in s)
                            if (s[a] && s[a].test(r)) {
                                l.unshift(a);
                                break
                            } if (l[0] in n) o = l[0];
                    else {
                        for (a in n) {
                            if (!l[0] || e.converters[a + " " + l[0]]) {
                                o = a;
                                break
                            }
                            i || (i = a)
                        }
                        o = o || i
                    }
                    return o ? (o !== l[0] && l.unshift(o), n[o]) : void 0
                }(d, k, i)), w = function(e, t, n, i) {
                    var r, o, a, s, l, c = {},
                        u = e.dataTypes.slice();
                    if (u[1])
                        for (a in e.converters) c[a.toLowerCase()] = e.converters[a];
                    for (o = u.shift(); o;)
                        if (e.responseFields[o] && (n[e.responseFields[o]] = t), !l && i && e.dataFilter && (t = e.dataFilter(t, e.dataType)), l = o, o = u.shift())
                            if ("*" === o) o = l;
                            else if ("*" !== l && l !== o) {
                        if (!(a = c[l + " " + o] || c["* " + o]))
                            for (r in c)
                                if ((s = r.split(" "))[1] === o && (a = c[l + " " + s[0]] || c["* " + s[0]])) {
                                    !0 === a ? a = c[r] : !0 !== c[r] && (o = s[0], u.unshift(s[1]));
                                    break
                                } if (!0 !== a)
                            if (a && e.throws) t = a(t);
                            else try {
                                t = a(t)
                            } catch (e) {
                                return {
                                    state: "parsererror",
                                    error: a ? e : "No conversion from " + l + " to " + o
                                }
                            }
                    }
                    return {
                        state: "success",
                        data: t
                    }
                }(d, w, k, u), u ? (d.ifModified && ((_ = k.getResponseHeader("Launhittable-Modified")) && (f.lastModified[o] = _), (_ = k.getResponseHeader("etag")) && (f.etag[o] = _)), 204 === t || "HEAD" === d.type ? T = "nocontent" : 304 === t ? T = "notmodified" : (T = w.state, g = w.data, u = !(b = w.error))) : (b = T, !t && T || (T = "error", 0 > t && (t = 0))), k.status = t, k.statusText = (n || T) + "", u ? v.resolveWith(p, [g, T, k]) : v.rejectWith(p, [k, T, b]), k.statusCode(y), y = void 0, l && h.trigger(u ? "ajaxSuccess" : "ajaxError", [k, d, u ? g : b]), m.fireWith(p, [k, T]), l && (h.trigger("ajaxComplete", [k, d]), --f.active || f.event.trigger("ajaxStop")))
            }
            return k
        },
        getJSON: function(e, t, n) {
            return f.get(e, t, n, "json")
        },
        getScript: function(e, t) {
            return f.get(e, void 0, t, "script")
        }
    }), f.each(["get", "post"], function(e, t) {
        f[t] = function(e, n, i, r) {
            return f.isFunction(n) && (r = r || i, i = n, n = void 0), f.ajax(f.extend({
                url: e,
                type: t,
                dataType: r,
                data: n,
                success: i
            }, f.isPlainObject(e) && e))
        }
    }), f._evalUrl = function(e) {
        return f.ajax({
            url: e,
            type: "GET",
            dataType: "script",
            cache: !0,
            async: !1,
            global: !1,
            throws: !0
        })
    }, f.fn.extend({
        wrapAll: function(e) {
            if (f.isFunction(e)) return this.each(function(t) {
                f(this).wrapAll(e.call(this, t))
            });
            if (this[0]) {
                var t = f(e, this[0].ownerDocument).eq(0).clone(!0);
                this[0].parentNode && t.insertBefore(this[0]), t.map(function() {
                    for (var e = this; e.firstChild && 1 === e.firstChild.nodeType;) e = e.firstChild;
                    return e
                }).append(this)
            }
            return this
        },
        wrapInner: function(e) {
            return f.isFunction(e) ? this.each(function(t) {
                f(this).wrapInner(e.call(this, t))
            }) : this.each(function() {
                var t = f(this),
                    n = t.contents();
                n.length ? n.wrapAll(e) : t.append(e)
            })
        },
        wrap: function(e) {
            var t = f.isFunction(e);
            return this.each(function(n) {
                f(this).wrapAll(t ? e.call(this, n) : e)
            })
        },
        unwrap: function() {
            return this.parent().each(function() {
                f.nodeName(this, "body") || f(this).replaceWith(this.childNodes)
            }).end()
        }
    }), f.expr.filters.hidden = function(e) {
        return d.reliableHiddenOffsets() ? e.offsetWidth <= 0 && e.offsetHeight <= 0 && !e.getClientRects().length : function(e) {
            if (!f.contains(e.ownerDocument || i, e)) return !0;
            for (; e && 1 === e.nodeType;) {
                if ("none" === Wt(e) || "hidden" === e.type) return !0;
                e = e.parentNode
            }
            return !1
        }(e)
    }, f.expr.filters.visible = function(e) {
        return !f.expr.filters.hidden(e)
    };
    var Bt = /%20/g,
        $t = /\[\]$/,
        Xt = /\r?\n/g,
        Jt = /^(?:submit|button|image|reset|file)$/i,
        Ut = /^(?:input|select|textarea|keygen)/i;

    function Vt(e, t, n, i) {
        var r;
        if (f.isArray(t)) f.each(t, function(t, r) {
            n || $t.test(e) ? i(e, r) : Vt(e + "[" + ("object" == typeof r && null != r ? t : "") + "]", r, n, i)
        });
        else if (n || "object" !== f.type(t)) i(e, t);
        else
            for (r in t) Vt(e + "[" + r + "]", t[r], n, i)
    }
    f.param = function(e, t) {
        var n, i = [],
            r = function(e, t) {
                t = f.isFunction(t) ? t() : null == t ? "" : t, i[i.length] = encodeURIComponent(e) + "=" + encodeURIComponent(t)
            };
        if (void 0 === t && (t = f.ajaxSettings && f.ajaxSettings.traditional), f.isArray(e) || e.jquery && !f.isPlainObject(e)) f.each(e, function() {
            r(this.name, this.value)
        });
        else
            for (n in e) Vt(n, e[n], t, r);
        return i.join("&").replace(Bt, "+")
    }, f.fn.extend({
        serialize: function() {
            return f.param(this.serializeArray())
        },
        serializeArray: function() {
            return this.map(function() {
                var e = f.prop(this, "elements");
                return e ? f.makeArray(e) : this
            }).filter(function() {
                var e = this.type;
                return this.name && !f(this).is(":disabled") && Ut.test(this.nodeName) && !Jt.test(e) && (this.checked || !Y.test(e))
            }).map(function(e, t) {
                var n = f(this).val();
                return null == n ? null : f.isArray(n) ? f.map(n, function(e) {
                    return {
                        name: t.name,
                        value: e.replace(Xt, "\r\n")
                    }
                }) : {
                    name: t.name,
                    value: n.replace(Xt, "\r\n")
                }
            }).get()
        }
    }), f.ajaxSettings.xhr = void 0 !== e.ActiveXObject ? function() {
        return this.isLocal ? Zt() : i.documentMode > 8 ? Kt() : /^(get|post|head|put|delete|options)$/i.test(this.type) && Kt() || Zt()
    } : Kt;
    var Yt = 0,
        Gt = {},
        Qt = f.ajaxSettings.xhr();

    function Kt() {
        try {
            return new e.XMLHttpRequest
        } catch (e) {}
    }

    function Zt() {
        try {
            return new e.ActiveXObject("Microsoft.XMLHTTP")
        } catch (e) {}
    }
    e.attachEvent && e.attachEvent("onunload", function() {
        for (var e in Gt) Gt[e](void 0, !0)
    }), d.cors = !!Qt && "withCredentials" in Qt, (Qt = d.ajax = !!Qt) && f.ajaxTransport(function(t) {
        var n;
        if (!t.crossDomain || d.cors) return {
            send: function(i, r) {
                var o, a = t.xhr(),
                    s = ++Yt;
                if (a.open(t.type, t.url, t.async, t.username, t.password), t.xhrFields)
                    for (o in t.xhrFields) a[o] = t.xhrFields[o];
                for (o in t.mimeType && a.overrideMimeType && a.overrideMimeType(t.mimeType), t.crossDomain || i["X-Requested-With"] || (i["X-Requested-With"] = "XMLHttpRequest"), i) void 0 !== i[o] && a.setRequestHeader(o, i[o] + "");
                a.send(t.hasContent && t.data || null), n = function(e, i) {
                    var o, l, c;
                    if (n && (i || 4 === a.readyState))
                        if (delete Gt[s], n = void 0, a.onreadystatechange = f.noop, i) 4 !== a.readyState && a.abort();
                        else {
                            c = {}, o = a.status, "string" == typeof a.responseText && (c.text = a.responseText);
                            try {
                                l = a.statusText
                            } catch (e) {
                                l = ""
                            }
                            o || !t.isLocal || t.crossDomain ? 1223 === o && (o = 204) : o = c.text ? 200 : 404
                        } c && r(o, l, c, a.getAllResponseHeaders())
                }, t.async ? 4 === a.readyState ? e.setTimeout(n) : a.onreadystatechange = Gt[s] = n : n()
            },
            abort: function() {
                n && n(void 0, !0)
            }
        }
    }), f.ajaxSetup({
        accepts: {
            script: "text/javascript, application/javascript, application/ecmascript, application/x-ecmascript"
        },
        contents: {
            script: /\b(?:java|ecma)script\b/
        },
        converters: {
            "text script": function(e) {
                return f.globalEval(e), e
            }
        }
    }), f.ajaxPrefilter("script", function(e) {
        void 0 === e.cache && (e.cache = !1), e.crossDomain && (e.type = "GET", e.global = !1)
    }), f.ajaxTransport("script", function(e) {
        if (e.crossDomain) {
            var t, n = i.head || f("head")[0] || i.documentElement;
            return {
                send: function(r, o) {
                    (t = i.createElement("script")).async = !0, e.scriptCharset && (t.charset = e.scriptCharset), t.src = e.url, t.onload = t.onreadystatechange = function(e, n) {
                        (n || !t.readyState || /loaded|complete/.test(t.readyState)) && (t.onload = t.onreadystatechange = null, t.parentNode && t.parentNode.removeChild(t), t = null, n || o(200, "success"))
                    }, n.insertBefore(t, n.firstChild)
                },
                abort: function() {
                    t && t.onload(void 0, !0)
                }
            }
        }
    });
    var en = [],
        tn = /(=)\?(?=&|$)|\?\?/;
    f.ajaxSetup({
        jsonp: "callback",
        jsonpCallback: function() {
            var e = en.pop() || f.expando + "_" + Ct++;
            return this[e] = !0, e
        }
    }), f.ajaxPrefilter("json jsonp", function(t, n, i) {
        var r, o, a, s = !1 !== t.jsonp && (tn.test(t.url) ? "url" : "string" == typeof t.data && 0 === (t.contentType || "").indexOf("application/x-www-form-urlencoded") && tn.test(t.data) && "data");
        return s || "jsonp" === t.dataTypes[0] ? (r = t.jsonpCallback = f.isFunction(t.jsonpCallback) ? t.jsonpCallback() : t.jsonpCallback, s ? t[s] = t[s].replace(tn, "$1" + r) : !1 !== t.jsonp && (t.url += (Et.test(t.url) ? "&" : "?") + t.jsonp + "=" + r), t.converters["script json"] = function() {
            return a || f.error(r + " was not called"), a[0]
        }, t.dataTypes[0] = "json", o = e[r], e[r] = function() {
            a = arguments
        }, i.always(function() {
            void 0 === o ? f(e).removeProp(r) : e[r] = o, t[r] && (t.jsonpCallback = n.jsonpCallback, en.push(r)), a && f.isFunction(o) && o(a[0]), a = o = void 0
        }), "script") : void 0
    }), f.parseHTML = function(e, t, n) {
        if (!e || "string" != typeof e) return null;
        "boolean" == typeof t && (n = t, t = !1), t = t || i;
        var r = _.exec(e),
            o = !n && [];
        return r ? [t.createElement(r[1])] : (r = se([e], t, o), o && o.length && f(o).remove(), f.merge([], r.childNodes))
    };
    var nn = f.fn.load;

    function rn(e) {
        return f.isWindow(e) ? e : 9 === e.nodeType && (e.defaultView || e.parentWindow)
    }
    f.fn.load = function(e, t, n) {
        if ("string" != typeof e && nn) return nn.apply(this, arguments);
        var i, r, o, a = this,
            s = e.indexOf(" ");
        return s > -1 && (i = f.trim(e.slice(s, e.length)), e = e.slice(0, s)), f.isFunction(t) ? (n = t, t = void 0) : t && "object" == typeof t && (r = "POST"), a.length > 0 && f.ajax({
            url: e,
            type: r || "GET",
            dataType: "html",
            data: t
        }).done(function(e) {
            o = arguments, a.html(i ? f("<div>").append(f.parseHTML(e)).find(i) : e)
        }).always(n && function(e, t) {
            a.each(function() {
                n.apply(this, o || [e.responseText, t, e])
            })
        }), this
    }, f.each(["ajaxStart", "ajaxStop", "ajaxComplete", "ajaxError", "ajaxSuccess", "ajaxSend"], function(e, t) {
        f.fn[t] = function(e) {
            return this.on(t, e)
        }
    }), f.expr.filters.animated = function(e) {
        return f.grep(f.timers, function(t) {
            return e === t.elem
        }).length
    }, f.offset = {
        setOffset: function(e, t, n) {
            var i, r, o, a, s, l, c = f.css(e, "position"),
                u = f(e),
                d = {};
            "static" === c && (e.style.position = "relative"), s = u.offset(), o = f.css(e, "top"), l = f.css(e, "left"), ("absolute" === c || "fixed" === c) && f.inArray("auto", [o, l]) > -1 ? (a = (i = u.position()).top, r = i.left) : (a = parseFloat(o) || 0, r = parseFloat(l) || 0), f.isFunction(t) && (t = t.call(e, n, f.extend({}, s))), null != t.top && (d.top = t.top - s.top + a), null != t.left && (d.left = t.left - s.left + r), "using" in t ? t.using.call(e, d) : u.css(d)
        }
    }, f.fn.extend({
        offset: function(e) {
            if (arguments.length) return void 0 === e ? this : this.each(function(t) {
                f.offset.setOffset(this, e, t)
            });
            var t, n, i = {
                    top: 0,
                    left: 0
                },
                r = this[0],
                o = r && r.ownerDocument;
            return o ? (t = o.documentElement, f.contains(t, r) ? (void 0 !== r.getBoundingClientRect && (i = r.getBoundingClientRect()), n = rn(o), {
                top: i.top + (n.pageYOffset || t.scrollTop) - (t.clientTop || 0),
                left: i.left + (n.pageXOffset || t.scrollLeft) - (t.clientLeft || 0)
            }) : i) : void 0
        },
        position: function() {
            if (this[0]) {
                var e, t, n = {
                        top: 0,
                        left: 0
                    },
                    i = this[0];
                return "fixed" === f.css(i, "position") ? t = i.getBoundingClientRect() : (e = this.offsetParent(), t = this.offset(), f.nodeName(e[0], "html") || (n = e.offset()), n.top += f.css(e[0], "borderTopWidth", !0), n.left += f.css(e[0], "borderLeftWidth", !0)), {
                    top: t.top - n.top - f.css(i, "marginTop", !0),
                    left: t.left - n.left - f.css(i, "marginLeft", !0)
                }
            }
        },
        offsetParent: function() {
            return this.map(function() {
                for (var e = this.offsetParent; e && !f.nodeName(e, "html") && "static" === f.css(e, "position");) e = e.offsetParent;
                return e || ze
            })
        }
    }), f.each({
        scrollLeft: "pageXOffset",
        scrollTop: "pageYOffset"
    }, function(e, t) {
        var n = /Y/.test(t);
        f.fn[e] = function(i) {
            return V(this, function(e, i, r) {
                var o = rn(e);
                return void 0 === r ? o ? t in o ? o[t] : o.document.documentElement[i] : e[i] : void(o ? o.scrollTo(n ? f(o).scrollLeft() : r, n ? r : f(o).scrollTop()) : e[i] = r)
            }, e, i, arguments.length, null)
        }
    }), f.each(["top", "left"], function(e, t) {
        f.cssHooks[t] = Be(d.pixelPosition, function(e, n) {
            return n ? (n = Ie(e, t), Pe.test(n) ? f(e).position()[t] + "px" : n) : void 0
        })
    }), f.each({
        Height: "height",
        Width: "width"
    }, function(e, t) {
        f.each({
            padding: "inner" + e,
            content: t,
            "": "outer" + e
        }, function(n, i) {
            f.fn[i] = function(i, r) {
                var o = arguments.length && (n || "boolean" != typeof i),
                    a = n || (!0 === i || !0 === r ? "margin" : "border");
                return V(this, function(t, n, i) {
                    var r;
                    return f.isWindow(t) ? t.document.documentElement["client" + e] : 9 === t.nodeType ? (r = t.documentElement, Math.max(t.body["scroll" + e], r["scroll" + e], t.body["offset" + e], r["offset" + e], r["client" + e])) : void 0 === i ? f.css(t, n, a) : f.style(t, n, i, a)
                }, t, o ? i : void 0, o, null)
            }
        })
    }), f.fn.extend({
        bind: function(e, t, n) {
            return this.on(e, null, t, n)
        },
        unbind: function(e, t) {
            return this.off(e, null, t)
        },
        delegate: function(e, t, n, i) {
            return this.on(t, e, n, i)
        },
        undelegate: function(e, t, n) {
            return 1 === arguments.length ? this.off(e, "**") : this.off(t, e || "**", n)
        }
    }), f.fn.size = function() {
        return this.length
    }, f.fn.andSelf = f.fn.addBack, "function" == typeof define && define.amd && define("jquery", [], function() {
        return f
    });
    var on = e.jQuery,
        an = e.$;
    return f.noConflict = function(t) {
        return e.$ === f && (e.$ = an), t && e.jQuery === f && (e.jQuery = on), f
    }, t || (e.jQuery = e.$ = f), f
}),
function(e) {
    "use strict";

    function t() {
        e(window).scrollTop() >= 10 ? e(".unhittable-sticky-header").addClass("unhittable-sticky-active") : e(".unhittable-sticky-header").removeClass("unhittable-sticky-active")
    }

    function n() {
        e(".unhittable-parallax").each(function() {
            var t = e(document).scrollTop(),
                n = e(window).height(),
                i = e(this).offset().top;
            if (i + e(this).height() >= t && i <= t + n) {
                var r = t + n - i,
                    o = r / 5,
                    a = r / 10;
                e(this).find(".unhittable-to-left").css("transform", `translateX(-${a}px)`), e(this).find(".unhittable-to-right").css("transform", `translateX(${a}px)`), e(this).css("background-position", `center -${o}px`)
            }
        })
    }
    e.exists = function(t) {
        return e(t).length > 0
    }, e(window).on("load", function() {
        e(window).trigger("scroll"), e(window).trigger("resize"), e(".unhittable-perloader").fadeOut(), e("unhittable-perloader-in").delay(150).fadeOut("slow")
    }), e(document).on("ready", function() {
        e(window).trigger("resize"), e(".unhittable-dynamic-bg").each(function() {
                var t = e(this).attr("data-src");
                e(this).css({
                    "background-image": "url(" + t + ")"
                })
            }), e.exists("#contact-form #submit") && (e("#unhittable-alert").hide(), e("#contact-form #submit").on("click", function() {
                var t = e("#name").val(),
                    n = e("#subject").val(),
                    i = e("#phone").val(),
                    r = e("#email").val(),
                    o = e("#msg").val();
                if (!/^([a-zA-Z0-9_.+-])+\@(([a-zA-Z0-9-])+\.)+([a-zA-Z0-9]{2,4})+$/.test(r)) return e("#unhittable-alert").fadeIn().html('<div class="alert alert-danger"><strong>Warning!</strong> Please Enter Valid Email.</div>'), !1;
                if (t = e.trim(t), n = e.trim(n), i = e.trim(i), r = e.trim(r), o = e.trim(o), "" != t && "" != r && "" != o) {
                    var a = "name=" + t + "&subject=" + n + "&phone=" + i + "&email=" + r + "&msg=" + o;
                    e.ajax({
                        type: "POST",
                        url: "assets/php/mail.php",
                        data: a,
                        success: function() {
                            e("#name").val(""), e("#subject").val(""), e("#phone").val(""), e("#email").val(""), e("#msg").val(""), e("#unhittable-alert").fadeIn().html('<div class="alert alert-success"><strong>Success!</strong> Email has been sent successfully.</div>'), setTimeout(function() {
                                e("#unhittable-alert").fadeOut("slow")
                            }, 4e3)
                        }
                    })
                } else e("#unhittable-alert").fadeIn().html('<div class="alert alert-danger"><strong>Warning!</strong> All fields are required.</div>');
                return !1
            })), e(".unhittable-progressbar").each(function() {
                var t = e(this).data("progress") + "%";
                e(this).find(".unhittable-progressbar-in").css("width", t)
            }), t(),
            function() {
                e(".unhittable-smooth-move").on("click", function() {
                    var t = e(this).attr("href");
                    if (e(t).length) {
                        var n = e(t).offset().top - 10;
                        e("body,html").animate({
                            scrollTop: n
                        }, 800)
                    }
                    return !1
                });
                var t = 300,
                    n = 200;
                e(".unhittable-onepage-nav").each(function() {
                    var i = e(this),
                        r = i.parent(),
                        o = null,
                        a = i.find("a");
                    e(window).on("scroll", function() {
                        var s = window.scrollY,
                            l = (i.outerHeight(), r.offset().top, r.outerHeight(), function(i) {
                                var r = a.first();
                                if (i < t) return r;
                                for (var o = 0; o < a.length; o++) {
                                    var s = a.eq(o),
                                        l = s.attr("href");
                                    if ("#" === l.charAt(0) && l.length > 1) {
                                        var c = e(l).first();
                                        if (c.length > 0) {
                                            var u = c.offset();
                                            if (i < u.top - n) return r;
                                            r = s
                                        }
                                    }
                                }
                                return r
                            }(s));
                        o !== l && (i.find(".active").removeClass("active"), l.addClass("active"), o = l)
                    })
                })
            }(), e(".unhittable-nav").append('<span class="unhittable-munu-toggle"><span></span></span>'), e(".menu-item-has-children").append('<span class="unhittable-munu-dropdown-toggle"></span>'), e(".unhittable-munu-toggle").on("click", function() {
                e(this).toggleClass("unhittable-toggle-active").siblings(".unhittable-nav-list").slideToggle()
            }), e(".unhittable-munu-dropdown-toggle").on("click", function() {
                e(this).toggleClass("active").siblings("ul").slideToggle()
            }), e(".unhittable-lightgallery").each(function() {
                e(this).lightGallery({
                    selector: ".unhittable-lightbox-item",
                    subHtmlSelectorRelative: !1,
                    thumbnail: !1,
                    mousewheel: !0
                })
            }), e(".unhittable-social-btn").hover(function() {
                e(this).addClass("active").siblings().removeClass("active")
            }), e(".unhittable-slider").each(function() {
                var t = e(this).find(".slick-container"),
                    n = e(this).find(".slick-wrapper"),
                    i = (e(this).siblings(".slider-number"), parseInt(t.attr("data-autoplay"), 10)),
                    r = 3e3;
                i > 1 && (r = i, i = 1);
                var o = parseInt(t.attr("data-speed"), 10),
                    a = Boolean(parseInt(t.attr("data-loop"), 10)),
                    s = Boolean(parseInt(t.attr("data-center"), 10)),
                    l = e(this).children().hasClass("pagination"),
                    c = t.attr("data-slides-per-view");
                if (1 == c && (c = 1), "responsive" == c) var c = parseInt(t.attr("data-add-slides"), 10),
                    u = parseInt(t.attr("data-lg-slides"), 10),
                    d = parseInt(t.attr("data-md-slides"), 10),
                    p = parseInt(t.attr("data-sm-slides"), 10),
                    f = parseInt(t.attr("data-xs-slides"), 10);
                var h = parseInt(e(t).attr("data-fade-slide"));
                h = 1 === h, n.slick({
                    infinite: !0,
                    autoplay: i,
                    dots: l,
                    centerPadding: "0",
                    speed: o,
                    infinite: a,
                    autoplaySpeed: r,
                    centerMode: s,
                    fade: h,
                    prevArrow: e(this).find(".slick-arrow-left"),
                    nextArrow: e(this).find(".slick-arrow-right"),
                    appendDots: e(this).find(".pagination"),
                    slidesToShow: c,
                    responsive: [{
                        breakpoint: 1600,
                        settings: {
                            slidesToShow: u
                        }
                    }, {
                        breakpoint: 1200,
                        settings: {
                            slidesToShow: d
                        }
                    }, {
                        breakpoint: 992,
                        settings: {
                            slidesToShow: p
                        }
                    }, {
                        breakpoint: 768,
                        settings: {
                            slidesToShow: f
                        }
                    }]
                })
            }), e.exists("#particles-js") && particlesJS("particles-js", {
                particles: {
                    number: {
                        value: 655,
                        density: {
                            enable: !0,
                            value_area: 989.1476416322727
                        }
                    },
                    color: {
                        value: "#ff3333"
                    },
                    shape: {
                        type: "circle",
                        stroke: {
                            width: 0,
                            color: "#ff3333"
                        },
                        polygon: {
                            nb_sides: 5
                        },
                        image: {
                            src: "img/github.svg",
                            width: 200,
                            height: 200
                        }
                    },
                    opacity: {
                        value: .48927153781200905,
                        random: !1,
                        anim: {
                            enable: !0,
                            speed: .6,
                            opacity_min: 0,
                            sync: !1
                        }
                    },
                    size: {
                        value: 3,
                        random: !0,
                        anim: {
                            enable: !0,
                            speed: 5,
                            size_min: 0,
                            sync: !1
                        }
                    },
                    line_linked: {
                        enable: !1,
                        distance: 150,
                        color: "#ffffff",
                        opacity: .4,
                        width: 1
                    },
                    move: {
                        enable: !0,
                        speed: .2,
                        direction: "none",
                        random: !0,
                        straight: !1,
                        out_mode: "out",
                        bounce: !1,
                        attract: {
                            enable: !1,
                            rotateX: 600,
                            rotateY: 1200
                        }
                    }
                },
                interactivity: {
                    detect_on: "canvas",
                    events: {
                        onhover: {
                            enable: !0,
                            mode: "bubble"
                        },
                        onclick: {
                            enable: !0,
                            mode: "push"
                        },
                        resize: !0
                    },
                    modes: {
                        grab: {
                            distance: 400,
                            line_linked: {
                                opacity: 1
                            }
                        },
                        bubble: {
                            distance: 83.91608391608392,
                            size: 1,
                            duration: 3,
                            opacity: 1,
                            speed: 3
                        },
                        repulse: {
                            distance: 200,
                            duration: .4
                        },
                        push: {
                            particles_nb: 4
                        },
                        remove: {
                            particles_nb: 2
                        }
                    }
                },
                retina_detect: !0
            }), n(), e.exists(".unhittable-ripple-version") && e(".unhittable-ripple-version").each(function() {
                e(".unhittable-ripple-version").ripples({
                    resolution: 512,
                    dropRadius: 20,
                    perturbance: .04
                })
            }), (new WOW).init()
    }), e(window).on("scroll", function() {
        t(), n()
    })
}(jQuery);
var pJS = function(e, t) {
    var n = document.querySelector("#" + e + " > .particles-js-canvas-el");
    this.pJS = {
        canvas: {
            el: n,
            w: n.offsetWidth,
            h: n.offsetHeight
        },
        particles: {
            number: {
                value: 400,
                density: {
                    enable: !0,
                    value_area: 800
                }
            },
            color: {
                value: "#fff"
            },
            shape: {
                type: "circle",
                stroke: {
                    width: 0,
                    color: "#ff0000"
                },
                polygon: {
                    nb_sides: 5
                },
                image: {
                    src: "",
                    width: 100,
                    height: 100
                }
            },
            opacity: {
                value: 1,
                random: !1,
                anim: {
                    enable: !1,
                    speed: 2,
                    opacity_min: 0,
                    sync: !1
                }
            },
            size: {
                value: 20,
                random: !1,
                anim: {
                    enable: !1,
                    speed: 20,
                    size_min: 0,
                    sync: !1
                }
            },
            line_linked: {
                enable: !0,
                distance: 100,
                color: "#fff",
                opacity: 1,
                width: 1
            },
            move: {
                enable: !0,
                speed: 2,
                direction: "none",
                random: !1,
                straight: !1,
                out_mode: "out",
                bounce: !1,
                attract: {
                    enable: !1,
                    rotateX: 3e3,
                    rotateY: 3e3
                }
            },
            array: []
        },
        interactivity: {
            detect_on: "canvas",
            events: {
                onhover: {
                    enable: !0,
                    mode: "grab"
                },
                onclick: {
                    enable: !0,
                    mode: "push"
                },
                resize: !0
            },
            modes: {
                grab: {
                    distance: 100,
                    line_linked: {
                        opacity: 1
                    }
                },
                bubble: {
                    distance: 200,
                    size: 80,
                    duration: .4
                },
                repulse: {
                    distance: 200,
                    duration: .4
                },
                push: {
                    particles_nb: 4
                },
                remove: {
                    particles_nb: 2
                }
            },
            mouse: {}
        },
        retina_detect: !1,
        fn: {
            interact: {},
            modes: {},
            vendors: {}
        },
        tmp: {}
    };
    var i = this.pJS;
    t && Object.deepExtend(i, t), i.tmp.obj = {
        size_value: i.particles.size.value,
        size_anim_speed: i.particles.size.anim.speed,
        move_speed: i.particles.move.speed,
        line_linked_distance: i.particles.line_linked.distance,
        line_linked_width: i.particles.line_linked.width,
        mode_grab_distance: i.interactivity.modes.grab.distance,
        mode_bubble_distance: i.interactivity.modes.bubble.distance,
        mode_bubble_size: i.interactivity.modes.bubble.size,
        mode_repulse_distance: i.interactivity.modes.repulse.distance
    }, i.fn.retinaInit = function() {
        i.retina_detect && window.devicePixelRatio > 1 ? (i.canvas.pxratio = window.devicePixelRatio, i.tmp.retina = !0) : (i.canvas.pxratio = 1, i.tmp.retina = !1), i.canvas.w = i.canvas.el.offsetWidth * i.canvas.pxratio, i.canvas.h = i.canvas.el.offsetHeight * i.canvas.pxratio, i.particles.size.value = i.tmp.obj.size_value * i.canvas.pxratio, i.particles.size.anim.speed = i.tmp.obj.size_anim_speed * i.canvas.pxratio, i.particles.move.speed = i.tmp.obj.move_speed * i.canvas.pxratio, i.particles.line_linked.distance = i.tmp.obj.line_linked_distance * i.canvas.pxratio, i.interactivity.modes.grab.distance = i.tmp.obj.mode_grab_distance * i.canvas.pxratio, i.interactivity.modes.bubble.distance = i.tmp.obj.mode_bubble_distance * i.canvas.pxratio, i.particles.line_linked.width = i.tmp.obj.line_linked_width * i.canvas.pxratio, i.interactivity.modes.bubble.size = i.tmp.obj.mode_bubble_size * i.canvas.pxratio, i.interactivity.modes.repulse.distance = i.tmp.obj.mode_repulse_distance * i.canvas.pxratio
    }, i.fn.canvasInit = function() {
        i.canvas.ctx = i.canvas.el.getContext("2d")
    }, i.fn.canvasSize = function() {
        i.canvas.el.width = i.canvas.w, i.canvas.el.height = i.canvas.h, i && i.interactivity.events.resize && window.addEventListener("resize", function() {
            i.canvas.w = i.canvas.el.offsetWidth, i.canvas.h = i.canvas.el.offsetHeight, i.tmp.retina && (i.canvas.w *= i.canvas.pxratio, i.canvas.h *= i.canvas.pxratio), i.canvas.el.width = i.canvas.w, i.canvas.el.height = i.canvas.h, i.particles.move.enable || (i.fn.particlesEmpty(), i.fn.particlesCreate(), i.fn.particlesDraw(), i.fn.vendors.densityAutoParticles()), i.fn.vendors.densityAutoParticles()
        })
    }, i.fn.canvasPaint = function() {
        i.canvas.ctx.fillRect(0, 0, i.canvas.w, i.canvas.h)
    }, i.fn.canvasClear = function() {
        i.canvas.ctx.clearRect(0, 0, i.canvas.w, i.canvas.h)
    }, i.fn.particle = function(e, t, n) {
        if (this.radius = (i.particles.size.random ? Math.random() : 1) * i.particles.size.value, i.particles.size.anim.enable && (this.size_status = !1, this.vs = i.particles.size.anim.speed / 100, i.particles.size.anim.sync || (this.vs = this.vs * Math.random())), this.x = n ? n.x : Math.random() * i.canvas.w, this.y = n ? n.y : Math.random() * i.canvas.h, this.x > i.canvas.w - 2 * this.radius ? this.x = this.x - this.radius : this.x < 2 * this.radius && (this.x = this.x + this.radius), this.y > i.canvas.h - 2 * this.radius ? this.y = this.y - this.radius : this.y < 2 * this.radius && (this.y = this.y + this.radius), i.particles.move.bounce && i.fn.vendors.checkOverlap(this, n), this.color = {}, "object" == typeof e.value)
            if (e.value instanceof Array) {
                var r = e.value[Math.floor(Math.random() * i.particles.color.value.length)];
                this.color.rgb = hexToRgb(r)
            } else null != e.value.r && null != e.value.g && null != e.value.b && (this.color.rgb = {
                r: e.value.r,
                g: e.value.g,
                b: e.value.b
            }), null != e.value.h && null != e.value.s && null != e.value.l && (this.color.hsl = {
                h: e.value.h,
                s: e.value.s,
                l: e.value.l
            });
        else "random" == e.value ? this.color.rgb = {
            r: Math.floor(256 * Math.random()) + 0,
            g: Math.floor(256 * Math.random()) + 0,
            b: Math.floor(256 * Math.random()) + 0
        } : "string" == typeof e.value && (this.color = e, this.color.rgb = hexToRgb(this.color.value));
        this.opacity = (i.particles.opacity.random ? Math.random() : 1) * i.particles.opacity.value, i.particles.opacity.anim.enable && (this.opacity_status = !1, this.vo = i.particles.opacity.anim.speed / 100, i.particles.opacity.anim.sync || (this.vo = this.vo * Math.random()));
        var o = {};
        switch (i.particles.move.direction) {
            case "top":
                o = {
                    x: 0,
                    y: -1
                };
                break;
            case "top-right":
                o = {
                    x: .5,
                    y: -.5
                };
                break;
            case "right":
                o = {
                    x: 1,
                    y: -0
                };
                break;
            case "bottom-right":
                o = {
                    x: .5,
                    y: .5
                };
                break;
            case "bottom":
                o = {
                    x: 0,
                    y: 1
                };
                break;
            case "bottom-left":
                o = {
                    x: -.5,
                    y: 1
                };
                break;
            case "left":
                o = {
                    x: -1,
                    y: 0
                };
                break;
            case "top-left":
                o = {
                    x: -.5,
                    y: -.5
                };
                break;
            default:
                o = {
                    x: 0,
                    y: 0
                }
        }
        i.particles.move.straight ? (this.vx = o.x, this.vy = o.y, i.particles.move.random && (this.vx = this.vx * Math.random(), this.vy = this.vy * Math.random())) : (this.vx = o.x + Math.random() - .5, this.vy = o.y + Math.random() - .5), this.vx_i = this.vx, this.vy_i = this.vy;
        var a = i.particles.shape.type;
        if ("object" == typeof a) {
            if (a instanceof Array) {
                var s = a[Math.floor(Math.random() * a.length)];
                this.shape = s
            }
        } else this.shape = a;
        if ("image" == this.shape) {
            var l = i.particles.shape;
            this.img = {
                src: l.image.src,
                ratio: l.image.width / l.image.height
            }, this.img.ratio || (this.img.ratio = 1), "svg" == i.tmp.img_type && null != i.tmp.source_svg && (i.fn.vendors.createSvgImg(this), i.tmp.pushing && (this.img.loaded = !1))
        }
    }, i.fn.particle.prototype.draw = function() {
        var e = this;
        if (null != e.radius_bubble) var t = e.radius_bubble;
        else t = e.radius;
        if (null != e.opacity_bubble) var n = e.opacity_bubble;
        else n = e.opacity;
        if (e.color.rgb) var r = "rgba(" + e.color.rgb.r + "," + e.color.rgb.g + "," + e.color.rgb.b + "," + n + ")";
        else r = "hsla(" + e.color.hsl.h + "," + e.color.hsl.s + "%," + e.color.hsl.l + "%," + n + ")";
        switch (i.canvas.ctx.fillStyle = r, i.canvas.ctx.beginPath(), e.shape) {
            case "circle":
                i.canvas.ctx.arc(e.x, e.y, t, 0, 2 * Math.PI, !1);
                break;
            case "edge":
                i.canvas.ctx.rect(e.x - t, e.y - t, 2 * t, 2 * t);
                break;
            case "triangle":
                i.fn.vendors.drawShape(i.canvas.ctx, e.x - t, e.y + t / 1.66, 2 * t, 3, 2);
                break;
            case "polygon":
                i.fn.vendors.drawShape(i.canvas.ctx, e.x - t / (i.particles.shape.polygon.nb_sides / 3.5), e.y - t / .76, 2.66 * t / (i.particles.shape.polygon.nb_sides / 3), i.particles.shape.polygon.nb_sides, 1);
                break;
            case "star":
                i.fn.vendors.drawShape(i.canvas.ctx, e.x - 2 * t / (i.particles.shape.polygon.nb_sides / 4), e.y - t / 1.52, 2 * t * 2.66 / (i.particles.shape.polygon.nb_sides / 3), i.particles.shape.polygon.nb_sides, 2);
                break;
            case "image":
                if ("svg" == i.tmp.img_type) var o = e.img.obj;
                else o = i.tmp.img_obj;
                o && i.canvas.ctx.drawImage(o, e.x - t, e.y - t, 2 * t, 2 * t / e.img.ratio)
        }
        i.canvas.ctx.closePath(), i.particles.shape.stroke.width > 0 && (i.canvas.ctx.strokeStyle = i.particles.shape.stroke.color, i.canvas.ctx.lineWidth = i.particles.shape.stroke.width, i.canvas.ctx.stroke()), i.canvas.ctx.fill()
    }, i.fn.particlesCreate = function() {
        for (var e = 0; e < i.particles.number.value; e++) i.particles.array.push(new i.fn.particle(i.particles.color, i.particles.opacity.value))
    }, i.fn.particlesUpdate = function() {
        for (var e = 0; e < i.particles.array.length; e++) {
            var t = i.particles.array[e];
            if (i.particles.move.enable) {
                var n = i.particles.move.speed / 2;
                t.x += t.vx * n, t.y += t.vy * n
            }
            if (i.particles.opacity.anim.enable && (1 == t.opacity_status ? (t.opacity >= i.particles.opacity.value && (t.opacity_status = !1), t.opacity += t.vo) : (t.opacity <= i.particles.opacity.anim.opacity_min && (t.opacity_status = !0), t.opacity -= t.vo), t.opacity < 0 && (t.opacity = 0)), i.particles.size.anim.enable && (1 == t.size_status ? (t.radius >= i.particles.size.value && (t.size_status = !1), t.radius += t.vs) : (t.radius <= i.particles.size.anim.size_min && (t.size_status = !0), t.radius -= t.vs), t.radius < 0 && (t.radius = 0)), "bounce" == i.particles.move.out_mode) var r = {
                x_left: t.radius,
                x_right: i.canvas.w,
                y_top: t.radius,
                y_bottom: i.canvas.h
            };
            else r = {
                x_left: -t.radius,
                x_right: i.canvas.w + t.radius,
                y_top: -t.radius,
                y_bottom: i.canvas.h + t.radius
            };
            switch (t.x - t.radius > i.canvas.w ? (t.x = r.x_left, t.y = Math.random() * i.canvas.h) : t.x + t.radius < 0 && (t.x = r.x_right, t.y = Math.random() * i.canvas.h), t.y - t.radius > i.canvas.h ? (t.y = r.y_top, t.x = Math.random() * i.canvas.w) : t.y + t.radius < 0 && (t.y = r.y_bottom, t.x = Math.random() * i.canvas.w), i.particles.move.out_mode) {
                case "bounce":
                    t.x + t.radius > i.canvas.w ? t.vx = -t.vx : t.x - t.radius < 0 && (t.vx = -t.vx), t.y + t.radius > i.canvas.h ? t.vy = -t.vy : t.y - t.radius < 0 && (t.vy = -t.vy)
            }
            if (isInArray("grab", i.interactivity.events.onhover.mode) && i.fn.modes.grabParticle(t), (isInArray("bubble", i.interactivity.events.onhover.mode) || isInArray("bubble", i.interactivity.events.onclick.mode)) && i.fn.modes.bubbleParticle(t), (isInArray("repulse", i.interactivity.events.onhover.mode) || isInArray("repulse", i.interactivity.events.onclick.mode)) && i.fn.modes.repulseParticle(t), i.particles.line_linked.enable || i.particles.move.attract.enable)
                for (var o = e + 1; o < i.particles.array.length; o++) {
                    var a = i.particles.array[o];
                    i.particles.line_linked.enable && i.fn.interact.linkParticles(t, a), i.particles.move.attract.enable && i.fn.interact.attractParticles(t, a), i.particles.move.bounce && i.fn.interact.bounceParticles(t, a)
                }
        }
    }, i.fn.particlesDraw = function() {
        i.canvas.ctx.clearRect(0, 0, i.canvas.w, i.canvas.h), i.fn.particlesUpdate();
        for (var e = 0; e < i.particles.array.length; e++) {
            i.particles.array[e].draw()
        }
    }, i.fn.particlesEmpty = function() {
        i.particles.array = []
    }, i.fn.particlesRefresh = function() {
        cancelRequestAnimFrame(i.fn.checkAnimFrame), cancelRequestAnimFrame(i.fn.drawAnimFrame), i.tmp.source_svg = void 0, i.tmp.img_obj = void 0, i.tmp.count_svg = 0, i.fn.particlesEmpty(), i.fn.canvasClear(), i.fn.vendors.start()
    }, i.fn.interact.linkParticles = function(e, t) {
        var n = e.x - t.x,
            r = e.y - t.y,
            o = Math.sqrt(n * n + r * r);
        if (o <= i.particles.line_linked.distance) {
            var a = i.particles.line_linked.opacity - o / (1 / i.particles.line_linked.opacity) / i.particles.line_linked.distance;
            if (a > 0) {
                var s = i.particles.line_linked.color_rgb_line;
                i.canvas.ctx.strokeStyle = "rgba(" + s.r + "," + s.g + "," + s.b + "," + a + ")", i.canvas.ctx.lineWidth = i.particles.line_linked.width, i.canvas.ctx.beginPath(), i.canvas.ctx.moveTo(e.x, e.y), i.canvas.ctx.lineTo(t.x, t.y), i.canvas.ctx.stroke(), i.canvas.ctx.closePath()
            }
        }
    }, i.fn.interact.attractParticles = function(e, t) {
        var n = e.x - t.x,
            r = e.y - t.y;
        if (Math.sqrt(n * n + r * r) <= i.particles.line_linked.distance) {
            var o = n / (1e3 * i.particles.move.attract.rotateX),
                a = r / (1e3 * i.particles.move.attract.rotateY);
            e.vx -= o, e.vy -= a, t.vx += o, t.vy += a
        }
    }, i.fn.interact.bounceParticles = function(e, t) {
        var n = e.x - t.x,
            i = e.y - t.y,
            r = Math.sqrt(n * n + i * i);
        e.radius + t.radius >= r && (e.vx = -e.vx, e.vy = -e.vy, t.vx = -t.vx, t.vy = -t.vy)
    }, i.fn.modes.pushParticles = function(e, t) {
        i.tmp.pushing = !0;
        for (var n = 0; e > n; n++) i.particles.array.push(new i.fn.particle(i.particles.color, i.particles.opacity.value, {
            x: t ? t.pos_x : Math.random() * i.canvas.w,
            y: t ? t.pos_y : Math.random() * i.canvas.h
        })), n == e - 1 && (i.particles.move.enable || i.fn.particlesDraw(), i.tmp.pushing = !1)
    }, i.fn.modes.removeParticles = function(e) {
        i.particles.array.splice(0, e), i.particles.move.enable || i.fn.particlesDraw()
    }, i.fn.modes.bubbleParticle = function(e) {
        function t() {
            e.opacity_bubble = e.opacity, e.radius_bubble = e.radius
        }

        function n(t, n, r, o, a) {
            if (t != n)
                if (i.tmp.bubble_duration_end) {
                    if (null != r) l = t + (t - (o - d * (o - t) / i.interactivity.modes.bubble.duration)), "size" == a && (e.radius_bubble = l), "opacity" == a && (e.opacity_bubble = l)
                } else if (u <= i.interactivity.modes.bubble.distance) {
                if (null != r) var s = r;
                else s = o;
                if (s != t) {
                    var l = o - d * (o - t) / i.interactivity.modes.bubble.duration;
                    "size" == a && (e.radius_bubble = l), "opacity" == a && (e.opacity_bubble = l)
                }
            } else "size" == a && (e.radius_bubble = void 0), "opacity" == a && (e.opacity_bubble = void 0)
        }
        if (i.interactivity.events.onhover.enable && isInArray("bubble", i.interactivity.events.onhover.mode)) {
            var r = e.x - i.interactivity.mouse.pos_x,
                o = e.y - i.interactivity.mouse.pos_y,
                a = 1 - (u = Math.sqrt(r * r + o * o)) / i.interactivity.modes.bubble.distance;
            if (u <= i.interactivity.modes.bubble.distance) {
                if (a >= 0 && "mousemove" == i.interactivity.status) {
                    if (i.interactivity.modes.bubble.size != i.particles.size.value)
                        if (i.interactivity.modes.bubble.size > i.particles.size.value) {
                            (l = e.radius + i.interactivity.modes.bubble.size * a) >= 0 && (e.radius_bubble = l)
                        } else {
                            var s = e.radius - i.interactivity.modes.bubble.size,
                                l = e.radius - s * a;
                            e.radius_bubble = l > 0 ? l : 0
                        } if (i.interactivity.modes.bubble.opacity != i.particles.opacity.value)
                        if (i.interactivity.modes.bubble.opacity > i.particles.opacity.value) {
                            (c = i.interactivity.modes.bubble.opacity * a) > e.opacity && c <= i.interactivity.modes.bubble.opacity && (e.opacity_bubble = c)
                        } else {
                            var c;
                            (c = e.opacity - (i.particles.opacity.value - i.interactivity.modes.bubble.opacity) * a) < e.opacity && c >= i.interactivity.modes.bubble.opacity && (e.opacity_bubble = c)
                        }
                }
            } else t();
            "mouseleave" == i.interactivity.status && t()
        } else if (i.interactivity.events.onclick.enable && isInArray("bubble", i.interactivity.events.onclick.mode)) {
            if (i.tmp.bubble_clicking) {
                r = e.x - i.interactivity.mouse.click_pos_x, o = e.y - i.interactivity.mouse.click_pos_y;
                var u = Math.sqrt(r * r + o * o),
                    d = ((new Date).getTime() - i.interactivity.mouse.click_time) / 1e3;
                d > i.interactivity.modes.bubble.duration && (i.tmp.bubble_duration_end = !0), d > 2 * i.interactivity.modes.bubble.duration && (i.tmp.bubble_clicking = !1, i.tmp.bubble_duration_end = !1)
            }
            i.tmp.bubble_clicking && (n(i.interactivity.modes.bubble.size, i.particles.size.value, e.radius_bubble, e.radius, "size"), n(i.interactivity.modes.bubble.opacity, i.particles.opacity.value, e.opacity_bubble, e.opacity, "opacity"))
        }
    }, i.fn.modes.repulseParticle = function(e) {
        if (i.interactivity.events.onhover.enable && isInArray("repulse", i.interactivity.events.onhover.mode) && "mousemove" == i.interactivity.status) {
            var t = e.x - i.interactivity.mouse.pos_x,
                n = e.y - i.interactivity.mouse.pos_y,
                r = Math.sqrt(t * t + n * n),
                o = {
                    x: t / r,
                    y: n / r
                },
                a = clamp(1 / (l = i.interactivity.modes.repulse.distance) * (-1 * Math.pow(r / l, 2) + 1) * l * 100, 0, 50),
                s = {
                    x: e.x + o.x * a,
                    y: e.y + o.y * a
                };
            "bounce" == i.particles.move.out_mode ? (s.x - e.radius > 0 && s.x + e.radius < i.canvas.w && (e.x = s.x), s.y - e.radius > 0 && s.y + e.radius < i.canvas.h && (e.y = s.y)) : (e.x = s.x, e.y = s.y)
        } else if (i.interactivity.events.onclick.enable && isInArray("repulse", i.interactivity.events.onclick.mode))
            if (i.tmp.repulse_finish || (i.tmp.repulse_count++, i.tmp.repulse_count == i.particles.array.length && (i.tmp.repulse_finish = !0)), i.tmp.repulse_clicking) {
                var l = Math.pow(i.interactivity.modes.repulse.distance / 6, 3),
                    c = i.interactivity.mouse.click_pos_x - e.x,
                    u = i.interactivity.mouse.click_pos_y - e.y,
                    d = c * c + u * u,
                    p = -l / d * 1;
                l >= d && function() {
                    var t = Math.atan2(u, c);
                    if (e.vx = p * Math.cos(t), e.vy = p * Math.sin(t), "bounce" == i.particles.move.out_mode) {
                        var n = {
                            x: e.x + e.vx,
                            y: e.y + e.vy
                        };
                        n.x + e.radius > i.canvas.w ? e.vx = -e.vx : n.x - e.radius < 0 && (e.vx = -e.vx), n.y + e.radius > i.canvas.h ? e.vy = -e.vy : n.y - e.radius < 0 && (e.vy = -e.vy)
                    }
                }()
            } else 0 == i.tmp.repulse_clicking && (e.vx = e.vx_i, e.vy = e.vy_i)
    }, i.fn.modes.grabParticle = function(e) {
        if (i.interactivity.events.onhover.enable && "mousemove" == i.interactivity.status) {
            var t = e.x - i.interactivity.mouse.pos_x,
                n = e.y - i.interactivity.mouse.pos_y,
                r = Math.sqrt(t * t + n * n);
            if (r <= i.interactivity.modes.grab.distance) {
                var o = i.interactivity.modes.grab.line_linked.opacity - r / (1 / i.interactivity.modes.grab.line_linked.opacity) / i.interactivity.modes.grab.distance;
                if (o > 0) {
                    var a = i.particles.line_linked.color_rgb_line;
                    i.canvas.ctx.strokeStyle = "rgba(" + a.r + "," + a.g + "," + a.b + "," + o + ")", i.canvas.ctx.lineWidth = i.particles.line_linked.width, i.canvas.ctx.beginPath(), i.canvas.ctx.moveTo(e.x, e.y), i.canvas.ctx.lineTo(i.interactivity.mouse.pos_x, i.interactivity.mouse.pos_y), i.canvas.ctx.stroke(), i.canvas.ctx.closePath()
                }
            }
        }
    }, i.fn.vendors.eventsListeners = function() {
        "window" == i.interactivity.detect_on ? i.interactivity.el = window : i.interactivity.el = i.canvas.el, (i.interactivity.events.onhover.enable || i.interactivity.events.onclick.enable) && (i.interactivity.el.addEventListener("mousemove", function(e) {
            if (i.interactivity.el == window) var t = e.clientX,
                n = e.clientY;
            else t = e.offsetX || e.clientX, n = e.offsetY || e.clientY;
            i.interactivity.mouse.pos_x = t, i.interactivity.mouse.pos_y = n, i.tmp.retina && (i.interactivity.mouse.pos_x *= i.canvas.pxratio, i.interactivity.mouse.pos_y *= i.canvas.pxratio), i.interactivity.status = "mousemove"
        }), i.interactivity.el.addEventListener("mouseleave", function(e) {
            i.interactivity.mouse.pos_x = null, i.interactivity.mouse.pos_y = null, i.interactivity.status = "mouseleave"
        })), i.interactivity.events.onclick.enable && i.interactivity.el.addEventListener("click", function() {
            if (i.interactivity.mouse.click_pos_x = i.interactivity.mouse.pos_x, i.interactivity.mouse.click_pos_y = i.interactivity.mouse.pos_y, i.interactivity.mouse.click_time = (new Date).getTime(), i.interactivity.events.onclick.enable) switch (i.interactivity.events.onclick.mode) {
                case "push":
                    i.particles.move.enable ? i.fn.modes.pushParticles(i.interactivity.modes.push.particles_nb, i.interactivity.mouse) : 1 == i.interactivity.modes.push.particles_nb ? i.fn.modes.pushParticles(i.interactivity.modes.push.particles_nb, i.interactivity.mouse) : i.interactivity.modes.push.particles_nb > 1 && i.fn.modes.pushParticles(i.interactivity.modes.push.particles_nb);
                    break;
                case "remove":
                    i.fn.modes.removeParticles(i.interactivity.modes.remove.particles_nb);
                    break;
                case "bubble":
                    i.tmp.bubble_clicking = !0;
                    break;
                case "repulse":
                    i.tmp.repulse_clicking = !0, i.tmp.repulse_count = 0, i.tmp.repulse_finish = !1, setTimeout(function() {
                        i.tmp.repulse_clicking = !1
                    }, 1e3 * i.interactivity.modes.repulse.duration)
            }
        })
    }, i.fn.vendors.densityAutoParticles = function() {
        if (i.particles.number.density.enable) {
            var e = i.canvas.el.width * i.canvas.el.height / 1e3;
            i.tmp.retina && (e /= 2 * i.canvas.pxratio);
            var t = e * i.particles.number.value / i.particles.number.density.value_area,
                n = i.particles.array.length - t;
            0 > n ? i.fn.modes.pushParticles(Math.abs(n)) : i.fn.modes.removeParticles(n)
        }
    }, i.fn.vendors.checkOverlap = function(e, t) {
        for (var n = 0; n < i.particles.array.length; n++) {
            var r = i.particles.array[n],
                o = e.x - r.x,
                a = e.y - r.y;
            Math.sqrt(o * o + a * a) <= e.radius + r.radius && (e.x = t ? t.x : Math.random() * i.canvas.w, e.y = t ? t.y : Math.random() * i.canvas.h, i.fn.vendors.checkOverlap(e))
        }
    }, i.fn.vendors.createSvgImg = function(e) {
        var t = i.tmp.source_svg.replace(/#([0-9A-F]{3,6})/gi, function(t, n, i, r) {
                if (e.color.rgb) var o = "rgba(" + e.color.rgb.r + "," + e.color.rgb.g + "," + e.color.rgb.b + "," + e.opacity + ")";
                else o = "hsla(" + e.color.hsl.h + "," + e.color.hsl.s + "%," + e.color.hsl.l + "%," + e.opacity + ")";
                return o
            }),
            n = new Blob([t], {
                type: "image/svg+xml;charset=utf-8"
            }),
            r = window.URL || window.webkitURL || window,
            o = r.createObjectURL(n),
            a = new Image;
        a.addEventListener("load", function() {
            e.img.obj = a, e.img.loaded = !0, r.revokeObjectURL(o), i.tmp.count_svg++
        }), a.src = o
    }, i.fn.vendors.destroypJS = function() {
        cancelAnimationFrame(i.fn.drawAnimFrame), n.remove(), pJSDom = null
    }, i.fn.vendors.drawShape = function(e, t, n, i, r, o) {
        var a = r * o,
            s = r / o,
            l = 180 * (s - 2) / s,
            c = Math.PI - Math.PI * l / 180;
        e.save(), e.beginPath(), e.translate(t, n), e.moveTo(0, 0);
        for (var u = 0; a > u; u++) e.lineTo(i, 0), e.translate(i, 0), e.rotate(c);
        e.fill(), e.restore()
    }, i.fn.vendors.exportImg = function() {
        window.open(i.canvas.el.toDataURL("image/png"), "_blank")
    }, i.fn.vendors.loadImg = function(e) {
        if (i.tmp.img_error = void 0, "" != i.particles.shape.image.src)
            if ("svg" == e) {
                var t = new XMLHttpRequest;
                t.open("GET", i.particles.shape.image.src), t.onreadystatechange = function(e) {
                    4 == t.readyState && (200 == t.status ? (i.tmp.source_svg = e.currentTarget.response, i.fn.vendors.checkBeforeDraw()) : (console.log("Error pJS - Image not found"), i.tmp.img_error = !0))
                }, t.send()
            } else {
                var n = new Image;
                n.addEventListener("load", function() {
                    i.tmp.img_obj = n, i.fn.vendors.checkBeforeDraw()
                }), n.src = i.particles.shape.image.src
            }
        else console.log("Error pJS - No image.src"), i.tmp.img_error = !0
    }, i.fn.vendors.draw = function() {
        "image" == i.particles.shape.type ? "svg" == i.tmp.img_type ? i.tmp.count_svg >= i.particles.number.value ? (i.fn.particlesDraw(), i.particles.move.enable ? i.fn.drawAnimFrame = requestAnimFrame(i.fn.vendors.draw) : cancelRequestAnimFrame(i.fn.drawAnimFrame)) : i.tmp.img_error || (i.fn.drawAnimFrame = requestAnimFrame(i.fn.vendors.draw)) : null != i.tmp.img_obj ? (i.fn.particlesDraw(), i.particles.move.enable ? i.fn.drawAnimFrame = requestAnimFrame(i.fn.vendors.draw) : cancelRequestAnimFrame(i.fn.drawAnimFrame)) : i.tmp.img_error || (i.fn.drawAnimFrame = requestAnimFrame(i.fn.vendors.draw)) : (i.fn.particlesDraw(), i.particles.move.enable ? i.fn.drawAnimFrame = requestAnimFrame(i.fn.vendors.draw) : cancelRequestAnimFrame(i.fn.drawAnimFrame))
    }, i.fn.vendors.checkBeforeDraw = function() {
        "image" == i.particles.shape.type ? "svg" == i.tmp.img_type && null == i.tmp.source_svg ? i.tmp.checkAnimFrame = requestAnimFrame(check) : (cancelRequestAnimFrame(i.tmp.checkAnimFrame), i.tmp.img_error || (i.fn.vendors.init(), i.fn.vendors.draw())) : (i.fn.vendors.init(), i.fn.vendors.draw())
    }, i.fn.vendors.init = function() {
        i.fn.retinaInit(), i.fn.canvasInit(), i.fn.canvasSize(), i.fn.canvasPaint(), i.fn.particlesCreate(), i.fn.vendors.densityAutoParticles(), i.particles.line_linked.color_rgb_line = hexToRgb(i.particles.line_linked.color)
    }, i.fn.vendors.start = function() {
        isInArray("image", i.particles.shape.type) ? (i.tmp.img_type = i.particles.shape.image.src.substr(i.particles.shape.image.src.length - 3), i.fn.vendors.loadImg(i.tmp.img_type)) : i.fn.vendors.checkBeforeDraw()
    }, i.fn.vendors.eventsListeners(), i.fn.vendors.start()
};
Object.deepExtend = function(e, t) {
        for (var n in t) t[n] && t[n].constructor && t[n].constructor === Object ? (e[n] = e[n] || {}, arguments.callee(e[n], t[n])) : e[n] = t[n];
        return e
    }, window.requestAnimFrame = window.requestAnimationFrame || window.webkitRequestAnimationFrame || window.mozRequestAnimationFrame || window.oRequestAnimationFrame || window.msRequestAnimationFrame || function(e) {
        window.setTimeout(e, 1e3 / 60)
    }, window.cancelRequestAnimFrame = window.cancelAnimationFrame || window.webkitCancelRequestAnimationFrame || window.mozCancelRequestAnimationFrame || window.oCancelRequestAnimationFrame || window.msCancelRequestAnimationFrame || clearTimeout, window.pJSDom = [], window.particlesJS = function(e, t) {
        "string" != typeof e && (t = e, e = "particles-js"), e || (e = "particles-js");
        var n = document.getElementById(e),
            i = "particles-js-canvas-el",
            r = n.getElementsByClassName(i);
        if (r.length)
            for (; r.length > 0;) n.removeChild(r[0]);
        var o = document.createElement("canvas");
        o.className = i, o.style.width = "100%", o.style.height = "100%", null != document.getElementById(e).appendChild(o) && pJSDom.push(new pJS(e, t))
    }, window.particlesJS.load = function(e, t, n) {
        var i = new XMLHttpRequest;
        i.open("GET", t), i.onreadystatechange = function(t) {
            if (4 == i.readyState)
                if (200 == i.status) {
                    var r = JSON.parse(t.currentTarget.response);
                    window.particlesJS(e, r), n && n()
                } else console.log("Error pJS - XMLHttpRequest status: " + i.status), console.log("Error pJS - File config not found")
        }, i.send()
    },
    function() {
        var e, t, n, i, r, o = function(e, t) {
                return function() {
                    return e.apply(t, arguments)
                }
            },
            a = [].indexOf || function(e) {
                for (var t = 0, n = this.length; n > t; t++)
                    if (t in this && this[t] === e) return t;
                return -1
            };
        t = function() {
            function e() {}
            return e.prototype.extend = function(e, t) {
                var n, i;
                for (n in t) i = t[n], null == e[n] && (e[n] = i);
                return e
            }, e.prototype.isMobile = function(e) {
                return /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(e)
            }, e.prototype.createEvent = function(e, t, n, i) {
                var r;
                return null == t && (t = !1), null == n && (n = !1), null == i && (i = null), null != document.createEvent ? (r = document.createEvent("CustomEvent")).initCustomEvent(e, t, n, i) : null != document.createEventObject ? (r = document.createEventObject()).eventType = e : r.eventName = e, r
            }, e.prototype.emitEvent = function(e, t) {
                return null != e.dispatchEvent ? e.dispatchEvent(t) : t in (null != e) ? e[t]() : "on" + t in (null != e) ? e["on" + t]() : void 0
            }, e.prototype.addEvent = function(e, t, n) {
                return null != e.addEventListener ? e.addEventListener(t, n, !1) : null != e.attachEvent ? e.attachEvent("on" + t, n) : e[t] = n
            }, e.prototype.removeEvent = function(e, t, n) {
                return null != e.removeEventListener ? e.removeEventListener(t, n, !1) : null != e.detachEvent ? e.detachEvent("on" + t, n) : delete e[t]
            }, e.prototype.innerHeight = function() {
                return "innerHeight" in window ? window.innerHeight : document.documentElement.clientHeight
            }, e
        }(), n = this.WeakMap || this.MozWeakMap || (n = function() {
            function e() {
                this.keys = [], this.values = []
            }
            return e.prototype.get = function(e) {
                var t, n, i, r;
                for (t = n = 0, i = (r = this.keys).length; i > n; t = ++n)
                    if (r[t] === e) return this.values[t]
            }, e.prototype.set = function(e, t) {
                var n, i, r, o;
                for (n = i = 0, r = (o = this.keys).length; r > i; n = ++i)
                    if (o[n] === e) return void(this.values[n] = t);
                return this.keys.push(e), this.values.push(t)
            }, e
        }()), e = this.MutationObserver || this.WebkitMutationObserver || this.MozMutationObserver || (e = function() {
            function e() {
                "undefined" != typeof console && null !== console && console.warn("MutationObserver is not supported by your browser."), "undefined" != typeof console && null !== console && console.warn("WOW.js cannot detect dom mutations, please call .sync() after loading new content.")
            }
            return e.notSupported = !0, e.prototype.observe = function() {}, e
        }()), i = this.getComputedStyle || function(e) {
            return this.getPropertyValue = function(t) {
                var n;
                return "float" === t && (t = "styleFloat"), r.test(t) && t.replace(r, function(e, t) {
                    return t.toUpperCase()
                }), (null != (n = e.currentStyle) ? n[t] : void 0) || null
            }, this
        }, r = /(\-([a-z]){1})/g, this.WOW = function() {
            function r(e) {
                null == e && (e = {}), this.scrollCallback = o(this.scrollCallback, this), this.scrollHandler = o(this.scrollHandler, this), this.resetAnimation = o(this.resetAnimation, this), this.start = o(this.start, this), this.scrolled = !0, this.config = this.util().extend(e, this.defaults), null != e.scrollContainer && (this.config.scrollContainer = document.querySelector(e.scrollContainer)), this.animationNameCache = new n, this.wowEvent = this.util().createEvent(this.config.boxClass)
            }
            return r.prototype.defaults = {
                boxClass: "wow",
                animateClass: "animated",
                offset: 0,
                mobile: !0,
                live: !0,
                callback: null,
                scrollContainer: null
            }, r.prototype.init = function() {
                var e;
                return this.element = window.document.documentElement, "interactive" === (e = document.readyState) || "complete" === e ? this.start() : this.util().addEvent(document, "DOMContentLoaded", this.start), this.finished = []
            }, r.prototype.start = function() {
                var t, n, i, r;
                if (this.stopped = !1, this.boxes = function() {
                        var e, n, i, r;
                        for (r = [], e = 0, n = (i = this.element.querySelectorAll("." + this.config.boxClass)).length; n > e; e++) t = i[e], r.push(t);
                        return r
                    }.call(this), this.all = function() {
                        var e, n, i, r;
                        for (r = [], e = 0, n = (i = this.boxes).length; n > e; e++) t = i[e], r.push(t);
                        return r
                    }.call(this), this.boxes.length)
                    if (this.disabled()) this.resetStyle();
                    else
                        for (n = 0, i = (r = this.boxes).length; i > n; n++) t = r[n], this.applyStyle(t, !0);
                return this.disabled() || (this.util().addEvent(this.config.scrollContainer || window, "scroll", this.scrollHandler), this.util().addEvent(window, "resize", this.scrollHandler), this.interval = setInterval(this.scrollCallback, 50)), this.config.live ? new e(function(e) {
                    return function(t) {
                        var n, i, r, o, a;
                        for (a = [], n = 0, i = t.length; i > n; n++) o = t[n], a.push(function() {
                            var e, t, n, i;
                            for (i = [], e = 0, t = (n = o.addedNodes || []).length; t > e; e++) r = n[e], i.push(this.doSync(r));
                            return i
                        }.call(e));
                        return a
                    }
                }(this)).observe(document.body, {
                    childList: !0,
                    subtree: !0
                }) : void 0
            }, r.prototype.stop = function() {
                return this.stopped = !0, this.util().removeEvent(this.config.scrollContainer || window, "scroll", this.scrollHandler), this.util().removeEvent(window, "resize", this.scrollHandler), null != this.interval ? clearInterval(this.interval) : void 0
            }, r.prototype.sync = function() {
                return e.notSupported ? this.doSync(this.element) : void 0
            }, r.prototype.doSync = function(e) {
                var t, n, i, r, o;
                if (null == e && (e = this.element), 1 === e.nodeType) {
                    for (o = [], n = 0, i = (r = (e = e.parentNode || e).querySelectorAll("." + this.config.boxClass)).length; i > n; n++) t = r[n], a.call(this.all, t) < 0 ? (this.boxes.push(t), this.all.push(t), this.stopped || this.disabled() ? this.resetStyle() : this.applyStyle(t, !0), o.push(this.scrolled = !0)) : o.push(void 0);
                    return o
                }
            }, r.prototype.show = function(e) {
                return this.applyStyle(e), e.className = e.className + " " + this.config.animateClass, null != this.config.callback && this.config.callback(e), this.util().emitEvent(e, this.wowEvent), this.util().addEvent(e, "animationend", this.resetAnimation), this.util().addEvent(e, "oanimationend", this.resetAnimation), this.util().addEvent(e, "webkitAnimationEnd", this.resetAnimation), this.util().addEvent(e, "MSAnimationEnd", this.resetAnimation), e
            }, r.prototype.applyStyle = function(e, t) {
                var n, i, r, o;
                return i = e.getAttribute("data-wow-duration"), n = e.getAttribute("data-wow-delay"), r = e.getAttribute("data-wow-iteration"), this.animate((o = this, function() {
                    return o.customStyle(e, t, i, n, r)
                }))
            }, r.prototype.animate = "requestAnimationFrame" in window ? function(e) {
                return window.requestAnimationFrame(e)
            } : function(e) {
                return e()
            }, r.prototype.resetStyle = function() {
                var e, t, n, i, r;
                for (r = [], t = 0, n = (i = this.boxes).length; n > t; t++) e = i[t], r.push(e.style.visibility = "visible");
                return r
            }, r.prototype.resetAnimation = function(e) {
                var t;
                return e.type.toLowerCase().indexOf("animationend") >= 0 ? (t = e.target || e.srcElement).className = t.className.replace(this.config.animateClass, "").trim() : void 0
            }, r.prototype.customStyle = function(e, t, n, i, r) {
                return t && this.cacheAnimationName(e), e.style.visibility = t ? "hidden" : "visible", n && this.vendorSet(e.style, {
                    animationDuration: n
                }), i && this.vendorSet(e.style, {
                    animationDelay: i
                }), r && this.vendorSet(e.style, {
                    animationIterationCount: r
                }), this.vendorSet(e.style, {
                    animationName: t ? "none" : this.cachedAnimationName(e)
                }), e
            }, r.prototype.vendors = ["moz", "webkit"], r.prototype.vendorSet = function(e, t) {
                var n, i, r, o;
                for (n in i = [], t) r = t[n], e["" + n] = r, i.push(function() {
                    var t, i, a, s;
                    for (s = [], t = 0, i = (a = this.vendors).length; i > t; t++) o = a[t], s.push(e["" + o + n.charAt(0).toUpperCase() + n.substr(1)] = r);
                    return s
                }.call(this));
                return i
            }, r.prototype.vendorCSS = function(e, t) {
                var n, r, o, a, s, l;
                for (a = (s = i(e)).getPropertyCSSValue(t), n = 0, r = (o = this.vendors).length; r > n; n++) l = o[n], a = a || s.getPropertyCSSValue("-" + l + "-" + t);
                return a
            }, r.prototype.animationName = function(e) {
                var t;
                try {
                    t = this.vendorCSS(e, "animation-name").cssText
                } catch (n) {
                    t = i(e).getPropertyValue("animation-name")
                }
                return "none" === t ? "" : t
            }, r.prototype.cacheAnimationName = function(e) {
                return this.animationNameCache.set(e, this.animationName(e))
            }, r.prototype.cachedAnimationName = function(e) {
                return this.animationNameCache.get(e)
            }, r.prototype.scrollHandler = function() {
                return this.scrolled = !0
            }, r.prototype.scrollCallback = function() {
                var e;
                return !this.scrolled || (this.scrolled = !1, this.boxes = function() {
                    var t, n, i, r;
                    for (r = [], t = 0, n = (i = this.boxes).length; n > t; t++)(e = i[t]) && (this.isVisible(e) ? this.show(e) : r.push(e));
                    return r
                }.call(this), this.boxes.length || this.config.live) ? void 0 : this.stop()
            }, r.prototype.offsetTop = function(e) {
                for (var t; void 0 === e.offsetTop;) e = e.parentNode;
                for (t = e.offsetTop; e = e.offsetParent;) t += e.offsetTop;
                return t
            }, r.prototype.isVisible = function(e) {
                var t, n, i, r, o;
                return n = e.getAttribute("data-wow-offset") || this.config.offset, r = (o = this.config.scrollContainer && this.config.scrollContainer.scrollTop || window.pageYOffset) + Math.min(this.element.clientHeight, this.util().innerHeight()) - n, t = (i = this.offsetTop(e)) + e.clientHeight, r >= i && t >= o
            }, r.prototype.util = function() {
                return null != this._util ? this._util : this._util = new t
            }, r.prototype.disabled = function() {
                return !this.config.mobile && this.util().isMobile(navigator.userAgent)
            }, r
        }()
    }.call(this);