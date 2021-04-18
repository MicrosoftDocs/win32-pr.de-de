---
title: IMsRdpClientSecuredSettings2-Schnittstelle
description: Definiert zusätzliche Eigenschaften des Remotedesktop ActiveX-Steuer Elements, die auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt sind.
ms.assetid: dde9824c-7adf-4783-bb1a-fb2bdbb7aead
ms.tgt_platform: multiple
keywords:
- IMsRdpClientSecuredSettings2-Schnittstelle Remotedesktopdienste
- IMsRdpClientSecuredSettings2 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8ceaf322b51a4b619f8d73a898c444706d61f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338729"
---
# <a name="imsrdpclientsecuredsettings2-interface"></a><span data-ttu-id="ebcd6-105">IMsRdpClientSecuredSettings2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ebcd6-105">IMsRdpClientSecuredSettings2 interface</span></span>

<span data-ttu-id="ebcd6-106">Definiert zusätzliche Eigenschaften des Remotedesktop ActiveX-Steuer Elements, die auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="ebcd6-106">Defines additional properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span>

## <a name="members"></a><span data-ttu-id="ebcd6-107">Member</span><span class="sxs-lookup"><span data-stu-id="ebcd6-107">Members</span></span>

<span data-ttu-id="ebcd6-108">Die **IMsRdpClientSecuredSettings2** -Schnittstelle erbt von [**imsrdpclientsecuredsettings**](imsrdpclientsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="ebcd6-108">The **IMsRdpClientSecuredSettings2** interface inherits from [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md).</span></span> <span data-ttu-id="ebcd6-109">**IMsRdpClientSecuredSettings2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ebcd6-109">**IMsRdpClientSecuredSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="ebcd6-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ebcd6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ebcd6-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ebcd6-111">Properties</span></span>

<span data-ttu-id="ebcd6-112">Die **IMsRdpClientSecuredSettings2** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ebcd6-112">The **IMsRdpClientSecuredSettings2** interface has these properties.</span></span>



| <span data-ttu-id="ebcd6-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ebcd6-113">Property</span></span>                                                   | <span data-ttu-id="ebcd6-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="ebcd6-114">Access type</span></span>           | <span data-ttu-id="ebcd6-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebcd6-115">Description</span></span>                                                                                                          |
|:-----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ebcd6-116">**PCB**</span><span class="sxs-lookup"><span data-stu-id="ebcd6-116">**PCB**</span></span>](imsrdpclientsecuredsettings2-pcb.md)<br/> | <span data-ttu-id="ebcd6-117">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ebcd6-117">Read/write</span></span><br/> | <span data-ttu-id="ebcd6-118">Gibt die Einstellung für die Vorverbindungs-BLOB (Festplatte) an, die vor der Verbindungs Herstellung mit dem Server verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ebcd6-118">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ebcd6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ebcd6-119">Requirements</span></span>



| <span data-ttu-id="ebcd6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ebcd6-120">Requirement</span></span> | <span data-ttu-id="ebcd6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ebcd6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebcd6-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ebcd6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ebcd6-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ebcd6-123">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="ebcd6-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ebcd6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ebcd6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ebcd6-125">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="ebcd6-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ebcd6-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="ebcd6-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebcd6-127"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="ebcd6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ebcd6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebcd6-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebcd6-129"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="ebcd6-130">IID</span><span class="sxs-lookup"><span data-stu-id="ebcd6-130">IID</span></span><br/>                      | <span data-ttu-id="ebcd6-131">IID \_ imsrdpclientsecuredsettings ist als 25F & 2ce20-8b1d-4971-A7CD-549dae201fc0 definiert.</span><span class="sxs-lookup"><span data-stu-id="ebcd6-131">IID\_IMsRdpClientSecuredSettings is defined as 25f2ce20-8b1d-4971-a7cd-549dae201fc0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebcd6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ebcd6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebcd6-133">**Imsrdpclientsecuredsettings**</span><span class="sxs-lookup"><span data-stu-id="ebcd6-133">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





