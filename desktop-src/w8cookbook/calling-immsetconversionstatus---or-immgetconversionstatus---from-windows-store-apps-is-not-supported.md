---
title: Das Aufrufen von ImmSetConversionStatus() oder ImmGetConversionStatus() aus Windows Store-Apps wird nicht unterstützt.
description: Das Aufrufen von ImmSetConversionStatus() oder ImmGetConversionStatus() aus Windows Store-Apps wird nicht unterstützt.
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8ca572b1ea88ca988ecba66231a87cb6ae6db2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443145"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a><span data-ttu-id="dbf88-103">Das Aufrufen von ImmSetConversionStatus() oder ImmGetConversionStatus() aus Windows Store-Apps wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dbf88-103">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>

## <a name="platforms"></a><span data-ttu-id="dbf88-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="dbf88-104">Platforms</span></span>

<dl> <span data-ttu-id="dbf88-105">Clients – Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dbf88-105">Clients - windows 8.1</span></span>  
<span data-ttu-id="dbf88-106">Server – Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dbf88-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="dbf88-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbf88-107">Description</span></span>

<span data-ttu-id="dbf88-108">Das Aufrufen von ImmSetConversionStatus() oder ImmGetConversionStatus() aus einer Windows Store-App wird nicht unterstützt und kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="dbf88-108">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from a Windows Store app is not supported and may cause unexpected results.</span></span>

## <a name="manifestations"></a><span data-ttu-id="dbf88-109">Manifestationen</span><span class="sxs-lookup"><span data-stu-id="dbf88-109">Manifestations</span></span>

<span data-ttu-id="dbf88-110">Beim Starten der Anwendung wird der IME-Modus auf die folgenden Standardwerte festgelegt:</span><span class="sxs-lookup"><span data-stu-id="dbf88-110">At application start up, the IME mode is set to the following defaults:</span></span>



| &nbsp;   | <span data-ttu-id="dbf88-111">Softwareeingabebereich</span><span class="sxs-lookup"><span data-stu-id="dbf88-111">Software input panel</span></span> | <span data-ttu-id="dbf88-112">Hardwaretastatur</span><span class="sxs-lookup"><span data-stu-id="dbf88-112">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="dbf88-113">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="dbf88-113">KOR, JPN</span></span> | <span data-ttu-id="dbf88-114">Ein</span><span class="sxs-lookup"><span data-stu-id="dbf88-114">On</span></span>                   | <span data-ttu-id="dbf88-115">Aus</span><span class="sxs-lookup"><span data-stu-id="dbf88-115">Off</span></span>               |
| <span data-ttu-id="dbf88-116">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="dbf88-116">CHS, CHT</span></span> | <span data-ttu-id="dbf88-117">Ein</span><span class="sxs-lookup"><span data-stu-id="dbf88-117">On</span></span>                   | <span data-ttu-id="dbf88-118">Ein</span><span class="sxs-lookup"><span data-stu-id="dbf88-118">On</span></span>                |



 

## <a name="solution"></a><span data-ttu-id="dbf88-119">Lösung</span><span class="sxs-lookup"><span data-stu-id="dbf88-119">Solution</span></span>

<span data-ttu-id="dbf88-120">Entwickler können den STANDARD-IME-Modus steuern, indem sie einen Eingabebereichswert für das Feld angeben.</span><span class="sxs-lookup"><span data-stu-id="dbf88-120">Developers can control the default IME mode by specifying an input scope value for the field.</span></span>

<span data-ttu-id="dbf88-121">Der IME-Modus für einen angegebenen Eingabebereich wird von jeder IME bestimmt.</span><span class="sxs-lookup"><span data-stu-id="dbf88-121">The IME mode for a specified input scope is determined by each IME.</span></span> <span data-ttu-id="dbf88-122">Entwickler können den IME-Modus nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="dbf88-122">Developers cannot specify the IME mode.</span></span>

## <a name="resources"></a><span data-ttu-id="dbf88-123">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dbf88-123">Resources</span></span>

-   [<span data-ttu-id="dbf88-124">InputScope-Enumeration</span><span class="sxs-lookup"><span data-stu-id="dbf88-124">InputScope Enumeration</span></span>](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [<span data-ttu-id="dbf88-125">ImmSetConversionStatus</span><span class="sxs-lookup"><span data-stu-id="dbf88-125">ImmSetConversionStatus</span></span>](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   <span data-ttu-id="dbf88-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="dbf88-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span></span>

 

 