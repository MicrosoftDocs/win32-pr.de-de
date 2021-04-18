---
description: Der Installer legt die Eigenschaft productstate bei der Initialisierung auf den Installationsstatus für das Produkt fest.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: Productstate (Eigenschaft)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364506"
---
# <a name="productstate-property"></a><span data-ttu-id="570c4-103">Productstate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="570c4-103">ProductState property</span></span>

<span data-ttu-id="570c4-104">Der Installer legt die Eigenschaft **productstate** bei der Initialisierung auf den Installationsstatus für das Produkt fest.</span><span class="sxs-lookup"><span data-stu-id="570c4-104">The installer sets the **ProductState** property to the installation state for the product at initialization.</span></span> <span data-ttu-id="570c4-105">Diese Eigenschaft wird auf einen der folgenden InstallState-Datentypen festgelegt, die von " [**msiqueryproductstate**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)" zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="570c4-105">This property is set to one of the following INSTALLSTATE data types returned by [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span></span>



| <span data-ttu-id="570c4-106">INSTALLSTATE</span><span class="sxs-lookup"><span data-stu-id="570c4-106">INSTALLSTATE</span></span>             | <span data-ttu-id="570c4-107">Numerischer Wert</span><span class="sxs-lookup"><span data-stu-id="570c4-107">Numeric value</span></span> | <span data-ttu-id="570c4-108">Installationsstatus des Produkts</span><span class="sxs-lookup"><span data-stu-id="570c4-108">Installation state of product</span></span>                   |
|--------------------------|---------------|-------------------------------------------------|
| <span data-ttu-id="570c4-109">InstallState \_ unbekannt</span><span class="sxs-lookup"><span data-stu-id="570c4-109">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="570c4-110">-1</span><span class="sxs-lookup"><span data-stu-id="570c4-110">-1</span></span>            | <span data-ttu-id="570c4-111">Das Produkt wird weder angekündigt noch installiert.</span><span class="sxs-lookup"><span data-stu-id="570c4-111">The product is neither advertised or installed.</span></span> |
| <span data-ttu-id="570c4-112">InstallState \_ angekündigt</span><span class="sxs-lookup"><span data-stu-id="570c4-112">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="570c4-113">1</span><span class="sxs-lookup"><span data-stu-id="570c4-113">1</span></span>             | <span data-ttu-id="570c4-114">Das Produkt wird angekündigt, aber nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="570c4-114">The product is advertised but not installed.</span></span>    |
| <span data-ttu-id="570c4-115">InstallState \_ fehlt.</span><span class="sxs-lookup"><span data-stu-id="570c4-115">INSTALLSTATE\_ABSENT</span></span>     | <span data-ttu-id="570c4-116">2</span><span class="sxs-lookup"><span data-stu-id="570c4-116">2</span></span>             | <span data-ttu-id="570c4-117">Das Produkt wird für einen anderen Benutzer installiert.</span><span class="sxs-lookup"><span data-stu-id="570c4-117">The product is installed for a different user.</span></span>  |
| <span data-ttu-id="570c4-118">InstallState ( \_ Standard)</span><span class="sxs-lookup"><span data-stu-id="570c4-118">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="570c4-119">5</span><span class="sxs-lookup"><span data-stu-id="570c4-119">5</span></span>             | <span data-ttu-id="570c4-120">Das Produkt ist für den aktuellen Benutzer installiert.</span><span class="sxs-lookup"><span data-stu-id="570c4-120">The product is installed for the current user.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="570c4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="570c4-121">Requirements</span></span>



| <span data-ttu-id="570c4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="570c4-122">Requirement</span></span> | <span data-ttu-id="570c4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="570c4-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="570c4-124">Version</span><span class="sxs-lookup"><span data-stu-id="570c4-124">Version</span></span><br/> | <span data-ttu-id="570c4-125">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="570c4-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="570c4-126">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="570c4-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="570c4-127">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="570c4-127">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="570c4-128">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="570c4-128">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="570c4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="570c4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="570c4-130">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="570c4-130">Properties</span></span>](properties.md)
</dt> </dl>

 

 




