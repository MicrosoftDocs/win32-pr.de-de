---
title: WMDM_SESSION_TYPE-Enumeration
description: Der Enumerationstyp für den WMDM- \_ Sitzungstyp \_ definiert den Sitzungstyp.
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- Device Manager der WMDM_SESSION_TYPE-Enumeration Windows Media
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84322986266143e5ff4ecc469c56504f29de9e3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370978"
---
# <a name="wmdm_session_type-enumeration"></a><span data-ttu-id="32a88-104">WMDM \_ - \_ Sitzungstyp-Enumeration</span><span class="sxs-lookup"><span data-stu-id="32a88-104">WMDM\_SESSION\_TYPE enumeration</span></span>

<span data-ttu-id="32a88-105">Der Enumerationstyp für den **WMDM- \_ \_ Sitzungstyp** definiert den Sitzungstyp.</span><span class="sxs-lookup"><span data-stu-id="32a88-105">The **WMDM\_SESSION\_TYPE** enumeration type defines the session type.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a88-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="32a88-106">Syntax</span></span>


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="32a88-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="32a88-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="32a88-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM- \_ Sitzung " \_ None"**</span><span class="sxs-lookup"><span data-stu-id="32a88-108"><span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM\_SESSION\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="32a88-109">Die Sitzung ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="32a88-109">The session is not defined.</span></span>

</dd> <dt>

<span data-ttu-id="32a88-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**WMDM- \_ Sitzungs \_ Übertragung \_ an \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="32a88-110"><span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**WMDM\_SESSION\_TRANSFER\_TO\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="32a88-111">Die Sitzung ist so definiert, dass Daten an das Gerät übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="32a88-111">The session is defined as transferring data to the device.</span></span>

</dd> <dt>

<span data-ttu-id="32a88-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**WMDM- \_ Sitzungs \_ Übertragung \_ von \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="32a88-112"><span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**WMDM\_SESSION\_TRANSFER\_FROM\_DEVICE**</span></span>
</dt> <dd>

<span data-ttu-id="32a88-113">Die Sitzung ist so definiert, dass Daten vom Gerät übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="32a88-113">The session is defined as transferring data from the device.</span></span>

</dd> <dt>

<span data-ttu-id="32a88-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**Löschen der WMDM- \_ Sitzung \_**</span><span class="sxs-lookup"><span data-stu-id="32a88-114"><span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**WMDM\_SESSION\_DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="32a88-115">Die Sitzung wird als Löschen von Daten definiert.</span><span class="sxs-lookup"><span data-stu-id="32a88-115">The session is defined as deleting data.</span></span>

</dd> <dt>

<span data-ttu-id="32a88-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**benutzerdefinierte WMDM- \_ Sitzung \_**</span><span class="sxs-lookup"><span data-stu-id="32a88-116"><span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**WMDM\_SESSION\_CUSTOM**</span></span>
</dt> <dd>

<span data-ttu-id="32a88-117">Die Sitzung wird als benutzerdefinierte Sitzung definiert.</span><span class="sxs-lookup"><span data-stu-id="32a88-117">The session is defined as a custom session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32a88-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32a88-118">Requirements</span></span>



| <span data-ttu-id="32a88-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32a88-119">Requirement</span></span> | <span data-ttu-id="32a88-120">Wert</span><span class="sxs-lookup"><span data-stu-id="32a88-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="32a88-121">Header</span><span class="sxs-lookup"><span data-stu-id="32a88-121">Header</span></span><br/> | <dl> <span data-ttu-id="32a88-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="32a88-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32a88-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32a88-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32a88-124">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="32a88-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





