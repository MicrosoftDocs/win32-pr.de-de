---
title: Imsrdppreferredredirectioninfo-Schnittstelle
description: Stellt eine Eigenschaft bereit, die mithilfe eines Umleitungs Servers gesteuert werden soll.
ms.assetid: 1EAD9B15-4A84-4179-8A92-F0736B04B4F1
ms.tgt_platform: multiple
keywords:
- Imsrdppreferredredirectioninfo-Schnittstelle Remotedesktopdienste
- Imsrdppreferredredirectioninfo-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpPreferredRedirectionInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8ea28c36ca06548128954298e35c0cc20de5b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475618"
---
# <a name="imsrdppreferredredirectioninfo-interface"></a><span data-ttu-id="ca162-105">Imsrdppreferredredirectioninfo-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ca162-105">IMsRdpPreferredRedirectionInfo interface</span></span>

<span data-ttu-id="ca162-106">Stellt eine Eigenschaft bereit, die mithilfe eines Umleitungs Servers gesteuert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca162-106">Provides a property to control using a redirection server.</span></span>

## <a name="members"></a><span data-ttu-id="ca162-107">Member</span><span class="sxs-lookup"><span data-stu-id="ca162-107">Members</span></span>

<span data-ttu-id="ca162-108">Die **imsrdppreferredredirectioninfo** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ca162-108">The **IMsRdpPreferredRedirectionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ca162-109">**Imsrdppreferredredirectioninfo** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ca162-109">**IMsRdpPreferredRedirectionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="ca162-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca162-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca162-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ca162-111">Properties</span></span>

<span data-ttu-id="ca162-112">Die **imsrdppreferredredirectioninfo** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ca162-112">The **IMsRdpPreferredRedirectionInfo** interface has these properties.</span></span>



| <span data-ttu-id="ca162-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ca162-113">Property</span></span>                                                                                               | <span data-ttu-id="ca162-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="ca162-114">Access type</span></span>           | <span data-ttu-id="ca162-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca162-115">Description</span></span>                                                          |
|:-------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="ca162-116">**Useredirectionservername**</span><span class="sxs-lookup"><span data-stu-id="ca162-116">**UseRedirectionServerName**</span></span>](imsrdppreferredredirectioninfo-useredirectionservername.md)<br/> | <span data-ttu-id="ca162-117">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ca162-117">Read/write</span></span><br/> | <span data-ttu-id="ca162-118">Ruft ab und legt fest, ob der Umleitungs Servername verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca162-118">Gets and sets whether to use the redirection server name.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ca162-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca162-119">Requirements</span></span>



| <span data-ttu-id="ca162-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca162-120">Requirement</span></span> | <span data-ttu-id="ca162-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ca162-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca162-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca162-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ca162-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ca162-123">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="ca162-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca162-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ca162-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ca162-125">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="ca162-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ca162-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="ca162-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca162-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ca162-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ca162-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca162-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca162-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ca162-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="ca162-130">CLSID</span></span><br/>                    | <span data-ttu-id="ca162-131">CLSID- \_ MsRdpClient10 ist als C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24 definiert.</span><span class="sxs-lookup"><span data-stu-id="ca162-131">CLSID\_MsRdpClient10 is defined as C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span></span><br/> <span data-ttu-id="ca162-132">CLSID- \_ MsRdpClient10NotSafeForScripting ist als A0C63C30-F08D-4AB4-907C-34905D770C7D definiert.</span><span class="sxs-lookup"><span data-stu-id="ca162-132">CLSID\_MsRdpClient10NotSafeForScripting is defined as A0C63C30-F08D-4AB4-907C-34905D770C7D</span></span><br/> <span data-ttu-id="ca162-133">CLSID- \_ MsRdpClient7 ist als A9D7038D-B5ED-472E-9C47-94BEA90A5910 definiert.</span><span class="sxs-lookup"><span data-stu-id="ca162-133">CLSID\_MsRdpClient7 is defined as A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span><br/> <span data-ttu-id="ca162-134">CLSID \_ MsRdpClient7NotSafeForScripting ist als 54d38bf 7-b1ef-4479-9674-1bd6ea465258 definiert.</span><span class="sxs-lookup"><span data-stu-id="ca162-134">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span><br/> <span data-ttu-id="ca162-135">CLSID \_ MsRdpClient8 ist als 5f681803-2900-4c43-a1cc-cf405404a676 definiert.</span><span class="sxs-lookup"><span data-stu-id="ca162-135">CLSID\_MsRdpClient8 is defined as 5F681803-2900-4C43-A1CC-CF405404A676</span></span><br/> <span data-ttu-id="ca162-136">CLSID- \_ MsRdpClient8NotSafeForScripting ist als A3BC03A0-041D-42E3-AD22-882B7865C9C5 definiert.</span><span class="sxs-lookup"><span data-stu-id="ca162-136">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="ca162-137">CLSID \_ MsRdpClient9 ist als 301b94ba-5d25-4a12-bffe-3b6e7a616585 definiert</span><span class="sxs-lookup"><span data-stu-id="ca162-137">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="ca162-138">CLSID \_ MsRdpClient9NotSafeForScripting ist als 8b918b82-7985-4c24-89df-c33ad2bbfbcd definiert.</span><span class="sxs-lookup"><span data-stu-id="ca162-138">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="ca162-139">IID</span><span class="sxs-lookup"><span data-stu-id="ca162-139">IID</span></span><br/>                      | <span data-ttu-id="ca162-140">IID \_ imsrdppreferredredirectioninfo ist als FDD029F9-9574-4DEF-8529-64B521CCCAA4 definiert.</span><span class="sxs-lookup"><span data-stu-id="ca162-140">IID\_IMsRdpPreferredRedirectionInfo is defined as FDD029F9-9574-4DEF-8529-64B521CCCAA4</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

