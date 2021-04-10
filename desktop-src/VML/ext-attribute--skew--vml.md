---
title: Ext-Attribut (schiefe) (VML)
description: Ext-Attribut (schiefe) (VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209280"
---
# <a name="ext-attribute-skewvml"></a><span data-ttu-id="e54a4-103">Ext-Attribut (schiefe) (VML)</span><span class="sxs-lookup"><span data-stu-id="e54a4-103">Ext Attribute (Skew)(VML)</span></span>

<span data-ttu-id="e54a4-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="e54a4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e54a4-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="e54a4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e54a4-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="e54a4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e54a4-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="e54a4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e54a4-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e54a4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e54a4-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e54a4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e54a4-110">Definiert die Art und Weise, wie eine schiefe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e54a4-110">Defines the way a skew is displayed.</span></span> <span data-ttu-id="e54a4-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e54a4-111">Read/write.</span></span> <span data-ttu-id="e54a4-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="e54a4-112">**String**.</span></span>

<span data-ttu-id="e54a4-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="e54a4-113">**Applies To**</span></span>

[<span data-ttu-id="e54a4-114">Neigen</span><span class="sxs-lookup"><span data-stu-id="e54a4-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="e54a4-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="e54a4-115">**Tag Syntax**</span></span>

<span data-ttu-id="e54a4-116"><o: *Element* v:ext = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="e54a4-116"><o: *element* v:ext=" *expression* "></span></span>

<span data-ttu-id="e54a4-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="e54a4-117">**Script Syntax**</span></span>

<span data-ttu-id="e54a4-118">*Element* . ext = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="e54a4-118">*element* .ext="*expression*"</span></span>

<span data-ttu-id="e54a4-119">*Ausdruck* = *Element*. ext</span><span class="sxs-lookup"><span data-stu-id="e54a4-119">*expression*=*element*.ext</span></span>

<span data-ttu-id="e54a4-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="e54a4-120">**Remarks**</span></span>

<span data-ttu-id="e54a4-121">Dieses Attribut wird verwendet, um grafischen Editoren mitzuteilen, wie das **schiefe** -Element verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e54a4-121">This attribute is used to tell graphical editors how to process the **Skew** element.</span></span> <span data-ttu-id="e54a4-122">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="e54a4-122">Values include:</span></span>

-   <span data-ttu-id="e54a4-123">**edit**</span><span class="sxs-lookup"><span data-stu-id="e54a4-123">**edit**</span></span>
-   <span data-ttu-id="e54a4-124">**anzeigen** (Standard)</span><span class="sxs-lookup"><span data-stu-id="e54a4-124">**view** (default)</span></span>
-   <span data-ttu-id="e54a4-125">**backwardkompatibel**</span><span class="sxs-lookup"><span data-stu-id="e54a4-125">**backwardCompatible**</span></span>

<span data-ttu-id="e54a4-126">Wenn eine Erweiterung auf **Bearbeiten** festgelegt ist, kann Sie von einem Software Viewer ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="e54a4-126">If an extension is set to **edit**, it can be ignored by a software viewer.</span></span> <span data-ttu-id="e54a4-127">Wenn Sie auf **View** festgelegt ist, muss der Viewer stattdessen die Bitmap-Darstellung Rendering.</span><span class="sxs-lookup"><span data-stu-id="e54a4-127">If set to **view**, the viewer must render the bitmap representation instead.</span></span>

<span data-ttu-id="e54a4-128">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="e54a4-128">*Microsoft Office Extensions Attribute*</span></span>

 

 