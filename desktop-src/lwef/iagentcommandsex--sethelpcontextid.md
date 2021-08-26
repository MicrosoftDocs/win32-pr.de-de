---
title: IAgentCommandsEx SetHelpContextID
description: IAgentCommandsEx SetHelpContextID
ms.assetid: b49d8184-f8dd-4359-9d45-3f038af18da5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e4ff5941d9f120c42cb2fa17d93a4f2a0c23e89d61dbee078b3ab5c3ffe611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888240"
---
# <a name="iagentcommandsexsethelpcontextid"></a>IAgentCommandsEx::SetHelpContextID

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

Legt die [**HelpContextID**](helpcontextid-property.md) für ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Die Kontextnummer des Hilfethemas, das dem [**Command-Objekt**](/windows/desktop/lwef/the-command-object) zugeordnet ist. wird verwendet, um kontextbezogene Hilfe für den Befehl bereitzustellen.

</dd> </dl>

Wenn Sie eine Windows Hilfedatei für Ihre Anwendung erstellt und in der [**HelpFile-Eigenschaft**](helpfile-property.md) des Zeichens festgelegt haben. Der Agent ruft die Hilfe automatisch auf, wenn [**HelpModeOn**](helpmodeon-property.md) auf **True** festgelegt ist und der Benutzer den Befehl auswählt. Wenn die [**HelpContextID**](helpcontextid-property.md)eine Kontextnummer enthält, ruft der -Agent die Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontextnummer identifiziert wird. Die aktuelle Kontextnummer ist der Wert von **HelpContextID** für den Befehl. Wenn die **HelpContextID-Eigenschaft** des ausgewählten Befehls eine Kontextnummer enthält, zeigt die Hilfe ein Thema an, das dem aktuellen Hilfekontext entspricht. Andernfalls wird "Diesem Element ist kein Hilfethema zugeordnet" angezeigt.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

> [!Note]  
> Zum Erstellen einer Hilfedatei ist der Microsoft Windows Help Compiler erforderlich.

 

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandsEx::GetHelpContextID**](iagentcommandsex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 