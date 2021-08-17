---
title: IAgentPropertySheet GetVisible
description: IAgentPropertySheet GetVisible
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac95d1da3d1c0b4e5bf65c2f5f43c67153cc1d6af934e1814735abb12ed8d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692302"
---
# <a name="iagentpropertysheetgetvisible"></a>IAgentPropertySheet::GetVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

Bestimmt, ob das Eigenschaftenblatt des Microsoft-Agents sichtbar oder ausgeblendet ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Adresse einer Variablen, die **True** empfängt, wenn das Eigenschaftenblatt sichtbar ist, und **FALSE,** wenn es ausgeblendet ist.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentPropertySheet::SetVisible**](iagentpropertysheet--setvisible.md)


 

 




