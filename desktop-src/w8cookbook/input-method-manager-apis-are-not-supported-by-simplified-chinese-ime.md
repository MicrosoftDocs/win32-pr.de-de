---
title: Eingabemethoden-Manager-APIs werden vom vereinfachten Chinesisch (IME) nicht unterstützt
description: Eingabemethoden-Manager-APIs werden vom vereinfachten Chinesisch (IME) nicht unterstützt
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d01d79d569ee7c72508bc217b68bcdf784f0d61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101902"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a><span data-ttu-id="d3c0a-103">Eingabemethoden-Manager-APIs werden vom vereinfachten Chinesisch (IME) nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d3c0a-103">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>

## <a name="platforms"></a><span data-ttu-id="d3c0a-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="d3c0a-104">Platforms</span></span>

<dl> <span data-ttu-id="d3c0a-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d3c0a-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="d3c0a-106">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d3c0a-106">Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="d3c0a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3c0a-107">Description</span></span>

<span data-ttu-id="d3c0a-108">Die folgenden Eingabemethoden-Manager-APIs werden von vereinfachten chinesischen IMEs in Windows 8.1 nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d3c0a-108">The following input method manager APIs are not supported by Simplified Chinese IMEs in Windows 8.1:</span></span>

-   <span data-ttu-id="d3c0a-109">Ifecommon-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d3c0a-109">IFECommon interface</span></span>
-   <span data-ttu-id="d3c0a-110">Ifedictionary-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d3c0a-110">IFEDictionary interface</span></span>
-   <span data-ttu-id="d3c0a-111">Ifelanguage-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d3c0a-111">IFELanguage interface</span></span>
-   <span data-ttu-id="d3c0a-112">Iimepad-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d3c0a-112">IImePad interface</span></span>
-   <span data-ttu-id="d3c0a-113">Iimepadapplet-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d3c0a-113">IImePadApplet interface</span></span>
-   <span data-ttu-id="d3c0a-114">Iimespecifyapplets-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d3c0a-114">IImeSpecifyApplets interface</span></span>

## <a name="manifestations"></a><span data-ttu-id="d3c0a-115">Kundgebungen</span><span class="sxs-lookup"><span data-stu-id="d3c0a-115">Manifestations</span></span>

<span data-ttu-id="d3c0a-116">Die Funktionen, die diese APIs verwenden, funktionieren nicht mit dem vereinfachten Chinesisch (IME).</span><span class="sxs-lookup"><span data-stu-id="d3c0a-116">The functions that use those APIs don’t work with Simplified Chinese IME.</span></span>

## <a name="solution"></a><span data-ttu-id="d3c0a-117">Lösung</span><span class="sxs-lookup"><span data-stu-id="d3c0a-117">Solution</span></span>

<span data-ttu-id="d3c0a-118">Anwendungen müssen so entworfen werden, dass Benutzer die gewünschte Aufgabe ohne die angegebene API durchführen können.</span><span class="sxs-lookup"><span data-stu-id="d3c0a-118">Applications must be designed so that users can complete the desired task without using the specified API.</span></span>

## <a name="resources"></a><span data-ttu-id="d3c0a-119">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d3c0a-119">Resources</span></span>

-   [<span data-ttu-id="d3c0a-120">Schnittstellen für Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="d3c0a-120">Input Method Manager Interfaces</span></span>](../intl/input-method-manager-interfaces.md)
-   [<span data-ttu-id="d3c0a-121">Ifecommon</span><span class="sxs-lookup"><span data-stu-id="d3c0a-121">IFECommon</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="d3c0a-122">Ifecommon-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d3c0a-122">IFECommon interface</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="d3c0a-123">Ifedictionary-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d3c0a-123">IFEDictionary interface</span></span>](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [<span data-ttu-id="d3c0a-124">Ifelanguage</span><span class="sxs-lookup"><span data-stu-id="d3c0a-124">IFELanguage</span></span>](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [<span data-ttu-id="d3c0a-125">Iimepad</span><span class="sxs-lookup"><span data-stu-id="d3c0a-125">IImePad</span></span>](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [<span data-ttu-id="d3c0a-126">Iimepadapplet</span><span class="sxs-lookup"><span data-stu-id="d3c0a-126">IImePadApplet</span></span>](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [<span data-ttu-id="d3c0a-127">Iimepluginditdiktattionarylist</span><span class="sxs-lookup"><span data-stu-id="d3c0a-127">IimePlugInDictDictionaryList</span></span>](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [<span data-ttu-id="d3c0a-128">Iimespecifyapplets</span><span class="sxs-lookup"><span data-stu-id="d3c0a-128">IImeSpecifyApplets</span></span>](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 