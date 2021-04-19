---
description: Das vorhanden sein der msiinstanceguid-Eigenschaft gibt an, dass ein Produktcode&\# 8211; Ändern der Transformation für das Produkt registriert ist.
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: Msiinstanceguid (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c798d56cf3ede6a75a133dd7e0ec7f42c32e84f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354054"
---
# <a name="msiinstanceguid-property"></a><span data-ttu-id="7df6b-103">Msiinstanceguid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7df6b-103">MSIINSTANCEGUID property</span></span>

<span data-ttu-id="7df6b-104">Das vorhanden sein der **msiinstanceguid** -Eigenschaft gibt an, dass ein Product Code – Changing Transform für das Produkt registriert ist.</span><span class="sxs-lookup"><span data-stu-id="7df6b-104">The presence of the **MSIINSTANCEGUID** property indicates that a product code–changing transform is registered to the product.</span></span> <span data-ttu-id="7df6b-105">Der Wert der **msiinstanceguid** -Eigenschaft gibt an, welche Instanz eines Produkts für die Installation verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7df6b-105">The value of the **MSIINSTANCEGUID** property specifies which instance of a product is to be used for installation.</span></span> <span data-ttu-id="7df6b-106">Die **msiinstanceguid** -Eigenschaft kann nur auf ein Produkt verweisen, das bereits mit einer instanztransformation installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7df6b-106">The **MSIINSTANCEGUID** property can only reference a product that has already been installed with an instance transform.</span></span>

<span data-ttu-id="7df6b-107">Instanztransformationen sind Produktcode – veränderliche Transformationen, die mit dem Installationsprogramm verfügbar sind, das unter Windows Server 2003 oder Windows XP ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7df6b-107">Instance transforms are product code–changing transforms available with the installer running on either Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7df6b-108">Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="7df6b-108">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7df6b-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7df6b-109">Requirements</span></span>



| <span data-ttu-id="7df6b-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7df6b-110">Requirement</span></span> | <span data-ttu-id="7df6b-111">Wert</span><span class="sxs-lookup"><span data-stu-id="7df6b-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df6b-112">Version</span><span class="sxs-lookup"><span data-stu-id="7df6b-112">Version</span></span><br/> | <span data-ttu-id="7df6b-113">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7df6b-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7df6b-114">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7df6b-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7df6b-115">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7df6b-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7df6b-116">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="7df6b-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7df6b-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7df6b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df6b-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7df6b-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="7df6b-119">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7df6b-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




