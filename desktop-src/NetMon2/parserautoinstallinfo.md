---
description: Die parserautoinstallinfo-Exportfunktion identifiziert den Parser oder Parser, die sich in einer DLL befinden. Parserautoinstallinfo sollte in allen Parser-DLLs implementiert werden.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: "\"Parameserautoinstallinfo\"-Rückruffunktion (Netmon. h)"
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
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342739"
---
# <a name="parserautoinstallinfo-callback-function"></a>Parameserautoinstallinfo-Rückruffunktion

Die **parserautoinstallinfo** -Exportfunktion identifiziert den Parser oder Parser, die sich in einer DLL befinden. **Parserautoinstallinfo** sollte in allen Parser-DLLs implementiert werden.

## <a name="syntax"></a>Syntax


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a>Parameter

Diese Rückruffunktion hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert eine [PF- \_ parametedllinfo](pf-parserdllinfo.md) -Struktur, die die Parser in der dll beschreibt.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Wenn Netzwerkmonitor zum ersten Mal geladen wird, wird **parserautoinstallinfo** aufgerufen (sofern vorhanden), um jeden Parser automatisch zu installieren, und anschließend werden alle parserdlls im Parser-Unterverzeichnis aufgelistet.

Zu den Informationen, die in der **PF-parametdllinfo \_** -Struktur zurückgegeben werden, gehören folgende:

-   Die Anzahl der Parser in der dll (in der Regel eine).
-   Der Name und eine kurze Beschreibung des Protokolls, das jeder Parser erkennt.
-   Eine optionale Hilfedatei für jedes Protokoll.
-   Die Protokolle, die jedem Protokoll vorangestellt sind.
-   Die Protokolle, die auf die einzelnen Protokolle folgen.

Jede Parser-DLL sollte einen Parser enthalten. Netzwerkmonitor ermöglicht es Ihnen jedoch, eine DLL zu erstellen, die mehr als einen Parser enthält. Beispielsweise ist tcpip.dll eine Netzwerkmonitor-dll mit mehr als einem Parser.



| Für Informationen zu                                               | Siehe                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.        | [Parser](parsers.md)                                                       |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.               | [Architektur der Parser-DLL](parser-dll-architecture.md)                       |
| Zum Implementieren von " **Parser autoinstallinfo**  " ist ein Beispiel enthalten. | [Implementieren von "parameserautoinstallinfo"](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[PF- \_ Parser (Parser)](pf-parserdllinfo.md)
</dt> </dl>

 

 




