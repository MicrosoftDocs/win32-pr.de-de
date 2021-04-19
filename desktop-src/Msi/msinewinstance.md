---
description: Die msinewinstance-Eigenschaft gibt die Installation einer neuen Instanz eines Produkts mit instanztransformationen an.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: Msinewinstance (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8b51ec02d7b30c42e6e400b6a6177d7ef47d88c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373856"
---
# <a name="msinewinstance-property"></a><span data-ttu-id="bc858-103">Msinewinstance (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bc858-103">MSINEWINSTANCE property</span></span>

<span data-ttu-id="bc858-104">Die **msinewinstance** -Eigenschaft gibt die Installation einer neuen Instanz eines Produkts mit instanztransformationen an.</span><span class="sxs-lookup"><span data-stu-id="bc858-104">The **MSINEWINSTANCE** property indicates the installation of a new instance of a product with instance transforms.</span></span> <span data-ttu-id="bc858-105">Diese Eigenschaft unterstützt mehrere Instanzen durch Produktcode – veränderliche Transformationen.</span><span class="sxs-lookup"><span data-stu-id="bc858-105">This property supports multiple instances through product code–changing transforms.</span></span> <span data-ttu-id="bc858-106">Der Wert dieser Eigenschaft ist 1.</span><span class="sxs-lookup"><span data-stu-id="bc858-106">The value of this property is 1.</span></span> <span data-ttu-id="bc858-107">Wenn diese Eigenschaft in der Befehlszeile vorhanden ist, muss auch die [**Transformationen**](transforms.md) -Eigenschaft vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="bc858-107">The presence of this property on the command line requires that the [**TRANSFORMS**](transforms.md) property also be present.</span></span> <span data-ttu-id="bc858-108">Die erste in **Transformationen** aufgelistete Transformation muss eine instanztransformation sein.</span><span class="sxs-lookup"><span data-stu-id="bc858-108">The first transform listed in **TRANSFORMS** must be an instance transform.</span></span> <span data-ttu-id="bc858-109">Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md) .</span><span class="sxs-lookup"><span data-stu-id="bc858-109">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md)</span></span>

<span data-ttu-id="bc858-110">Diese Eigenschaft ist für das Installationsprogramm verfügbar, das ein System in Windows Server 2003 oder Windows XP ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bc858-110">This property is available with the installer running a system in the Windows Server 2003 or Windows XP.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc858-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc858-111">Requirements</span></span>



| <span data-ttu-id="bc858-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc858-112">Requirement</span></span> | <span data-ttu-id="bc858-113">Wert</span><span class="sxs-lookup"><span data-stu-id="bc858-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc858-114">Version</span><span class="sxs-lookup"><span data-stu-id="bc858-114">Version</span></span><br/> | <span data-ttu-id="bc858-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bc858-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bc858-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bc858-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bc858-117">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bc858-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bc858-118">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="bc858-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc858-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc858-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc858-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc858-120">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="bc858-121">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bc858-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




