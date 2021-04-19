---
description: Vergleicht zwei aufgelistete Listen von Skripts.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: Downlevelverifyscripts-Funktion (idndl. h)
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
ms.openlocfilehash: 62e029576d53109e3c57faf4ec913472f8aea65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364190"
---
# <a name="downlevelverifyscripts-function"></a>Downlevelverifyscripts-Funktion

Vergleicht zwei aufgelistete Listen von Skripts.

> [!Note]  
> Diese Funktion wird nur von Anwendungen verwendet, die auf Betriebssystemen vor Windows Vista ausgeführt werden. Die Verwendung von erfordert das Downloadpaket. Anwendungen, die nur unter Windows Vista und höher ausgeführt werden, sollten [**verifyscripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)aufruft.

 

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

*dwFlags* \[ in\]
</dt> <dd>

Flags, die Optionen für die Skript Überprüfung angeben.



| Wert                                                                                                                                                             | Bedeutung                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <dt>**VS \_ Allow \_ Latin**</dt> </dl> | Lassen Sie "Latn" (lateinische Skripts) in der Testliste zu, auch wenn Sie sich nicht in der Liste der Gebiets Schemas befinden.<br/> |



 

</dd> <dt>

*lplocalescripts* \[ in\]
</dt> <dd>

Zeiger auf die Liste der Gebiets Schemas, die Aufzählungs Liste der Skripts für ein bestimmtes Gebiets Schema. Diese Liste wird in der Regel durch Aufrufen von [**downlevelgetlocalescripts**](downlevelgetlocalescripts.md)aufgefüllt.

</dd> <dt>

*cchlocalescripts* \[ in\]
</dt> <dd>

Die Größe (in Zeichen) der Zeichenfolge, die von *lplocalescripts* angegeben wird. Die Anwendung legt diesen Parameter auf-1 fest, wenn die Zeichenfolge NULL-terminiert ist. Wenn dieser Parameter auf 0 festgelegt ist, schlägt die Funktion fehl.

</dd> <dt>

*lptestscripts* \[ in\]
</dt> <dd>

Zeiger auf die Testliste, eine zweite aufgelistete Liste von Skripts. Diese Liste wird in der Regel durch Aufrufen von [**downlevelgetstringscripts**](downlevelgetstringscripts.md)aufgefüllt.

</dd> <dt>

*cchtestscripts* \[ in\]
</dt> <dd>

Die Größe (in Zeichen) der Zeichenfolge, die von *lptestscripts* angegeben wird. Die Anwendung legt diesen Parameter auf-1 fest, wenn die Zeichenfolge NULL-terminiert ist. Wenn dieser Parameter auf 0 festgelegt ist, schlägt die Funktion fehl.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn die Testliste nicht leer ist und alle Elemente in der Liste auch in der Liste der Gebiets Schemas enthalten sind. Andernfalls gibt die Funktion **false** zurück.

Der Rückgabewert **false** kann darauf hindeuten, dass die Testliste ein Element enthält, das nicht in der Liste der Gebiets Schemas enthalten ist, oder es kann auf einen Fehler hinweisen. Um zwischen diesen beiden Fällen zu unterscheiden, kann die Anwendung [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)aufrufen. Wenn **downlevelverifyscripts** erfolgreich festgestellt hat, dass ein Element in der Testliste vorhanden ist, das nicht in der Liste der Gebiets Schemas enthalten ist, gibt **GetLastError** den Fehler \_ Erfolg zurück. Andernfalls kann **GetLastError** einen der folgenden Fehlercodes zurückgeben:

-   \_ungültige \_ Flags. Die für Flags angegebenen Werte waren ungültig.
-   Fehler \_ : Ungültiger \_ Parameter. Jeder Parameterwert war ungültig.

## <a name="remarks"></a>Bemerkungen

Diese Funktion vergleicht Zeichen folgen, z. b. "Latn;". Cyrl; ", die aus einer Reihe von 4-Zeichen-Skriptnamen bestehen, wobei jeder Skript Name auf ein Semikolon folgt. Es gilt auch für einen besonderen Fall, dass das lateinische Skript häufig in Sprachen und Gebiets Schemas verwendet wird, für die es nicht nativ ist.

Diese Funktion ist als Teil einer Strategie zum mindern von Sicherheitsproblemen im Zusammenhang mit [internationalisierten Domänen Namen (IDNs)](handling-internationalized-domain-names--idns.md)nützlich.

Im folgenden finden Sie Beispiele für die Rückgabe dieser Funktion und einen nachfolgenden Rückruf von [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) in verschiedenen Szenarien. In den letzten beiden Beispielen wird ein Fall veranschaulicht, in dem die Testliste ein abschließendes Semikolon (falsch formatierte Zeichenfolge) und einen Fall, in dem die Testliste leer ist, fehlt.



| "Locale"-Zeichenfolge | "Test"-Zeichenfolge | *dwFlags*        | Rückgabewert | GetLastError-Rückgabe       |
|-----------------|---------------|------------------|--------------|---------------------------|
| Han Hira; Betrieben | Han         | –              | **TRUE**     | –                       |
| Han Hira; Betrieben | Han Latn    | 0                | **FALSE**    | Fehler \_ erfolgreich            |
| Han Hira; Betrieben | Han Latn    | VS \_ Allow \_ Latin | **TRUE**     | –                       |
| Han Hira; Betrieben | Cyrl;         | –              | **FALSE**    | Fehler \_ erfolgreich            |
| Han Hira; Betrieben | Cyrl;         | –              | **FALSE**    | Fehler bei \_ ungültigem \_ Parameter |
| Han Hira; Betrieben |               | –              | **FALSE**    | Fehler \_ erfolgreich            |



 

Die erforderliche Header Datei und dll sind Teil des Downloads ["Microsoft Internationalized Domain Name (IDN) Entschärfungs-APIs"](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , der im [MSDN Download Center](https://www.microsoft.com/?ref=go)verfügbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                                                         |
| Verteilbare Komponente<br/>          | Microsoft Internationalized Domain Name (IDN) Entschärfungs-APIs onwindows XP mit SP2, Windows Server 2003 mit SP1, orwindows Vista<br/> |
| Header<br/>                   | <dl> <dt>Idndl. h</dt> </dl>                                                           |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Unterstützung für nationale Sprache](national-language-support.md)
</dt> <dt>

[Funktionen zur Unterstützung der Landessprache](national-language-support-functions.md)
</dt> <dt>

[Umgang mit internationalisierten Domänen Namen (IDNs)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**Downlevelgetlocalescripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**Downlevelgetstringscripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**Verifyscripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
