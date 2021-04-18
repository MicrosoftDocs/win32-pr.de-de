---
title: Iagentcommands getcaption
description: Iagentcommands getcaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f886413ae6bfbfe104306d7280d8c66b08bf311a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340897"
---
# <a name="iagentcommandsgetcaption"></a>Iagentcommands:: getcaption

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

Ruft die [**Beschriftung**](caption-property.md) für eine [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszcaption*
</dt> <dd>

Die Adresse eines BSTR-Werts, der den Wert der über [**Schrift**](caption-property.md) Texteinstellung empfängt, der für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angezeigt wird.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommands:: setCaption**](iagentcommands--setcaption.md), [**iagentcommands:: getVisible**](iagentcommands--getvisible.md), [**iagentcommands:: getvoice**](iagentcommands--getvoice.md)


 

 