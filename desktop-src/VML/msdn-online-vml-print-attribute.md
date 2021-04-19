---
title: VML-Druck Attribut
description: VML-Druck Attribut
ms.assetid: ef9f9f11-782a-40db-986c-946d9ee03071
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55925621ab56f011c998f3feac21a892a4d7ea66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341306"
---
# <a name="vml-print-attribute"></a><span data-ttu-id="33a5b-103">VML-Druck Attribut</span><span class="sxs-lookup"><span data-stu-id="33a5b-103">VML Print Attribute</span></span>

<span data-ttu-id="33a5b-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="33a5b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="33a5b-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="33a5b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="33a5b-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="33a5b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="33a5b-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="33a5b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="33a5b-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="33a5b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="33a5b-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="33a5b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="33a5b-110">Bestimmt, ob die Form gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="33a5b-110">Determines whether the shape will be printed.</span></span> <span data-ttu-id="33a5b-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="33a5b-111">Read/write.</span></span> <span data-ttu-id="33a5b-112">[Vgder State](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="33a5b-112">[VgTriState](msdn-online-vml-vgtristate.md).</span></span>

<span data-ttu-id="33a5b-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="33a5b-113">**Applies To**</span></span>

[<span data-ttu-id="33a5b-114">Form</span><span class="sxs-lookup"><span data-stu-id="33a5b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="33a5b-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="33a5b-115">**Tag Syntax**</span></span>

<span data-ttu-id="33a5b-116"><v: *Element* Print = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="33a5b-116"><v: *element* print=" *expression* "></span></span>

<span data-ttu-id="33a5b-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="33a5b-117">**Script Syntax**</span></span>

<span data-ttu-id="33a5b-118">*Element* . Print = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="33a5b-118">*element* .print="*expression*"</span></span>

<span data-ttu-id="33a5b-119">*Ausdruck* = *Element*. Print</span><span class="sxs-lookup"><span data-stu-id="33a5b-119">*expression*=*element*.print</span></span>

<span data-ttu-id="33a5b-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="33a5b-120">**Remarks**</span></span>

<span data-ttu-id="33a5b-121">Wird als Möglichkeit bereitgestellt, anzugeben, ob Formen gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="33a5b-121">Provided as a way to specify whether shapes will be printed.</span></span> <span data-ttu-id="33a5b-122">Beachten Sie, dass eine Form weiterhin auf dem Bildschirm angezeigt werden kann, auch wenn Sie nicht als Ergebnis dieses Attributs gedruckt wird, das **false** ist.</span><span class="sxs-lookup"><span data-stu-id="33a5b-122">Note that a shape can still be displayed on the screen, even if it is not printed as a result of this attribute being **False**.</span></span> <span data-ttu-id="33a5b-123">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="33a5b-123">The default value is **True**.</span></span>

<span data-ttu-id="33a5b-124">Dieses Attribut wird von Microsoft Office verwendet, wird aber nicht von Microsoft Internet Explorer verwendet.</span><span class="sxs-lookup"><span data-stu-id="33a5b-124">This attribute is used by Microsoft Office but is not used by Microsoft Internet Explorer.</span></span>

<span data-ttu-id="33a5b-125">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="33a5b-125">*Microsoft Office Extensions Attribute*</span></span>

 

 