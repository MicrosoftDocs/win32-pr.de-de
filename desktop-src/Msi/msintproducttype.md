---
description: Der Installer legt die msintproducttype-Eigenschaft für Windows NT, Windows 2000 und spätere Betriebssysteme fest.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Msintproducttype (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361351"
---
# <a name="msintproducttype-property"></a><span data-ttu-id="bc0b4-103">Msintproducttype (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bc0b4-103">MsiNTProductType property</span></span>

<span data-ttu-id="bc0b4-104">Der Installer legt die **msintproducttype** -Eigenschaft für Windows NT, Windows 2000 und spätere Betriebssysteme fest.</span><span class="sxs-lookup"><span data-stu-id="bc0b4-104">The installer sets the **MsiNTProductType** property for Windows NT, Windows 2000, and later operating systems.</span></span> <span data-ttu-id="bc0b4-105">Diese Eigenschaft gibt den Windows-Produkttyp an.</span><span class="sxs-lookup"><span data-stu-id="bc0b4-105">This property indicates the Windows product type.</span></span>

<span data-ttu-id="bc0b4-106">Für Windows 2000 und spätere Betriebssysteme legt das Installationsprogramm die folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="bc0b4-106">For Windows 2000 and later operating systems, the installer sets the following values.</span></span> <span data-ttu-id="bc0b4-107">Beachten Sie, dass die Werte mit dem Feld **wProductType** der [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) -Struktur identisch sind.</span><span class="sxs-lookup"><span data-stu-id="bc0b4-107">Note that values are the same as of the **wProductType** field of the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span>



| <span data-ttu-id="bc0b4-108">Wert</span><span class="sxs-lookup"><span data-stu-id="bc0b4-108">Value</span></span> | <span data-ttu-id="bc0b4-109">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bc0b4-109">Meaning</span></span>                                  |
|-------|------------------------------------------|
| <span data-ttu-id="bc0b4-110">1</span><span class="sxs-lookup"><span data-stu-id="bc0b4-110">1</span></span>     | <span data-ttu-id="bc0b4-111">Windows 2000 Professional und höher</span><span class="sxs-lookup"><span data-stu-id="bc0b4-111">Windows 2000 Professional and later</span></span>      |
| <span data-ttu-id="bc0b4-112">2</span><span class="sxs-lookup"><span data-stu-id="bc0b4-112">2</span></span>     | <span data-ttu-id="bc0b4-113">Windows 2000-Domänen Controller und höher</span><span class="sxs-lookup"><span data-stu-id="bc0b4-113">Windows 2000 domain controller and later</span></span> |
| <span data-ttu-id="bc0b4-114">3</span><span class="sxs-lookup"><span data-stu-id="bc0b4-114">3</span></span>     | <span data-ttu-id="bc0b4-115">Windows 2000-Server und höher</span><span class="sxs-lookup"><span data-stu-id="bc0b4-115">Windows 2000 Server and later</span></span>            |



 

<span data-ttu-id="bc0b4-116">Für ältere Betriebssysteme als Windows 2000 legt das Installationsprogramm die folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="bc0b4-116">For operating systems earlier than Windows 2000, the installer sets the following values.</span></span>



| <span data-ttu-id="bc0b4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bc0b4-117">Value</span></span> | <span data-ttu-id="bc0b4-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bc0b4-118">Meaning</span></span>                      |
|-------|------------------------------|
| <span data-ttu-id="bc0b4-119">1</span><span class="sxs-lookup"><span data-stu-id="bc0b4-119">1</span></span>     | <span data-ttu-id="bc0b4-120">Windows NT-Arbeitsstation</span><span class="sxs-lookup"><span data-stu-id="bc0b4-120">Windows NT Workstation</span></span>       |
| <span data-ttu-id="bc0b4-121">2</span><span class="sxs-lookup"><span data-stu-id="bc0b4-121">2</span></span>     | <span data-ttu-id="bc0b4-122">Windows NT-Domänen Controller</span><span class="sxs-lookup"><span data-stu-id="bc0b4-122">Windows NT domain controller</span></span> |
| <span data-ttu-id="bc0b4-123">3</span><span class="sxs-lookup"><span data-stu-id="bc0b4-123">3</span></span>     | <span data-ttu-id="bc0b4-124">Windows NT-Server</span><span class="sxs-lookup"><span data-stu-id="bc0b4-124">Windows NT Server</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="bc0b4-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc0b4-125">Requirements</span></span>



| <span data-ttu-id="bc0b4-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc0b4-126">Requirement</span></span> | <span data-ttu-id="bc0b4-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bc0b4-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0b4-128">Version</span><span class="sxs-lookup"><span data-stu-id="bc0b4-128">Version</span></span><br/> | <span data-ttu-id="bc0b4-129">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bc0b4-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bc0b4-130">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bc0b4-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bc0b4-131">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bc0b4-131">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bc0b4-132">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="bc0b4-132">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc0b4-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc0b4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc0b4-134">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bc0b4-134">Properties</span></span>](properties.md)
</dt> </dl>

 

 
