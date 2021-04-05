---
title: Iagentcharakteriex "einhalbpcontextid"
description: Iagentcharakteriex "einhalbpcontextid"
ms.assetid: 218e970e-825e-441d-8947-30ec6a2845bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500187bf04babbecf7577ff933dd0adcc53609f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708963"
---
# <a name="iagentcharacterexsethelpcontextid"></a>Iagentcharakteriex:: Setup Element-ID

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

Legt die [**HelpContextID**](helpcontextid-property.md) für das Zeichen fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulhelpid*
</dt> <dd>

Die Kontext Nummer des Hilfe Themas, das einem Zeichen zugeordnet ist. wird verwendet, um die kontextbezogene Hilfe für das Zeichen bereitzustellen.

</dd> </dl>

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und diese in der [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben, ruft der Microsoft-Agent automatisch Hilfe auf, wenn [**helpmadeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer das Zeichen auswählt. Wenn in [**HelpContextID**](helpcontextid-property.md)eine Kontext Nummer vorhanden ist, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird. Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für das Zeichen. Wenn in der **HelpContextID** -Eigenschaft eine Kontext Nummer vorhanden ist, wird in der Hilfe ein Thema angezeigt, das dem aktuellen Hilfe Kontext entspricht. Andernfalls wird "kein Hilfethema mit diesem Element verknüpft" angezeigt.

Diese Einstellung gilt nur, wenn die Client Anwendung der aktive Client des obersten Zeichens ist. Es wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen aus, die von der Client Anwendung verwendet werden.

> [!Note]  
> Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex:: gethelpcontextid**](iagentcharacterex--gethelpcontextid.md), [**iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Elementname, iagentcharakteriex: [**:**](iagentcharacterex--sethelpfilename.md) Setup Name


 

 




