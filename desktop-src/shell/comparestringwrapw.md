---
description: Vergleicht zwei Unicode-Zeichen folgen unter Verwendung eines angegebenen Gebiets Schemas.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: Comparestringwrapw-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 0731182f5c01ad56db722972628d2cbe39373835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977384"
---
# <a name="comparestringwrapw-function"></a>Comparestringwrapw-Funktion

\[**Comparestringwrapw** ist für die Verwendung in Windows XP verfügbar. Sie wird in nachfolgenden Versionen nicht verfügbar sein. Sie sollten [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) an seiner Stelle verwenden.\]

Vergleicht zwei Unicode-Zeichen folgen unter Verwendung eines angegebenen Gebiets Schemas.

> [!Note]  
> **Comparestringwrapw** ist ein Wrapper für die **CompareStringW** -Funktion. Weitere Hinweise zur Verwendung finden Sie auf der Seite " [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ".

 

## <a name="syntax"></a>Syntax


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gebiets Schema  \[ in\]
</dt> <dd>

Typ: **LCID**

Ein für den Vergleich verwendeter Gebiets Schema Bezeichner. Dieser Parameter kann einer der folgenden vordefinierten Gebiets Schema Bezeichner oder ein Gebiets Schema Bezeichner sein, der vom [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) -Makro erstellt wurde.

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**Standard für Gebiets Schema \_ System \_**


</dt> <dd>

Das Standard Gebiets Schema des Systems.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**\_Standardbenutzer Name für locale \_**


</dt> <dd>

Das Standard Gebiets Schema des aktuellen Benutzers.

</dd> </dl> </dd> <dt>

*dwcmpflags* \[ in\]
</dt> <dd>

Typ: **DWORD**

Die Flags, die angeben, wie die Funktion die beiden Zeichen folgen vergleicht. Standardmäßig sind diese Flags nicht festgelegt. Legen Sie den Wert auf NULL fest, um das Standardverhalten oder eine beliebige Kombination der folgenden Werte zu erhalten.

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**Norm \_ ignoreCase**


</dt> <dd>

Fall ignorieren.

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**Norm \_ IgnoreKanaType**


</dt> <dd>

Unterscheiden Sie nicht zwischen Hiragana-und Katakana-Zeichen. Die entsprechenden Hiragana-und Katakana-Zeichen vergleichen als gleich.

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**Norm \_ ignoronspace**


</dt> <dd>

Zeichen ohne zwischen Raum ignorieren.

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**Norm \_ IgnoreSymbols**


</dt> <dd>

Symbole ignorieren.

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**Norm \_ IgnoreWidth**


</dt> <dd>

Unterscheiden Sie nicht zwischen einem Einzel Byte Zeichen und demselben Zeichen als Doppelbyte Zeichen.

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**\_StringSort sortieren**


</dt> <dd>

Interpunktions Zeichen werden wie Symbole behandelt.

</dd> </dl> </dd> <dt>

*lpString1* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf die erste zu vergleichende Unicode-Zeichenfolge.

</dd> <dt>

*cchCount1* \[ in\]
</dt> <dd>

Typ: **int**

Die Anzahl der Zeichen in der Zeichenfolge, auf die durch den *lpString1* -Parameter verwiesen wird. Der Zähler umfasst nicht das abschließende Null Zeichen. Wenn dieser Parameter ein negativer Wert ist, wird angenommen, dass die Zeichenfolge mit NULL endet, und die Länge wird automatisch berechnet.

</dd> <dt>

*lpString2* \[ in\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.

</dd> <dt>

*cchCount2* \[ in\]
</dt> <dd>

Typ: **int**

Die Anzahl der Zeichen in der Zeichenfolge, auf die durch den *lpString2* -Parameter verwiesen wird. Der Zähler umfasst nicht das abschließende Null Zeichen. Wenn dieser Parameter ein negativer Wert ist, wird angenommen, dass die Zeichenfolge mit NULL endet, und die Länge wird automatisch berechnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf. " **GetLastError** " kann einen der folgenden Fehlercodes zurückgeben.

-   \_ungültige \_ Flags.
-   Fehler bei \_ ungültigem \_ Parameter

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert einer der folgenden Werte. 

| Anforderung | Wert |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| CStr \_ kleiner \_ als    | Die Zeichenfolge, auf die der *lpString1* -Parameter verweist, ist weniger lexikalischer Wert als die Zeichenfolge, auf die der *lpString2* -Parameter verweist. |
| CStr \_ gleich         | Die Zeichenfolge, auf die von *lpString1* verwiesen wird, ist gleich dem lexikalischen Wert der Zeichenfolge, auf die von *lpString2* verwiesen wird.                              |
| CStr \_ größer \_ als | Die Zeichenfolge, auf die von *lpString1* verwiesen wird, ist im lexikalischen Wert größer als die Zeichenfolge, auf die *lpString2*                           |



 

## <a name="remarks"></a>Bemerkungen

**Sicherheitswarnung:** Wenn Sie diese Funktion falsch verwenden, kann die Sicherheit Ihrer Anwendung beeinträchtigt werden. Zeichen folgen, die nicht ordnungsgemäß verglichen werden, können ungültige Eingaben verursachen. Testen Sie Zeichen folgen, um sicherzustellen, dass Sie gültig sind, bevor Sie Sie verwenden und Fehlerhandler bereitstellen. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features](../intl/security-considerations--international-features.md)

Die bevorzugte Methode ist die Verwendung von [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in Verbindung mit der Microsoft-Schicht für Unicode (MSLU).

**Comparestringwrapw** muss direkt aus Shlwapi.dll aufgerufen werden. dabei wird die Ordnungszahl 45 verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>None</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
