---
title: Iagentpropertysheet getVisible
description: Iagentpropertysheet getVisible
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcda8be2a3ae3e4084087225e0d7ed79d33621a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310215"
---
# <a name="iagentpropertysheetgetvisible"></a>Iagentpropertysheet:: getVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

Bestimmt, ob das Eigenschaften Blatt des Microsoft-Agents sichtbar oder ausgeblendet ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbvisible*
</dt> <dd>

Adresse einer Variablen, die **true** erhält, wenn das Eigenschaften Blatt sichtbar ist, und **false** , wenn es ausgeblendet ist.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentpropertysheet:: setVisible**](iagentpropertysheet--setvisible.md)


 

 




