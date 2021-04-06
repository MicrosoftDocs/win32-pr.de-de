---
title: DWRITE_RENDERING_MODE Enumerationen
description: Ab Windows 8 wurden von der Enumeration des dwrite \_ -Renderingmodus \_ neue Enumerationswerte hinzugefügt und andere als veraltet markiert.
ms.assetid: 3EA568B4-310D-4F70-9530-5916419282E5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fa79cf34a03960ddb42a8a80221e99d47be847
ms.sourcegitcommit: d1b8f5ed3d6e35e93cb254efc49428a072d7ef9a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/12/2019
ms.locfileid: "103947284"
---
# <a name="dwrite_rendering_mode-enumerations"></a><span data-ttu-id="0042f-103">Enumerationen im dwrite- \_ \_ Renderingmodus</span><span class="sxs-lookup"><span data-stu-id="0042f-103">DWRITE\_RENDERING\_MODE enumerations</span></span>

<span data-ttu-id="0042f-104">Ab Windows 8 wurden von der Enumeration des **dwrite- \_ Renderingmodus \_** neue Enumerationswerte hinzugefügt und andere als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="0042f-104">Starting in Windows 8, the **DWRITE\_RENDERING\_MODE** enumeration added new enumeration values and deprecated others.</span></span>

<span data-ttu-id="0042f-105">Ab Windows 8 bestimmt die Enumeration des [**\_ \_ Antialias \_ Modus für den dwrite-Text**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) , ob Text mit ClearType gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="0042f-105">Starting in Windows 8, the [**DWRITE\_TEXT\_ANTIALIAS\_MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) enumeration determines whether text is rendered using ClearType.</span></span> <span data-ttu-id="0042f-106">Folglich sind alle ClearType-Renderingmodi in der Enumeration des **dwrite- \_ Renderingmodus \_** veraltet.</span><span class="sxs-lookup"><span data-stu-id="0042f-106">As a result, all the ClearType rendering modes in the **DWRITE\_RENDERING\_MODE** enumeration are deprecated.</span></span> <span data-ttu-id="0042f-107">Diese Enumerationswerte werden nun neuen Renderingmodi zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0042f-107">These enumeration values now map to new rendering modes.</span></span>

<span data-ttu-id="0042f-108">In der folgenden Tabelle werden die alten Enumerationswerte und die neuen Werte angezeigt, denen Sie zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0042f-108">The table here shows the old enumeration values and the new values they are mapped to.</span></span> <span data-ttu-id="0042f-109">Beschreibungen der neuen Werte finden Sie unter [**dwrite- \_ Renderingmodus \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode).</span><span class="sxs-lookup"><span data-stu-id="0042f-109">For descriptions of the new values, see [**DWRITE\_RENDERING\_MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode).</span></span>



| <span data-ttu-id="0042f-110">Alter Modus</span><span class="sxs-lookup"><span data-stu-id="0042f-110">Old mode</span></span>                                                                                | <span data-ttu-id="0042f-111">Neuer Modus</span><span class="sxs-lookup"><span data-stu-id="0042f-111">New mode</span></span>                                                                                |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="0042f-112">**dwrite \_ - \_ Renderingmodus \_ ClearType \_ GDI \_ Classic**</span><span class="sxs-lookup"><span data-stu-id="0042f-112">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_GDI\_CLASSIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [<span data-ttu-id="0042f-113">**dwrite \_ - \_ Renderingmodus, \_ klassisches GDI \_**</span><span class="sxs-lookup"><span data-stu-id="0042f-113">**DWRITE\_RENDERING\_MODE\_GDI\_CLASSIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [<span data-ttu-id="0042f-114">**dwrite \_ - \_ Renderingmodus \_ ClearType \_ GDI \_ Natural**</span><span class="sxs-lookup"><span data-stu-id="0042f-114">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_GDI\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [<span data-ttu-id="0042f-115">**dwrite \_ - \_ Renderingmodus, \_ natürliche GDI \_**</span><span class="sxs-lookup"><span data-stu-id="0042f-115">**DWRITE\_RENDERING\_MODE\_GDI\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [<span data-ttu-id="0042f-116">**ClearType für dwrite- \_ \_ Rendermodus \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0042f-116">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            | [<span data-ttu-id="0042f-117">**ClearType für dwrite- \_ \_ Rendermodus \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0042f-117">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            |
| [<span data-ttu-id="0042f-118">**dwrite \_ - \_ Renderingmodus \_ ClearType \_ Natural \_ Symmetric**</span><span class="sxs-lookup"><span data-stu-id="0042f-118">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL\_SYMMETRIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) | [<span data-ttu-id="0042f-119">**dwrite \_ - \_ Renderingmodus \_ ClearType \_ Natural \_ Symmetric**</span><span class="sxs-lookup"><span data-stu-id="0042f-119">**DWRITE\_RENDERING\_MODE\_CLEARTYPE\_NATURAL\_SYMMETRIC**</span></span>](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) |



 

## <a name="in-this-section"></a><span data-ttu-id="0042f-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0042f-120">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0042f-121">Thema</span><span class="sxs-lookup"><span data-stu-id="0042f-121">Topic</span></span></th>
<th><span data-ttu-id="0042f-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0042f-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0042f-123"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 und höher)</strong></a></span><span class="sxs-lookup"><span data-stu-id="0042f-123"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 and later)</strong></a></span></span><br/></td>
<td><span data-ttu-id="0042f-124">Stellt eine Methode zum Rendern von Symbolen dar.</span><span class="sxs-lookup"><span data-stu-id="0042f-124">Represents a method of rendering glyphs.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0042f-125">In diesem Thema geht es um <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> in Windows 8 und höher.</span><span class="sxs-lookup"><span data-stu-id="0042f-125">This topic is about <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> in Windows 8 and later.</span></span> <span data-ttu-id="0042f-126">Informationen zur vorherigen Version finden Sie in <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>diesem Thema</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0042f-126">For info on the previous version see <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>this topic</strong></a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0042f-127"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="0042f-127"><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="0042f-128">Stellt eine Methode zum Rendern von Symbolen dar.</span><span class="sxs-lookup"><span data-stu-id="0042f-128">Represents a method of rendering glyphs.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0042f-129">In diesem Thema geht es um <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> vor Windows 8 und höher.</span><span class="sxs-lookup"><span data-stu-id="0042f-129">This topic is about <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> previous to Windows 8 and later.</span></span> <span data-ttu-id="0042f-130">Informationen zur neueren Version finden Sie in <strong>diesem Thema</strong>.</span><span class="sxs-lookup"><span data-stu-id="0042f-130">For info on the newer version see <strong>this topic</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 





