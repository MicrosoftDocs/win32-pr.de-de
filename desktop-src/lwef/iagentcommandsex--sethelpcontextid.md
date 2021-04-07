---
title: Iagentcommandsex * thelpcontextid
description: Iagentcommandsex * thelpcontextid
ms.assetid: b49d8184-f8dd-4359-9d45-3f038af18da5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ed692185adbd60a73085b367b30b14fb646ab6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725921"
---
# <a name="iagentcommandsexsethelpcontextid"></a>Iagentcommandsex:: Setup Element-ID

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

Legt die [**HelpContextID**](helpcontextid-property.md) für ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulhelpid*
</dt> <dd>

Die Kontext Nummer des Hilfe Themas, das dem [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt zugeordnet ist. wird verwendet, um kontextbezogene Hilfe für den Befehl bereitzustellen.

</dd> </dl>

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und diese in der [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben. Der-Agent ruft automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer den Befehl auswählt. Wenn in [**HelpContextID**](helpcontextid-property.md)eine Kontext Nummer vorhanden ist, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird. Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für den Befehl. Wenn in der **HelpContextID** -Eigenschaft des ausgewählten Befehls eine Kontext Nummer vorhanden ist, wird in der Hilfe ein Thema angezeigt, das dem aktuellen Hilfe Kontext entspricht. Andernfalls wird "kein Hilfethema mit diesem Element verknüpft" angezeigt.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

> [!Note]  
> Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandsex:: gethelpcontextid**](iagentcommandsex--gethelpcontextid.md), [**iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Elementname, [**iagentcharakteriex::**](iagentcharacterex--sethelpfilename.md) Setup Name


 

 