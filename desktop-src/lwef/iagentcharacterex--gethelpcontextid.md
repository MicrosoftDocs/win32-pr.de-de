---
title: Iagentcharakteriex gethelpcontextid
description: Iagentcharakteriex gethelpcontextid
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfec03a217745838b88a592433defae01529ed50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713181"
---
# <a name="iagentcharacterexgethelpcontextid"></a>Iagentcharakteriex:: gethelpcontextid

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

Ruft [**HelpContextID**](helpcontextid-property.md) für das Zeichen ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulhelpid*
</dt> <dd>

Adresse einer Variablen, die die Kontext Nummer des Hilfe Themas für das Zeichen empfängt.

</dd> </dl>

Wenn Sie eine Windows-Hilfedatei für Ihre Anwendung erstellt und die [**HelpFile**](helpfile-property.md) -Eigenschaft des Zeichens festgelegt haben, ruft der Microsoft-Agent automatisch die Hilfe auf, wenn [**helpmudeon**](helpmodeon-property.md) auf **true** festgelegt ist und der Benutzer das Zeichen auswählt. Wenn in [**HelpContextID**](helpcontextid-property.md)eine Kontext Nummer vorhanden ist, ruft der-Agent Hilfe auf und sucht nach dem Thema, das durch die aktuelle Kontext Nummer identifiziert wird. Die aktuelle Kontext Nummer ist der Wert von **HelpContextID** für das Zeichen.

**Iagentcharakteriex:: gethelpcontextid** gibt die [**HelpContextID**](helpcontextid-property.md) zurück, die Sie für das Zeichen festgelegt haben. Die von anderen Clients festgelegte **HelpContextID** wird nicht zurückgegeben.

> [!Note]  
> Das Entwickeln einer Hilfedatei erfordert den Microsoft Windows Help Compiler.

 

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex::**](iagentcharacterex--sethelpcontextid.md)Setup Element-ID, [**iagentcharakteriex::**](iagentcharacterex--sethelpmodeon.md)Setup Elementname, iagentcharakteriex: [**:**](iagentcharacterex--sethelpfilename.md) Setup Name


 

 




