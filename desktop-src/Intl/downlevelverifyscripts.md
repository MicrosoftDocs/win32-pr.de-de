---
description: Vergleicht zwei aufzählte Listen von Skripts.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: DownlevelVerifyScripts-Funktion (Idndl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: df0bdb1e8968d6bb044a3f270eb9200adf1ecaa54137fe3cface0e0898a9b5be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068240"
---
# <a name="downlevelverifyscripts-function"></a>DownlevelVerifyScripts-Funktion

Vergleicht zwei aufzählte Listen von Skripts.

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die auf vista-Windows ausgeführt werden. Die Verwendung erfordert das Downloadpaket. Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**VerifyScripts aufrufen.**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)

 

## <a name="syntax"></a>Syntax


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Flags, die Skriptüberprüfungsoptionen angeben.



| Wert                                                                                                                                                             | Bedeutung                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <dt>**VS \_ ALLOW \_ LATIN**</dt> </dl> | Lassen Sie "Latn" (lateinisches Skript) in der Testliste zu, auch wenn es sich nicht in der Liste des Locale befindet.<br/> |



 

</dd> <dt>

*lpLocaleScripts* \[ In\]
</dt> <dd>

Zeiger auf die Locale-Liste, die aufzählte Liste von Skripts für ein bestimmtes Locale. Diese Liste wird in der Regel durch Aufrufen von [**DownlevelGetLocaleScripts aufgefüllt.**](downlevelgetlocalescripts.md)

</dd> <dt>

*cchLocaleScripts* \[ In\]
</dt> <dd>

Größe der durch *lpLocaleScripts angegebenen Zeichenfolge* in Zeichen. Die Anwendung legt diesen Parameter auf -1 fest, wenn die Zeichenfolge null-terminiert ist. Wenn dieser Parameter auf 0 festgelegt ist, schlägt die Funktion fehl.

</dd> <dt>

*lpTestScripts* \[ In\]
</dt> <dd>

Zeiger auf die Testliste, eine zweite Liste von Skripts. Diese Liste wird in der Regel durch Aufrufen von [**DownlevelGetStringScripts aufgefüllt.**](downlevelgetstringscripts.md)

</dd> <dt>

*cchTestScripts* \[ In\]
</dt> <dd>

Größe der durch *lpTestScripts angegebenen Zeichenfolge* in Zeichen. Die Anwendung legt diesen Parameter auf -1 fest, wenn die Zeichenfolge null-terminiert ist. Wenn dieser Parameter auf 0 festgelegt ist, schlägt die Funktion fehl.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn die Testliste nicht leer ist und alle Elemente in der Liste ebenfalls in der Locale-Liste enthalten sind. Andernfalls gibt die Funktion **FALSE zurück.**

Der Rückgabewert **FALSE kann angeben,** dass die Testliste ein Element enthält, das nicht in der Locale-Liste enthalten ist, oder es kann auf einen Fehler hindeuten. Um zwischen diesen beiden Fällen zu unterscheiden, kann die Anwendung [**GetLastError aufrufen.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) Wenn **DownlevelVerifyScripts** erfolgreich ermittelt hat, dass in der Testliste ein Element enthalten ist, das nicht in der Liste mit dem Locale enthalten ist, gibt **GetLastError** ERROR \_ SUCCESS zurück. **Andernfalls kann GetLastError** einen der folgenden Fehlercodes zurückgeben:

-   FEHLER \_ \_ UNGÜLTIGE FLAGS. Die für Flags angegebenen Werte waren ungültig.
-   FEHLER \_ \_ UNGÜLTIGER PARAMETER. Jeder der Parameterwerte war ungültig.

## <a name="remarks"></a>Hinweise

Diese Funktion vergleicht Zeichenfolgen, z. B. "Latn; Cyrl;", die aus einer Reihe von Vier-Zeichen-Skriptnamen besteht, mit jedem Skriptnamen gefolgt von einem Semikolon. Es gibt auch einen Sonderfall, um die Tatsache zu berücksichtigen, dass das lateinische Skript häufig in Sprachen und Lokalen verwendet wird, für die es nicht nativ ist.

Diese Funktion ist im Rahmen einer Strategie zur Entschärfung von Sicherheitsproblemen im Zusammenhang mit internationalisierten Domänennamen [(IDNs) nützlich.](handling-internationalized-domain-names--idns.md)

Im Folgenden finden Sie Beispiele für die Rückgabe dieser Funktion und einen nachfolgenden Aufruf von [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in verschiedenen Szenarien. Die letzten beiden Beispiele veranschaulichen jeweils einen Fall, in dem die Testliste kein abschließendes Semikolon (falsch formatierte Zeichenfolge) und einen Fall fehlt, in dem die Testliste leer ist.



| "Locale"-Zeichenfolge | Zeichenfolge "Test" | *dwFlags*        | Rückgabewert | GetLastError-Rückgabe       |
|-----------------|---------------|------------------|--------------|---------------------------|
| Hani; Hira; Kana; | Hani;         | Nicht zutreffend              | **TRUE**     | Nicht zutreffend                       |
| Hani; Hira; Kana; | Hani; Latn;    | 0                | **FALSE**    | FEHLER \_ ERFOLGREICH            |
| Hani; Hira; Kana; | Hani; Latn;    | VS \_ ALLOW \_ LATIN | **TRUE**     | Nicht zutreffend                       |
| Hani; Hira; Kana; | Cyrl;         | Nicht zutreffend              | **FALSE**    | FEHLER \_ ERFOLGREICH            |
| Hani; Hira; Kana; | Cyrl;         | Nicht zutreffend              | **FALSE**    | FEHLER \_ UNGÜLTIGER \_ PARAMETER |
| Hani; Hira; Kana; |               | Nicht zutreffend              | **FALSE**    | FEHLER \_ ERFOLGREICH            |



 

Die erforderliche Headerdatei und DLL sind Teil des Downloads ["Microsoft Internationalized Domain Name (IDN)-Entschärfungs-APIs",](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) der im [MSDN Download Center verfügbar ist.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                                                         |
| Verteilbare Komponente<br/>          | Microsoft Internationalized Domain Name (IDN) Mitigation APIs onWindows XP with SP2,Windows Server 2003 with SP1 oderWindows Vista<br/> |
| Header<br/>                   | <dl> <dt>Idndl.h</dt> </dl>                                                           |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Unterstützung der Landessprache](national-language-support.md)
</dt> <dt>

[Unterstützungsfunktionen für nationale Sprachen](national-language-support-functions.md)
</dt> <dt>

[Behandeln von internationalisierten Domänennamen (IDNs)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
