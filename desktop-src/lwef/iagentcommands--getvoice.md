---
title: Iagentcommands getvoice
description: Iagentcommands getvoice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1915512c89611267df3788e5dcaa84fb0874a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390317"
---
# <a name="iagentcommandsgetvoice"></a>Iagentcommands:: getvoice

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

Ruft den Wert der [**Voice**](voice-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszvoice*
</dt> <dd>

Die Adresse eines BSTR-Werts, der den Wert der [**sprach**](voice-property.md) Texteinstellung für eine [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommands:: setvoice**](iagentcommands--setvoice.md), [**iagentcommands:: getcaption**](iagentcommands--getcaption.md), [**iagentcommands:: getVisible**](iagentcommands--getvisible.md)


 

 