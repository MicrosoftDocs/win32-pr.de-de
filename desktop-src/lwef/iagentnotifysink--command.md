---
title: IAgentNotifySink-Befehl
description: IAgentNotifySink-Befehl
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d9c20de96c1bb14cf003ad7beff98e716e272ad3de39532d9b455e279d97af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105202"
---
# <a name="iagentnotifysinkcommand"></a>IAgentNotifySink::Command

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

Benachrichtigt eine Clientanwendung, dass vom Benutzer ein [**Befehl**](/windows/desktop/lwef/the-command-object) ausgewählt wurde.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Bezeichner der Befehlsalternative für die beste Übereinstimmung.

</dd> <dt>

<span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punUserInput*
</dt> <dd>

Adresse der [**IUnknown-Schnittstelle**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) für das [**IAgentUserInput-Objekt.**](iagentuserinput.md)

</dd> </dl>

Verwenden Sie [**QueryInterface,**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) um die [**IAgentUserInput-Schnittstelle**](iagentuserinput.md) abzurufen.

Der Server benachrichtigt den eingabeaktiven Client, wenn der Benutzer einen Befehl per Stimme oder durch Auswählen eines Befehls im Popupmenü des Zeichens auswählt. Das Ereignis tritt auch dann auf, wenn der Benutzer einen der Serverbefehle auswählt. In diesem Fall gibt der Server eine NULL-Befehls-ID, die Zuverlässigkeitsbewertung und den Sprachtext zurück, der von der Sprach-Engine für diesen Eintrag zurückgegeben wird.

## <a name="see-also"></a>Weitere Informationen

[**IAgentUserInput**](iagentuserinput.md)


 

 