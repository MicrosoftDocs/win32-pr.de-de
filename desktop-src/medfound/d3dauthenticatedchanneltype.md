---
description: Gibt den Typ des Direct3D-authentifizierten Kanals an.
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
title: D3DAUTHENTICATEDCHANNELTYPE-Enumeration (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5c0cab8a0a208bfb1a005166740dcc64c319c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346662"
---
# <a name="d3dauthenticatedchanneltype-enumeration"></a><span data-ttu-id="ee119-103">D3DAUTHENTICATEDCHANNELTYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ee119-103">D3DAUTHENTICATEDCHANNELTYPE enumeration</span></span>

<span data-ttu-id="ee119-104">Gibt den Typ des Direct3D-authentifizierten Kanals an.</span><span class="sxs-lookup"><span data-stu-id="ee119-104">Specifies the type of Direct3D authenticated channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee119-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee119-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DAUTHENTICATEDCHANNEL_D3D9             = 1,
  D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE  = 2,
  D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE  = 3
} D3DAUTHENTICATEDCHANNELTYPE;
```



## <a name="constants"></a><span data-ttu-id="ee119-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ee119-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ee119-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="ee119-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
</dt> <dd>

<span data-ttu-id="ee119-108">Direct3D 9-Kanal.</span><span class="sxs-lookup"><span data-stu-id="ee119-108">Direct3D 9 channel.</span></span> <span data-ttu-id="ee119-109">Dieser Kanal ermöglicht die Kommunikation mit der Direct3D-Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="ee119-109">This channel provides communication with the Direct3D runtime.</span></span>

</dd> <dt>

<span data-ttu-id="ee119-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="ee119-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>
</dt> <dd>

<span data-ttu-id="ee119-111">Software Treiber Kanal.</span><span class="sxs-lookup"><span data-stu-id="ee119-111">Software driver channel.</span></span> <span data-ttu-id="ee119-112">Dieser Kanal ermöglicht die Kommunikation mit einem Treiber, der Inhalts Schutzmechanismen in Software implementiert.</span><span class="sxs-lookup"><span data-stu-id="ee119-112">This channel provides communication with a driver that implements content protection mechanisms in software.</span></span>

</dd> <dt>

<span data-ttu-id="ee119-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Hardware**</span><span class="sxs-lookup"><span data-stu-id="ee119-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
</dt> <dd>

<span data-ttu-id="ee119-114">Hardware Treiber Kanal.</span><span class="sxs-lookup"><span data-stu-id="ee119-114">Hardware driver channel.</span></span> <span data-ttu-id="ee119-115">Dieser Kanal ermöglicht die Kommunikation mit einem Treiber, der Inhalts Schutzmechanismen in der GPU-Hardware implementiert.</span><span class="sxs-lookup"><span data-stu-id="ee119-115">This channel provides communication with a driver that implements content protection mechanisms in the GPU hardware.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee119-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee119-116">Requirements</span></span>



| <span data-ttu-id="ee119-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee119-117">Requirement</span></span> | <span data-ttu-id="ee119-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ee119-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee119-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee119-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee119-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee119-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ee119-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee119-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee119-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee119-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ee119-123">Header</span><span class="sxs-lookup"><span data-stu-id="ee119-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee119-124"><dt>D3d9types. h (Include d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee119-124"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee119-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee119-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee119-126">Direct3D-videoenumerationen</span><span class="sxs-lookup"><span data-stu-id="ee119-126">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> <dt>

[<span data-ttu-id="ee119-127">**IDirect3DDevice9Video:: kreateauthentiinitiedchannel**</span><span class="sxs-lookup"><span data-stu-id="ee119-127">**IDirect3DDevice9Video::CreateAuthenticatedChannel**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)
</dt> </dl>

 

 




