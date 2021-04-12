---
title: VML regroupid-Attribut
description: VML regroupid-Attribut
ms.assetid: 2fbcc8c5-6e31-4301-9fb8-c2618bb17a1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384703d3fc5675013de09c4e3b5dec7505cf4164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390432"
---
# <a name="vml-regroupid-attribute"></a><span data-ttu-id="6fafc-103">VML regroupid-Attribut</span><span class="sxs-lookup"><span data-stu-id="6fafc-103">VML ReGroupID Attribute</span></span>

<span data-ttu-id="6fafc-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="6fafc-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6fafc-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="6fafc-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6fafc-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="6fafc-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6fafc-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="6fafc-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6fafc-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6fafc-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6fafc-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6fafc-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6fafc-110">Definiert eine vorherige Gruppe für eine Form.</span><span class="sxs-lookup"><span data-stu-id="6fafc-110">Defines a previous group for a shape.</span></span> <span data-ttu-id="6fafc-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6fafc-111">Read/write.</span></span> <span data-ttu-id="6fafc-112">**Vginteger**.</span><span class="sxs-lookup"><span data-stu-id="6fafc-112">**VgInteger**.</span></span>

<span data-ttu-id="6fafc-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="6fafc-113">**Applies To**</span></span>

[<span data-ttu-id="6fafc-114">Form</span><span class="sxs-lookup"><span data-stu-id="6fafc-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="6fafc-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="6fafc-115">**Tag Syntax**</span></span>

<span data-ttu-id="6fafc-116"><v: *Element* o:regroupid = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="6fafc-116"><v: *element* o:regroupid=" *expression* "></span></span>

<span data-ttu-id="6fafc-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="6fafc-117">**Remarks**</span></span>

<span data-ttu-id="6fafc-118">Eine ID-Nummer wird verwendet, um Gruppen von Formen zu identifizieren, die nicht mehr gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="6fafc-118">An ID number is used to identify groups of shapes that are no longer grouped.</span></span> <span data-ttu-id="6fafc-119">Ermöglicht das programmgesteuerte erneute Gruppieren von Formen.</span><span class="sxs-lookup"><span data-stu-id="6fafc-119">Allows shapes to be regrouped programmatically.</span></span>

<span data-ttu-id="6fafc-120">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="6fafc-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="6fafc-121">**Beispiel**</span><span class="sxs-lookup"><span data-stu-id="6fafc-121">**Example**</span></span>

<span data-ttu-id="6fafc-122">Die Form war Teil einer Gruppe, die durch die Gruppen-ID 040754 gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="6fafc-122">The shape was part of a group denoted by the group ID 040754.</span></span>


```HTML
   <v:shape id="rect01" ReGroupID="040754"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 