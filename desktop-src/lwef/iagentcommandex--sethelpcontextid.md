---
title: IAgentCommandEx SetHelpContextID
description: IAgentCommandEx SetHelpContextID
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b876276d42ff07081b60194e90beff3ad9ef19fec383c50d70a551e1c9a5e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750191"
---
# <a name="iagentcommandexsethelpcontextid"></a>IAgentCommandEx::SetHelpContextID

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

Legt die [**HelpContextID**](helpcontextid-property-com.md) für ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*
</dt> <dd>

Die Kontextnummer des Hilfethemas, das dem [**Command-Objekt**](/windows/desktop/lwef/the-command-object) zugeordnet ist. wird verwendet, um kontextbezogene Hilfe für den Befehl bereitzustellen.

</dd> </dl>

Wenn Sie eine Windows Hilfedatei für Ihre Anwendung erstellt und in der [**HelpFile-Eigenschaft**](helpfile-property.md) des Zeichens festgelegt haben. Der Microsoft-Agent ruft die Hilfe automatisch auf, wenn [**HelpModeOn**](helpmodeon-property.md) auf **True** festgelegt ist und der Benutzer den Befehl auswählt. Wenn die [**HelpContextID**](helpcontextid-property-com.md)eine Kontextnummer enthält, ruft der -Agent die Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontextnummer identifiziert wird. Die aktuelle Kontextnummer ist der Wert von **HelpContextID** für den Befehl.

> [!Note]  
> Zum Erstellen einer Hilfedatei ist der Microsoft Windows Help Compiler erforderlich.

 

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandEx::GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 