---
title: IAgentCharacterEx GetHelpContextID
description: IAgentCharacterEx GetHelpContextID
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3a64de0f4373bcaa890156ec88595d066aae9ae84b5b242fe62ffae10479d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750795"
---
# <a name="iagentcharacterexgethelpcontextid"></a>IAgentCharacterEx::GetHelpContextID

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

Ruft die [**HelpContextID für**](helpcontextid-property.md) das Zeichen ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*
</dt> <dd>

Adresse einer Variablen, die die Kontextnummer des Hilfethemas für das Zeichen empfängt.

</dd> </dl>

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile-Eigenschaft**](helpfile-property.md) des Zeichens festgelegt haben, ruft Microsoft Agent automatisch Help auf, wenn [**HelpModeOn**](helpmodeon-property.md) auf True festgelegt ist und der Benutzer das Zeichen auswählt.  Wenn die [**HelpContextID**](helpcontextid-property.md)eine Kontextnummer enthält, ruft der -Agent die Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontextnummer identifiziert wird. Die aktuelle Kontextnummer ist der Wert von **HelpContextID** für das Zeichen.

**IAgentCharacterEx::GetHelpContextID gibt** die [**HelpContextID**](helpcontextid-property.md) zurück, die Sie für das Zeichen festgelegt haben. Die von anderen Clients **festgelegte HelpContextID** wird nicht zurückgeben.

> [!Note]  
> Zum Erstellen einer Hilfedatei ist der Microsoft Windows Help Compiler erforderlich.

 

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




