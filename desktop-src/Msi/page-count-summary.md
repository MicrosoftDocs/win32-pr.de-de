---
description: Die Zusammenfassungs Eigenschaft Seitenanzahl enthält die für das Installationspaket erforderliche mindestinstallerversion.
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: Zusammenfassungs Eigenschaft für Seitenanzahl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ec5e319450bb7a7db5515587be7777ad3e657d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367674"
---
# <a name="page-count-summary-property"></a><span data-ttu-id="c7cc5-103">Zusammenfassungs Eigenschaft für Seitenanzahl</span><span class="sxs-lookup"><span data-stu-id="c7cc5-103">Page Count Summary property</span></span>

<span data-ttu-id="c7cc5-104">Die **Zusammenfassungs Eigenschaft Seitenanzahl** enthält die für das Installationspaket erforderliche mindestinstallerversion.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-104">The **Page Count Summary** property contains the minimum installer version required by the installation package.</span></span> <span data-ttu-id="c7cc5-105">Für mindestens Windows Installer 2,0 muss diese Eigenschaft auf die ganze Zahl 200 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-105">For a minimum of Windows Installer 2.0, this property must be set to the integer 200.</span></span> <span data-ttu-id="c7cc5-106">Für mindestens Windows Installer 3,0 muss diese Eigenschaft auf die ganze Zahl 300 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-106">For a minimum of Windows Installer 3.0, this property must be set to the integer 300.</span></span> <span data-ttu-id="c7cc5-107">Für mindestens Windows Installer 3,1 muss diese Eigenschaft auf 301 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-107">For a minimum of Windows Installer 3.1, this property must be set to 301.</span></span> <span data-ttu-id="c7cc5-108">Für mindestens Windows Installer 4,5 muss diese Eigenschaft auf 405 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-108">For a minimum of Windows Installer 4.5, this property must be set to 405.</span></span> <span data-ttu-id="c7cc5-109">Für mindestens Windows Installer 5,0 muss diese Eigenschaft auf 500 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-109">For a minimum of Windows Installer 5.0, this property must be set to 500.</span></span>

<span data-ttu-id="c7cc5-110">Bei [64-Bit-Windows Installer Paketen](64-bit-windows-installer-packages.md)muss diese Eigenschaft auf die ganze Zahl 200 oder höher festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-110">For [64-bit Windows Installer Packages](64-bit-windows-installer-packages.md), this property must be set to the integer 200 or greater.</span></span> <span data-ttu-id="c7cc5-111">Bei 64-Bit-Windows Installer Paketen auf der Arm64-Plattform muss diese Eigenschaft auf die ganze Zahl 500 oder höher festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-111">For 64-bit Windows Installer Packages on the Arm64 platform, this property must be set to the integer 500 or greater.</span></span>

<span data-ttu-id="c7cc5-112">Bei einem Transformations Paket enthält die **Zusammenfassungs Eigenschaft Seitenanzahl** die mindestinstallerversion, die zum Verarbeiten der Transformation erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-112">For a transform package, the **Page Count Summary** property contains the minimum installer version required to process the transform.</span></span> <span data-ttu-id="c7cc5-113">Legen Sie auf die größere der beiden **Zusammenfassungs** Eigenschaftswerte der Seitenanzahl fest, die zu den Datenbanken gehören, die zum Generieren der Transformation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-113">Set to the greater of the two **Page Count Summary** property values that belong to the databases used to generate the transform.</span></span>

<span data-ttu-id="c7cc5-114">Bei einem Patchpaket wird die **Zusammenfassungs Eigenschaft der Seitenanzahl** auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-114">For a patch package, the **Page Count Summary** property is set to Null.</span></span>

<span data-ttu-id="c7cc5-115">Diese Zusammenfassungs Eigenschaft ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-115">This summary property is required.</span></span>

<span data-ttu-id="c7cc5-116">Diese Eigenschaft kann verwendet werden, um ein Paket zu erstellen, das nur mit der angegebenen Mindestversion oder einer höheren Version des Windows Installer installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-116">This property can be used to author a package that can be installed only by the specified minimum or later version of the Windows Installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7cc5-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7cc5-117">Requirements</span></span>



| <span data-ttu-id="c7cc5-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7cc5-118">Requirement</span></span> | <span data-ttu-id="c7cc5-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c7cc5-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7cc5-120">Version</span><span class="sxs-lookup"><span data-stu-id="c7cc5-120">Version</span></span><br/> | <span data-ttu-id="c7cc5-121">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c7cc5-122">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c7cc5-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c7cc5-123">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7cc5-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7cc5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7cc5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7cc5-125">Beschreibungen der Zusammenfassungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c7cc5-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




