---
title: VML connecttype-Attribut
description: VML connecttype-Attribut
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a54135dcb4ffe0a86f781d68b8babe1259029be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101663"
---
# <a name="vml-connecttype-attribute"></a><span data-ttu-id="4d5d1-103">VML connecttype-Attribut</span><span class="sxs-lookup"><span data-stu-id="4d5d1-103">VML ConnectType Attribute</span></span>

<span data-ttu-id="4d5d1-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4d5d1-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4d5d1-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4d5d1-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4d5d1-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4d5d1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4d5d1-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4d5d1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4d5d1-110">Definiert den Typ der Verbindungspunkte, die zum Anfügen von Formen an andere Formen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-110">Defines the type of connection points used for attaching shapes to other shapes.</span></span> <span data-ttu-id="4d5d1-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-111">Read/write.</span></span> <span data-ttu-id="4d5d1-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-112">**String**.</span></span>

<span data-ttu-id="4d5d1-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="4d5d1-113">**Applies To**</span></span>

[<span data-ttu-id="4d5d1-114">Pfad</span><span class="sxs-lookup"><span data-stu-id="4d5d1-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="4d5d1-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="4d5d1-115">**Tag Syntax**</span></span>

<span data-ttu-id="4d5d1-116"><v: *Element* o:connecttype = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="4d5d1-116"><v: *element* o:connecttype=" *expression* "></span></span>

<span data-ttu-id="4d5d1-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="4d5d1-117">**Remarks**</span></span>

<span data-ttu-id="4d5d1-118">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="4d5d1-118">Values include:</span></span>



| <span data-ttu-id="4d5d1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4d5d1-119">Value</span></span>    | <span data-ttu-id="4d5d1-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d5d1-120">Description</span></span>                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d5d1-121">none</span><span class="sxs-lookup"><span data-stu-id="4d5d1-121">none</span></span>     | <span data-ttu-id="4d5d1-122">Keine Verbindungs Standorte.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-122">No connection sites.</span></span> <span data-ttu-id="4d5d1-123">Standard.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-123">Default.</span></span>                                                                                                         |
| <span data-ttu-id="4d5d1-124">rect</span><span class="sxs-lookup"><span data-stu-id="4d5d1-124">rect</span></span>     | <span data-ttu-id="4d5d1-125">Standard vier Verbindungspunkte in Mittelpunkten von oben, unten, Links und rechts.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-125">Standard four connection points at midpoints of top, bottom, left, and right sides.</span></span>                                                   |
| <span data-ttu-id="4d5d1-126">Segmente</span><span class="sxs-lookup"><span data-stu-id="4d5d1-126">segments</span></span> | <span data-ttu-id="4d5d1-127">Die Bearbeitungspunkte der Form werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-127">The edit points of the shape are used.</span></span> <span data-ttu-id="4d5d1-128">Bearbeitungspunkte sind die schwarzen Punkte in einem grafischen Editor, die verwendet werden, um Teile einer Form auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-128">Edit points are the black dots in a graphical editor that are used to select parts of a shape.</span></span> |
| <span data-ttu-id="4d5d1-129">custom</span><span class="sxs-lookup"><span data-stu-id="4d5d1-129">custom</span></span>   | <span data-ttu-id="4d5d1-130">Ein benutzerdefiniertes Array von Verbindungs Standorten.</span><span class="sxs-lookup"><span data-stu-id="4d5d1-130">A custom array of connection locations.</span></span>                                                                                               |



 

<span data-ttu-id="4d5d1-131">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="4d5d1-131">*Microsoft Office Extensions Attribute*</span></span>

 

 