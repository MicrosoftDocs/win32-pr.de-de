---
title: Iagentcommandsex setdefaultid
description: Iagentcommandsex setdefaultid
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390219"
---
# <a name="iagentcommandsexsetdefaultid"></a>Iagentcommandsex:: setdefaultid

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

Legt die ID des Standard Befehls in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

Die ID für den [**Befehl**](/windows/desktop/lwef/the-command-object) , der als Standard festgelegt werden soll.

</dd> </dl>

Diese Eigenschaft legt das Standard [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt fest, das in der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung festgelegt ist. Der Standardbefehl ist im Popupmenü des Zeichens fett formatiert. Wenn Sie jedoch den Standardbefehl festlegen, werden die Befehle zur Behandlung von Befehlen oder zum Doppelklicken nicht tatsächlich geändert.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandsex:: getdefaultid**](iagentcommandsex--getdefaultid.md)


 

 