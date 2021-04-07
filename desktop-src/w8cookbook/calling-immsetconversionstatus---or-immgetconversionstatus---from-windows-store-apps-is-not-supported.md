---
title: Das Aufrufen von immsetconfiguration Manager Status () oder immgetanversionstatus () aus Windows Store-Apps wird nicht unterstützt.
description: Das Aufrufen von immsetconfiguration Manager Status () oder immgetanversionstatus () aus Windows Store-Apps wird nicht unterstützt.
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0846b56b1d6c2367c46e4adf82dac011c49fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727696"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a><span data-ttu-id="4d8f3-103">Das Aufrufen von immsetconfiguration Manager Status () oder immgetanversionstatus () aus Windows Store-Apps wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d8f3-103">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>

## <a name="platforms"></a><span data-ttu-id="4d8f3-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="4d8f3-104">Platforms</span></span>

<dl> <span data-ttu-id="4d8f3-105">Clients-Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="4d8f3-105">Clients - windows 8.1</span></span>  
<span data-ttu-id="4d8f3-106">Server-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4d8f3-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="4d8f3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d8f3-107">Description</span></span>

<span data-ttu-id="4d8f3-108">Das Aufrufen von immsetconfiguration Manager Status () oder immgetanversionstatus () aus einer Windows Store-App wird nicht unterstützt und kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="4d8f3-108">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from a Windows Store app is not supported and may cause unexpected results.</span></span>

## <a name="manifestations"></a><span data-ttu-id="4d8f3-109">Kundgebungen</span><span class="sxs-lookup"><span data-stu-id="4d8f3-109">Manifestations</span></span>

<span data-ttu-id="4d8f3-110">Beim Starten der Anwendung wird der IME-Modus auf die folgenden Standardwerte festgelegt:</span><span class="sxs-lookup"><span data-stu-id="4d8f3-110">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="4d8f3-111">Software Eingabebereich</span><span class="sxs-lookup"><span data-stu-id="4d8f3-111">Software input panel</span></span> | <span data-ttu-id="4d8f3-112">Hardware Tastatur</span><span class="sxs-lookup"><span data-stu-id="4d8f3-112">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="4d8f3-113">Kor, jpn</span><span class="sxs-lookup"><span data-stu-id="4d8f3-113">KOR, JPN</span></span> | <span data-ttu-id="4d8f3-114">Ein</span><span class="sxs-lookup"><span data-stu-id="4d8f3-114">On</span></span>                   | <span data-ttu-id="4d8f3-115">Aus</span><span class="sxs-lookup"><span data-stu-id="4d8f3-115">Off</span></span>               |
| <span data-ttu-id="4d8f3-116">CHS, cht</span><span class="sxs-lookup"><span data-stu-id="4d8f3-116">CHS, CHT</span></span> | <span data-ttu-id="4d8f3-117">Ein</span><span class="sxs-lookup"><span data-stu-id="4d8f3-117">On</span></span>                   | <span data-ttu-id="4d8f3-118">Ein</span><span class="sxs-lookup"><span data-stu-id="4d8f3-118">On</span></span>                |



 

## <a name="solution"></a><span data-ttu-id="4d8f3-119">Lösung</span><span class="sxs-lookup"><span data-stu-id="4d8f3-119">Solution</span></span>

<span data-ttu-id="4d8f3-120">Entwickler können den Standard-IME-Modus steuern, indem Sie einen Eingabe Bereichs Wert für das Feld angeben.</span><span class="sxs-lookup"><span data-stu-id="4d8f3-120">Developers can control the default IME mode by specifying an input scope value for the field.</span></span>

<span data-ttu-id="4d8f3-121">Der IME-Modus für einen angegebenen Eingabebereich wird von jedem IME bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4d8f3-121">The IME mode for a specified input scope is determined by each IME.</span></span> <span data-ttu-id="4d8f3-122">Entwickler können den IME-Modus nicht angeben.</span><span class="sxs-lookup"><span data-stu-id="4d8f3-122">Developers cannot specify the IME mode.</span></span>

## <a name="resources"></a><span data-ttu-id="4d8f3-123">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4d8f3-123">Resources</span></span>

-   [<span data-ttu-id="4d8f3-124">InputScope-Enumeration</span><span class="sxs-lookup"><span data-stu-id="4d8f3-124">InputScope Enumeration</span></span>](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [<span data-ttu-id="4d8f3-125">Immsetsystemversionstatus</span><span class="sxs-lookup"><span data-stu-id="4d8f3-125">ImmSetConversionStatus</span></span>](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   <span data-ttu-id="4d8f3-126">[Immgetsystemversionstatus](/previous-versions/aa912903(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="4d8f3-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span></span>

 

 