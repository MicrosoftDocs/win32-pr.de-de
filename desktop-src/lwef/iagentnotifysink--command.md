---
title: Iagentnotifysink-Befehl
description: Iagentnotifysink-Befehl
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690d2914db9d284cd4ba4b826905d3169b83f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948677"
---
# <a name="iagentnotifysinkcommand"></a>Iagentnotifysink:: Command

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

Benachrichtigt eine Client Anwendung, dass ein [**Befehl**](/windows/desktop/lwef/the-command-object) vom Benutzer ausgewählt wurde.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwcommandid*
</dt> <dd>

Der Bezeichner der optimalen Übereinstimmungs-Befehls Alternativen.

</dd> <dt>

<span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkuserinput*
</dt> <dd>

Adresse der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle für das [**iagentuserinput**](iagentuserinput.md) -Objekt.

</dd> </dl>

Verwenden Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) , um die [**iagentuserinput**](iagentuserinput.md) -Schnittstelle abzurufen.

Der Server benachrichtigt den Eingabe aktiven Client, wenn der Benutzer einen Befehl per Stimme auswählt, oder indem er im Popup Menü des Zeichens einen Befehl auswählt. Das Ereignis tritt auch dann auf, wenn der Benutzer einen der Befehle des Servers auswählt. In diesem Fall gibt der Server eine NULL-Befehls-ID, die vertrauensbewertung und den von der Sprach-Engine für diesen Eintrag zurückgegebenen sprach Text zurück.

## <a name="see-also"></a>Weitere Informationen

[**Iagentuserinput**](iagentuserinput.md)


 

 