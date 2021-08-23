---
description: Die ParserAutoInstallInfo-Exportfunktion identifiziert den Parser oder Parser, die sich in einer DLL befinden. ParserAutoInstallInfo sollte in allen Parser-DLLs implementiert werden.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: ParserAutoInstallInfo-Rückruffunktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3c6c69b66f3ff92905333a28c5dadfd79290033f0abb68cb2a790f07c6e34412
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063750"
---
# <a name="parserautoinstallinfo-callback-function"></a>ParserAutoInstallInfo-Rückruffunktion

Die **ParserAutoInstallInfo-Exportfunktion** identifiziert den Parser oder Parser, die sich in einer DLL befinden. **ParserAutoInstallInfo** sollte in allen Parser-DLLs implementiert werden.

## <a name="syntax"></a>Syntax


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a>Parameter

Diese Rückruffunktion verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert eine [PF \_ PARSERDLLINFO-Struktur,](pf-parserdllinfo.md) die die Parser in der DLL beschreibt.

Wenn die Funktion nicht erfolgreich ist, lautet der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Wenn Netzwerkmonitor zum ersten Mal geladen wird, ruft es **ParserAutoInstallInfo** auf (sofern vorhanden), um jeden Parser automatisch zu installieren, und listet dann alle Parser-DLLs im Parser-Unterverzeichnis auf.

Die in der **PF \_ PARSERDLLINFO-Struktur** zurückgegebenen Informationen umfassen Folgendes:

-   Die Anzahl der Parser in der DLL (in der Regel eins).
-   Der Name und eine kurze Beschreibung des Protokolls, das jeder Parser erkennt.
-   Eine optionale Hilfedatei für jedes Protokoll.
-   Die Protokolle, die jedem Protokoll vorangestellt sind.
-   Die Protokolle, die den einzelnen Protokollen folgen.

Jede Parser-DLL sollte einen Parser enthalten. Mit Netzwerkmonitor können Sie jedoch eine DLL erstellen, die mehr als einen Parser enthält. Beispielsweise ist tcpip.dll eine Netzwerkmonitor DLL mit mehreren Parsern.



| Für Informationen zu                                               | Siehe                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Was Parser sind und wie sie mit Netzwerkmonitor arbeiten.        | [Parser](parsers.md)                                                       |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.               | [Parser-DLL-Architektur](parser-dll-architecture.md)                       |
| Die Implementierung von **ParserAutoInstallInfo**  enthält ein Beispiel. | [Implementieren von ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[PF \_ PARSERDLLINFO](pf-parserdllinfo.md)
</dt> </dl>

 

 




