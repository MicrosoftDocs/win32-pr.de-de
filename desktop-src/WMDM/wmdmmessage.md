---
title: Wmdmmess-Enumeration
description: Der wmdmmess-Enumerationstyp definiert Nachrichten Typen und-Zustände.
ms.assetid: 49a77100-8890-4e40-852f-c6fd436f22c5
keywords:
- Wmdmmess-Enumeration Windows Media Device Manager
topic_type:
- apiref
api_name:
- WMDMMessage
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489dc7059f10e1a6f61d1a290f8f664a385f96c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364447"
---
# <a name="wmdmmessage-enumeration"></a><span data-ttu-id="ee3b5-104">Wmdmmess-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ee3b5-104">WMDMMessage enumeration</span></span>

<span data-ttu-id="ee3b5-105">Der **wmdmmess** -Enumerationstyp definiert Nachrichten Typen und-Zustände.</span><span class="sxs-lookup"><span data-stu-id="ee3b5-105">The **WMDMMessage** enumeration type defines message types and states.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee3b5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee3b5-106">Syntax</span></span>


```C++
enum WMDMMessage {
  WMDM_MSG_DEVICE_ARRIVAL, 
  WMDM_MSG_DEVICE_REMOVAL, 
  WMDM_MSG_MEDIA_ARRIVAL, 
  WMDM_MSG_MEDIA_REMOVAL 

};
```



## <a name="constants"></a><span data-ttu-id="ee3b5-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ee3b5-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ee3b5-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**WMDM-Meldung \_ \_ Geräte \_ Ankunft**</span><span class="sxs-lookup"><span data-stu-id="ee3b5-108"><span id="WMDM_MSG_DEVICE_ARRIVAL"></span><span id="wmdm_msg_device_arrival"></span>**WMDM\_MSG\_DEVICE\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="ee3b5-109">Ein Windows Media Device Manager-Gerät wurde angeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ee3b5-109">A Windows Media Device Manager device has been plugged in.</span></span>

</dd> <dt>

<span data-ttu-id="ee3b5-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**WMDM-Meldung \_ \_ Geräte \_ Entfernung**</span><span class="sxs-lookup"><span data-stu-id="ee3b5-110"><span id="WMDM_MSG_DEVICE_REMOVAL"></span><span id="wmdm_msg_device_removal"></span>**WMDM\_MSG\_DEVICE\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="ee3b5-111">Ein Windows Media Device Manager-Gerät wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="ee3b5-111">A Windows Media Device Manager device has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="ee3b5-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM- \_ msg- \_ Medien \_ Ankunft**</span><span class="sxs-lookup"><span data-stu-id="ee3b5-112"><span id="WMDM_MSG_MEDIA_ARRIVAL"></span><span id="wmdm_msg_media_arrival"></span>**WMDM\_MSG\_MEDIA\_ARRIVAL**</span></span>
</dt> <dd>

<span data-ttu-id="ee3b5-113">Medien wurden in ein Windows Media Device Manager-Gerät eingefügt.</span><span class="sxs-lookup"><span data-stu-id="ee3b5-113">Media has been inserted in a Windows Media Device Manager device.</span></span>

</dd> <dt>

<span data-ttu-id="ee3b5-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**Entfernen von WMDM- \_ msg- \_ Medien \_**</span><span class="sxs-lookup"><span data-stu-id="ee3b5-114"><span id="WMDM_MSG_MEDIA_REMOVAL"></span><span id="wmdm_msg_media_removal"></span>**WMDM\_MSG\_MEDIA\_REMOVAL**</span></span>
</dt> <dd>

<span data-ttu-id="ee3b5-115">Das Medium wurde von einem Windows Media Device Manager-Gerät entfernt.</span><span class="sxs-lookup"><span data-stu-id="ee3b5-115">Media has been removed from a Windows Media Device Manager device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee3b5-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee3b5-116">Requirements</span></span>



| <span data-ttu-id="ee3b5-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee3b5-117">Requirement</span></span> | <span data-ttu-id="ee3b5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ee3b5-118">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ee3b5-119">Header</span><span class="sxs-lookup"><span data-stu-id="ee3b5-119">Header</span></span><br/> | <dl> <span data-ttu-id="ee3b5-120"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ee3b5-120"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee3b5-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee3b5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee3b5-122">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="ee3b5-122">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





