---
title: Althref-Attribut (imagedata) (VML)
description: Althref-Attribut (imagedata) (VML)
ms.assetid: c55ede90-3d57-4f27-9940-1fe4751cef71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004625d769c12e67de024bf537ee04c377a18c8c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039176"
---
# <a name="althref-attribute-imagedatavml"></a><span data-ttu-id="d27cb-103">Althref-Attribut (imagedata) (VML)</span><span class="sxs-lookup"><span data-stu-id="d27cb-103">AltHRef Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="d27cb-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="d27cb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d27cb-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="d27cb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d27cb-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="d27cb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d27cb-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d27cb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d27cb-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d27cb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d27cb-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d27cb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d27cb-110">Gibt einen alternativen Verweis für ein Bild an.</span><span class="sxs-lookup"><span data-stu-id="d27cb-110">Specifies an alternate reference for an image.</span></span> <span data-ttu-id="d27cb-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d27cb-111">Read/write.</span></span> <span data-ttu-id="d27cb-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="d27cb-112">**String**.</span></span>

<span data-ttu-id="d27cb-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="d27cb-113">**Applies To**</span></span>

[<span data-ttu-id="d27cb-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="d27cb-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="d27cb-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="d27cb-115">**Tag Syntax**</span></span>

<span data-ttu-id="d27cb-116"><v: *Element* o:althref = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="d27cb-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="d27cb-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="d27cb-117">**Script Syntax**</span></span>

<span data-ttu-id="d27cb-118">*Element* . althref = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="d27cb-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="d27cb-119">*Ausdruck* = *Element*. althref</span><span class="sxs-lookup"><span data-stu-id="d27cb-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="d27cb-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="d27cb-120">**Remarks**</span></span>

<span data-ttu-id="d27cb-121">Unterstützt die Beibehaltung von Daten mithilfe von HTML-Roundtripping.</span><span class="sxs-lookup"><span data-stu-id="d27cb-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="d27cb-122">Beim HTML-Schreibvorgang wird die alternative Darstellung (d. h. die ursprünglichen Daten, wenn die Datei vom Macintosh stammt) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d27cb-122">On HTML write, the alternate representation (that is, the original PICT data if the file originated from the Macintosh) is saved.</span></span> <span data-ttu-id="d27cb-123">Bei einem HTML-Lesevorgang wird **althref** gegenüber **src** bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="d27cb-123">On an HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="d27cb-124">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="d27cb-124">*Microsoft Office Extensions Attribute*</span></span>

 

 