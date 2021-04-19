---
title: Änderungen in DX9 Legacy Hardwareunterstützung
description: Änderungen in DX9 Legacy Hardwareunterstützung
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1ae5c4b15a2019450cc5b209f34561d8ec672d
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106341969"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a><span data-ttu-id="71659-103">Änderungen in DX9 Legacy Hardwareunterstützung</span><span class="sxs-lookup"><span data-stu-id="71659-103">Changes in DX9 legacy hardware support</span></span>

## <a name="platform"></a><span data-ttu-id="71659-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="71659-104">Platform</span></span>

<span data-ttu-id="71659-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="71659-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="71659-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71659-106">Description</span></span>

<span data-ttu-id="71659-107">Intel und AMD/ATI unterstützen Ihre DX9-Grafik Teile nicht mehr und aktualisieren die Treiber für diese Geräte nicht für Windows 8.</span><span class="sxs-lookup"><span data-stu-id="71659-107">Intel and AMD/ATI no longer support their DX9 graphics parts and will not be updating drivers for these devices for Windows 8.</span></span> <span data-ttu-id="71659-108">Außerdem werden diese Geräte nicht in Box für Windows 8 behandelt.</span><span class="sxs-lookup"><span data-stu-id="71659-108">Furthermore, these devices are not covered in-box for Windows 8.</span></span> <span data-ttu-id="71659-109">Die letzten Treiber für diese Geräte sind auf Wu und auf den Websites von OEM/IHV verfügbar. viele Datumsangaben von Vista, und viele dieser endgültigen Versions Treiber zeigen Probleme unter Windows 8 an.</span><span class="sxs-lookup"><span data-stu-id="71659-109">The last drivers for these devices are those available on WU and on the OEM/IHV’s websites; many date from Vista, and many of these final version drivers exhibit problems on Windows 8.</span></span> <span data-ttu-id="71659-110">Außerdem hat NVIDIA vor kurzem festgestellt, dass Ihre DX9-(Vista und ältere) mobilen (Notebook-) Teile für Windows 8 nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="71659-110">In addition, nVidia has recently stated that they will not support their DX9 (Vista and older) mobile (notebook) parts for Windows 8.</span></span> <span data-ttu-id="71659-111">Sie unterstützen weiterhin Ihre Desktop-DX9-Teile.</span><span class="sxs-lookup"><span data-stu-id="71659-111">They continue to support their desktop DX9 parts.</span></span>

<span data-ttu-id="71659-112">Alle diese Treiber/Teil-Kombinationen finden Sie in der Internet Explorer 9-Software Fall Back Liste.</span><span class="sxs-lookup"><span data-stu-id="71659-112">All of these driver/part combinations are on the Internet Explorer 9 software fallback list.</span></span> <span data-ttu-id="71659-113">Dies bedeutet, dass Internet Explorer 9 aus Leistungs-oder Stabilitätsgründen das Software Rendering auf diesen Geräten verwendet.</span><span class="sxs-lookup"><span data-stu-id="71659-113">This means that for either performance or stability reasons, Internet Explorer 9 uses software rendering on these devices.</span></span> <span data-ttu-id="71659-114">Dies ist ein guter Hinweis darauf, dass die Verwendung von Windows Store-Apps für diese Treiber und Teile nicht zufriedenstellend ist.</span><span class="sxs-lookup"><span data-stu-id="71659-114">This is a good indication that the experience with Windows Store apps will not be satisfactory on these drivers and parts.</span></span>

## <a name="manifestation"></a><span data-ttu-id="71659-115">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="71659-115">Manifestation</span></span>

<span data-ttu-id="71659-116">Da es keine Unterstützung für diese Geräte gibt, werden viele Benutzer mit diesen Teilen auf dem Microsoft Basic-Anzeigetreiber ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71659-116">As there is no in-box support for these devices, many users with these parts will wind up running on the Microsoft Basic Display Driver.</span></span> <span data-ttu-id="71659-117">Dabei handelt es sich um eine auf Warp basierende WDDM 1,2-softwaregpu, die tatsächlich schneller ist als einige der Teile in dieser Klasse, z. b. die Intel GMA500-Serie).</span><span class="sxs-lookup"><span data-stu-id="71659-117">This is a WARP-based WDDM 1.2 software GPU, and is actually faster than some of the parts in this class, for example, the Intel GMA500 series).</span></span> <span data-ttu-id="71659-118">Es werden Aero-Glass und DWM unterstützt, und es können Windows Store-Apps ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="71659-118">It supports aero-glass and DWM, and can run Windows Store apps.</span></span>

<span data-ttu-id="71659-119">Es bestehen jedoch einige wichtige Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="71659-119">However, it has some important limitations:</span></span>

-   <span data-ttu-id="71659-120">Es unterstützt nicht mehrere Monitore oder Projektionen.</span><span class="sxs-lookup"><span data-stu-id="71659-120">It doesn’t support multiple monitors or projection</span></span>
-   <span data-ttu-id="71659-121">Der Standbymodus wird nicht unterstützt, obwohl er Ruhe Zustands unterstützt.</span><span class="sxs-lookup"><span data-stu-id="71659-121">It doesn’t support sleep, though it does support hibernation</span></span>
-   <span data-ttu-id="71659-122">Das Ändern der Bildschirmauflösung wird häufig nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="71659-122">It often will not allow changing screen resolution</span></span>

## <a name="mitigation"></a><span data-ttu-id="71659-123">Minderung</span><span class="sxs-lookup"><span data-stu-id="71659-123">Mitigation</span></span>

<span data-ttu-id="71659-124">Wenn Sie nach dem Testen feststellen, dass die Benutzer Leistung nicht akzeptabel ist, können Sie Hardwareanforderungen für Ihre Produkte festlegen, die diese älteren DX9 Intel-und AMD-Komponenten ausschließen.</span><span class="sxs-lookup"><span data-stu-id="71659-124">If after testing, you find that the user experience is not acceptable, you may choose to set hardware requirements for their products that exclude these older DX9 Intel and AMD parts.</span></span> <span data-ttu-id="71659-125">Sie können auch eine Warnung für Ihre Kunden angeben, dass Sie für diese Teile möglicherweise nicht akzeptabel sind.</span><span class="sxs-lookup"><span data-stu-id="71659-125">You may also choose to alert your customers that they may have an unacceptable experience on these parts.</span></span>

## <a name="tests"></a><span data-ttu-id="71659-126">Tests</span><span class="sxs-lookup"><span data-stu-id="71659-126">Tests</span></span>

<span data-ttu-id="71659-127">Bewerten Sie die Leistung und die Leistung auf diesen Geräten:</span><span class="sxs-lookup"><span data-stu-id="71659-127">Evaluate the performance and experience on these devices:</span></span>

-   <span data-ttu-id="71659-128">Wie sieht die endgültige Treiber Version aus?</span><span class="sxs-lookup"><span data-stu-id="71659-128">What is the experience like on the final driver version available?</span></span>
-   <span data-ttu-id="71659-129">Wie sieht das auf msbdd aus?</span><span class="sxs-lookup"><span data-stu-id="71659-129">What is the experience like on the MSBDD?</span></span>

 

 




