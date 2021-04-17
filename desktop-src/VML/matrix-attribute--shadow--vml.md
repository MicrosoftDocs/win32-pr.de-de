---
title: Matrix Attribut (Schatten) (VML)
description: Matrix Attribut (Schatten) (VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d599aa817e87481aefdec43dbe345b7235fc54bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390923"
---
# <a name="matrix-attribute-shadowvml"></a><span data-ttu-id="3316a-103">Matrix Attribut (Schatten) (VML)</span><span class="sxs-lookup"><span data-stu-id="3316a-103">Matrix Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="3316a-104">In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="3316a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3316a-105">Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.</span><span class="sxs-lookup"><span data-stu-id="3316a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3316a-106">Ab Dezember 2011 wurde dieses Thema archiviert.</span><span class="sxs-lookup"><span data-stu-id="3316a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3316a-107">Daher wird er nicht mehr aktiv verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3316a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3316a-108">Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3316a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3316a-109">Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3316a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3316a-110">Definiert eine perspektivische Transformation für einen Schatten.</span><span class="sxs-lookup"><span data-stu-id="3316a-110">Defines a perspective transform for a shadow.</span></span> <span data-ttu-id="3316a-111">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3316a-111">Read/write.</span></span> <span data-ttu-id="3316a-112">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="3316a-112">**String**.</span></span>

<span data-ttu-id="3316a-113">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="3316a-113">**Applies To**</span></span>

[<span data-ttu-id="3316a-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="3316a-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="3316a-115">**Tagsyntax**</span><span class="sxs-lookup"><span data-stu-id="3316a-115">**Tag Syntax**</span></span>

<span data-ttu-id="3316a-116"><v: *Element* Matrix = " *Ausdruck* " ></span><span class="sxs-lookup"><span data-stu-id="3316a-116"><v: *element* matrix=" *expression* "></span></span>

<span data-ttu-id="3316a-117">**Skript Syntax**</span><span class="sxs-lookup"><span data-stu-id="3316a-117">**Script Syntax**</span></span>

<span data-ttu-id="3316a-118">*Element* . Matrix = "*Ausdruck*"</span><span class="sxs-lookup"><span data-stu-id="3316a-118">*element* .matrix="*expression*"</span></span>

<span data-ttu-id="3316a-119">*Ausdruck* = *Element*. Matrix</span><span class="sxs-lookup"><span data-stu-id="3316a-119">*expression*=*element*.matrix</span></span>

<span data-ttu-id="3316a-120">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="3316a-120">**Remarks**</span></span>

<span data-ttu-id="3316a-121">Eine perspektivische Transformationsmatrix in der Form "Sxx, sxy, syx, SYY, px, py", wobei s = Scale und p = Perspective ist.</span><span class="sxs-lookup"><span data-stu-id="3316a-121">A perspective transform matrix in the form "sxx,sxy,syx,syy,px,py" where s= scale and p = perspective.</span></span> <span data-ttu-id="3316a-122">Wenn der Offset in absoluten Einheiten liegt, sind px und py in 1/Emu-Einheiten. andernfalls handelt es sich um einen umgekehrten Bruchteil der Shape-Größe.</span><span class="sxs-lookup"><span data-stu-id="3316a-122">If offset is in absolute units then px, py are in 1/emu units; otherwise they are an inverse fraction of the shape size.</span></span>

<span data-ttu-id="3316a-123">*VML-Standard Attribut*</span><span class="sxs-lookup"><span data-stu-id="3316a-123">*VML Standard Attribute*</span></span>

 

 