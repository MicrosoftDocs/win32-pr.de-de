---
title: Iagentcommands getVisible
description: Iagentcommands getVisible
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853a47f6136779415a08adc3c891d9b5cc95dcca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338660"
---
# <a name="iagentcommandsgetvisible"></a>Iagentcommands:: getVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

Ruft den Wert der [**Visible**](visible-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbvisible*
</dt> <dd>

Die Adresse einer Variablen, die den Wert der [**Visible**](visible-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommands:: setVisible**](iagentcommands--setvisible.md), [ **iagentcommands:: setCaption**](iagentcommands--setcaption.md)


 

 