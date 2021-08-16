---
description: Vergleicht zwei Unicode-Zeichenfolgen unter Verwendung eines angegebenen Locale.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: CompareStringWrapW-Funktion
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
ms.openlocfilehash: 9fe05c354aaa901d87c77ba04eecd5dc4efd925d77bdeaf5387a137d85b27348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861511"
---
# <a name="comparestringwrapw-function"></a>CompareStringWrapW-Funktion

\[**CompareStringWrapW** ist für die Verwendung in Windows XP verfügbar. Sie ist in nachfolgenden Versionen nicht verfügbar. Verwenden Sie [**an seiner Stelle CompareStringW.**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)\]

Vergleicht zwei Unicode-Zeichenfolgen unter Verwendung eines angegebenen Locale.

> [!Note]  
> **CompareStringWrapW** ist ein Wrapper für die **CompareStringW-Funktion.** Weitere Hinweise zur Verwendung finden Sie auf der Seite [**CompareString.**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)

 

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

*Locale* \[ In\]
</dt> <dd>

Typ: **LCID**

Ein für den Vergleich verwendeter Locale Identifier. Dieser Parameter kann einer der folgenden vordefinierten Locale Identifiers oder ein vom [**MAKELCID-Makro**](/windows/win32/api/winnt/nf-winnt-makelcid) erstellter Locale Identifier sein.

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**LOCALE \_ SYSTEM \_ DEFAULT**


</dt> <dd>

Das Standard-Locale des Systems.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**LOCALE \_ USER \_ DEFAULT**


</dt> <dd>

Das Standard-Locale des aktuellen Benutzers.

</dd> </dl> </dd> <dt>

*dwCmpFlags* \[ In\]
</dt> <dd>

Typ: **DWORD**

Die Flags, die angeben, wie die Funktion die beiden Zeichenfolgen vergleicht. Standardmäßig sind diese Flags nicht festgelegt. Legen Sie auf 0 fest, um das Standardverhalten oder eine beliebige Kombination der folgenden Werte zu erhalten.

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**NORM \_ IGNORECASE**


</dt> <dd>

Ignorieren Der Fall.

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**NORM \_ IGNOREKANATYPE**


</dt> <dd>

Unterscheiden Sie nicht zwischen Hiragana- und Katakana-Zeichen. Die entsprechenden Hiragana- und Katakana-Zeichen werden als gleich verglichen.

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**NORM \_ IGNORENONSPACE**


</dt> <dd>

Ignorieren Sie zeichenfreie Zeichen.

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**NORM \_ IGNORESYMBOLS**


</dt> <dd>

Symbole ignorieren.

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**NORM \_ IGNOREWIDTH**


</dt> <dd>

Unterscheiden Sie nicht zwischen einem Einzel bytezeichen und demselben Zeichen wie ein Doppel bytezeichen.

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**SORT \_ STRINGSORT**


</dt> <dd>

Behandeln Sie Interpunktion wie Symbole.

</dd> </dl> </dd> <dt>

*lpString1* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf die erste zu vergleichende Unicode-Zeichenfolge.

</dd> <dt>

*cchCount1* \[ In\]
</dt> <dd>

Typ: **int**

Die Anzahl der Zeichen in der Zeichenfolge, auf die der *lpString1-Parameter* zeigt. Die Anzahl schließt das beendende NULL-Zeichen nicht ein. Wenn dieser Parameter ein negativer Wert ist, wird davon ausgegangen, dass die Zeichenfolge null-terminiert ist, und die Länge wird automatisch berechnet.

</dd> <dt>

*lpString2* \[ In\]
</dt> <dd>

Typ: **LPCWSTR**

Ein Zeiger auf die zweite zu vergleichende Unicode-Zeichenfolge.

</dd> <dt>

*cchCount2* \[ In\]
</dt> <dd>

Typ: **int**

Die Anzahl der Zeichen in der Zeichenfolge, auf die der *lpString2-Parameter* zeigt. Die Anzahl schließt das beendende NULL-Zeichen nicht ein. Wenn dieser Parameter ein negativer Wert ist, wird davon ausgegangen, dass die Zeichenfolge null-terminiert ist, und die Länge wird automatisch berechnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf. **GetLastError** gibt möglicherweise einen der folgenden Fehlercodes zurück.

-   FEHLER \_ \_ UNGÜLTIGE FLAGS
-   FEHLER \_ UNGÜLTIGER \_ PARAMETER

Wenn die Funktion erfolgreich ist, ist der Rückgabewert einer der folgenden Werte. 

| Anforderung | Wert |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| CSTR \_ KLEINER \_ ALS    | Die Zeichenfolge, auf die der *lpString1-Parameter* zeigt, ist weniger lexikalisch als die Zeichenfolge, auf die der *lpString2-Parameter* zeigt. |
| CSTR \_ EQUAL         | Die Zeichenfolge, auf die *lpString1* zeigt, entspricht im lexikalischen Wert der Zeichenfolge, auf die *lpString2 zeigt.*                              |
| CSTR \_ GREATER \_ THAN | Die Zeichenfolge, auf die *lpString1* zeigt, ist im lexikalischen Wert größer als die Zeichenfolge, auf die *lpString2 zeigt.*                           |



 

## <a name="remarks"></a>Hinweise

**Sicherheitswarnung:** Die falsche Verwendung dieser Funktion kann die Sicherheit Ihrer Anwendung gefährden. Zeichenfolgen, die nicht ordnungsgemäß verglichen werden, können ungültige Eingaben erzeugen. Testen Sie Zeichenfolgen, um sicherzustellen, dass sie gültig sind, bevor Sie sie verwenden, und stellen Sie Fehlerhandler zur Verfügung. Weitere Informationen finden Sie unter [Sicherheitsüberlegungen: Internationale Features.](../intl/security-considerations--international-features.md)

Die bevorzugte Methode ist die Verwendung [**von CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) in Verbindung mit microsoft Layer for Unicode (MSLU).

**CompareStringWrapW** muss mithilfe der Ordnungszahl 45 direkt Shlwapi.dll aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Keine</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
