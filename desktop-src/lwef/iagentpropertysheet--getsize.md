---
title: Iagentpropertysheet GetSize
description: Iagentpropertysheet GetSize
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341240"
---
# <a name="iagentpropertysheetgetsize"></a><span data-ttu-id="4ca34-103">Iagentpropertysheet:: GetSize</span><span class="sxs-lookup"><span data-stu-id="4ca34-103">IAgentPropertySheet::GetSize</span></span>

<span data-ttu-id="4ca34-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="4ca34-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

<span data-ttu-id="4ca34-105">Ruft die Größe des Eigenschaften Blatt Fensters von Microsoft-Agent ab.</span><span class="sxs-lookup"><span data-stu-id="4ca34-105">Retrieves the size of the Microsoft Agent property sheet window.</span></span>

-   <span data-ttu-id="4ca34-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4ca34-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4ca34-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plwidth*</span><span class="sxs-lookup"><span data-stu-id="4ca34-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="4ca34-108">Adresse einer Variablen, die die Breite des Eigenschaften Blatts in Pixel relativ zum Bildschirm Ursprung (oben links) empfängt.</span><span class="sxs-lookup"><span data-stu-id="4ca34-108">Address of a variable that receives the width of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="4ca34-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plheight*</span><span class="sxs-lookup"><span data-stu-id="4ca34-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="4ca34-110">Adresse einer Variablen, die die Höhe des Eigenschaften Blatts in Pixel relativ zum Bildschirm Ursprung (oben links) empfängt.</span><span class="sxs-lookup"><span data-stu-id="4ca34-110">Address of a variable that receives the height of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="4ca34-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4ca34-111">See Also</span></span>

[<span data-ttu-id="4ca34-112">**Iagentpropertysheet:: GetPosition**</span><span class="sxs-lookup"><span data-stu-id="4ca34-112">**IAgentPropertySheet::GetPosition**</span></span>](iagentpropertysheet--getposition.md)


 

 




