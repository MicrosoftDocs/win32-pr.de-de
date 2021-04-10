---
title: Matrix Attribut (schiefe) (VML)
description: Matrix Attribut (schiefe) (VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8327acfebfe4d968e673060f2f3cbef69d3e9db6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039514"
---
# <a name="matrix-attribute-skewvml"></a><span data-ttu-id="af64d-103">Matrix Attribut (schiefe) (VML)</span><span class="sxs-lookup"><span data-stu-id="af64d-103">Matrix Attribute (Skew)(VML)</span></span>

<span data-ttu-id="af64d-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="af64d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="af64d-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="af64d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="af64d-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="af64d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="af64d-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="af64d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="af64d-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="af64d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="af64d-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="af64d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="af64d-110">Definiert eine perspektivische Transformation einer Schiefe.</span><span class="sxs-lookup"><span data-stu-id="af64d-110">Defines a perspective transform of a skew.</span></span> <span data-ttu-id="af64d-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="af64d-111">Read/write.</span></span> <span data-ttu-id="af64d-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="af64d-112">**String**.</span></span>

<span data-ttu-id="af64d-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="af64d-113">**Applies To**</span></span>

[<span data-ttu-id="af64d-114">Neigen</span><span class="sxs-lookup"><span data-stu-id="af64d-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="af64d-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="af64d-115">**Tag Syntax**</span></span>

<span data-ttu-id="af64d-116"><o: *Element* Matrix = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="af64d-116"><o: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="af64d-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="af64d-117">**Script Syntax**</span></span>

<span data-ttu-id="af64d-118">*Element* . Matrix = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="af64d-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="af64d-119">*Ausdruck* = *Element*. Matrix</span><span class="sxs-lookup"><span data-stu-id="af64d-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="af64d-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="af64d-120">**Remarks**</span></span>

<span data-ttu-id="af64d-121">Die Matrix ist eine Zeichenfolge im Format "Sxx, sxy, syx, SYY, px, py", wobei s den Wert "Scale", "p" und "x" und "y" x-und y-Werte darstellen.</span><span class="sxs-lookup"><span data-stu-id="af64d-121">The matrix is a string in the form "sxx, sxy, syx, syy, px, py" where s is scale, p is perspective, and x and y are x and y values.</span></span> <span data-ttu-id="af64d-122">Wenn [Offset](offset-attribute--skew--vml.md) in absoluten Einheiten ist, befinden sich px und py in den [Einheiten](msdn-online-vml-units.md) "EMU ^-1" (andernfalls handelt es sich um einen umgekehrten Bruchteil der Shape-Größe).</span><span class="sxs-lookup"><span data-stu-id="af64d-122">If [Offset](offset-attribute--skew--vml.md) is in absolute units, then px and py are in emu^-1 [units](msdn-online-vml-units.md) (otherwise they are an inverse fraction of the shape size).</span></span> <span data-ttu-id="af64d-123">Der Standardwert ist "1, 0, 0, 1, 0, 0".</span><span class="sxs-lookup"><span data-stu-id="af64d-123">The default value is "1,0,0,1,0,0".</span></span>

<span data-ttu-id="af64d-124">*Microsoft Office Extensions-Attribut*</span><span class="sxs-lookup"><span data-stu-id="af64d-124">*Microsoft Office Extensions Attribute*</span></span>

 

 