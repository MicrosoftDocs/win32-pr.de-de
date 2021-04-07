---
title: VML-tablelimits-Attribut
description: VML-tablelimits-Attribut
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b35a7449cc2f348e6040161c1fb599c29972803
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727577"
---
# <a name="vml-tablelimits-attribute"></a><span data-ttu-id="423ba-103">VML-tablelimits-Attribut</span><span class="sxs-lookup"><span data-stu-id="423ba-103">VML TableLimits Attribute</span></span>

<span data-ttu-id="423ba-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="423ba-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="423ba-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="423ba-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="423ba-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="423ba-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="423ba-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="423ba-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="423ba-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="423ba-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="423ba-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="423ba-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="423ba-110">Liste der minimalen Höhenwerte für jede Zeile in einer Tabelle.</span><span class="sxs-lookup"><span data-stu-id="423ba-110">List of minimum height values for each row in a table.</span></span> <span data-ttu-id="423ba-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="423ba-111">Read/write.</span></span> <span data-ttu-id="423ba-112">**Vglengtharray**.</span><span class="sxs-lookup"><span data-stu-id="423ba-112">**VgLengthArray**.</span></span>

<span data-ttu-id="423ba-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="423ba-113">**Applies To**</span></span>

[<span data-ttu-id="423ba-114">Form</span><span class="sxs-lookup"><span data-stu-id="423ba-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="423ba-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="423ba-115">**Tag Syntax**</span></span>

<span data-ttu-id="423ba-116"><v: *Element* o:tablelimits = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="423ba-116"><v: *element* o:tablelimits=" *expression* "></span></span>

<span data-ttu-id="423ba-117">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="423ba-117">**Remarks**</span></span>

<span data-ttu-id="423ba-118">Wird von Microsoft PowerPoint für Native Tabellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="423ba-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="423ba-119">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="423ba-119">Default value is **Null**.</span></span>

<span data-ttu-id="423ba-120">Obwohl der Wert in einer Form gespeichert ist, ist das-Attribut nur nützlich, wenn die Tabelle aus Formen besteht, die gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="423ba-120">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.</span></span> <span data-ttu-id="423ba-121">Wenn den Tabellenzellen Text hinzugefügt wird, kann sich die Zeilenhöhe erhöhen.</span><span class="sxs-lookup"><span data-stu-id="423ba-121">When text is added to table cells, the row height may increase.</span></span> <span data-ttu-id="423ba-122">Das **tablelimits** -Attribut speichert die ursprüngliche Zeilenhöhe, sodass die Zeilenhöhe, wenn der Text gelöscht wird, nicht unter den ursprünglichen Wert fällt.</span><span class="sxs-lookup"><span data-stu-id="423ba-122">The **TableLimits** attribute stores the original row height so that if text is deleted, the row height will not fall below the original value.</span></span>

<span data-ttu-id="423ba-123">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="423ba-123">*Microsoft Office Extensions Attribute*</span></span>

 

 