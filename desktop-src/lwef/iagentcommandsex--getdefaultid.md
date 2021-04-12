---
title: Iagentcommandsex getdefaultid
description: Iagentcommandsex getdefaultid
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4380eca62a65758979a94fb23511348b11acdf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390316"
---
# <a name="iagentcommandsexgetdefaultid"></a>Iagentcommandsex:: getdefaultid

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

Ruft die ID des Standard Befehls in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwid*
</dt> <dd>

Adresse einer Variablen, die die ID des [**Befehls**](/windows/desktop/lwef/the-command-object) Satzes als Standardwert empfängt.

</dd> </dl>

Diese Eigenschaft gibt das aktuelle Standard [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt in der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung zurück. Der Standardbefehl ist im Popupmenü des Zeichens fett formatiert. Wenn Sie jedoch den Standardbefehl festlegen, werden die Befehle zur Behandlung von Befehlen oder zum Doppelklicken nicht geändert.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandsex:: setdefaultid**](iagentcommandsex--setdefaultid.md)


 

 