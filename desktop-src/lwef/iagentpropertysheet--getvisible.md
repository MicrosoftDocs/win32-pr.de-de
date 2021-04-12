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
# <a name="iagentpropertysheetgetvisible"></a><span data-ttu-id="0c31e-103">Iagentpropertysheet:: getVisible</span><span class="sxs-lookup"><span data-stu-id="0c31e-103">IAgentPropertySheet::GetVisible</span></span>

<span data-ttu-id="0c31e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0c31e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

<span data-ttu-id="0c31e-105">Bestimmt, ob das Eigenschaften Blatt des Microsoft-Agents sichtbar oder ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="0c31e-105">Determines whether the Microsoft Agent property sheet is visible or hidden.</span></span>

-   <span data-ttu-id="0c31e-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0c31e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0c31e-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbvisible*</span><span class="sxs-lookup"><span data-stu-id="0c31e-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="0c31e-108">Adresse einer Variablen, die **true** erhält, wenn das Eigenschaften Blatt sichtbar ist, und **false** , wenn es ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="0c31e-108">Address of a variable that receives **True** if the property sheet is visible and **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="0c31e-109">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0c31e-109">See Also</span></span>

[<span data-ttu-id="0c31e-110">**Iagentpropertysheet:: setVisible**</span><span class="sxs-lookup"><span data-stu-id="0c31e-110">**IAgentPropertySheet::SetVisible**</span></span>](iagentpropertysheet--setvisible.md)


 

 




