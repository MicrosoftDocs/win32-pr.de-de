---
title: RAS_PARAMETERS Struktur (rassapi. h)
description: Die Struktur der RAS- \_ Parameter wird von der rasadminportgetinfo-Funktion verwendet, um den Namen und den Wert eines medienspezifischen Parameters zurückzugeben, der einem Port auf einem RAS-Server zugeordnet ist.
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS_PARAMETERS Struktur-RAS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffaefa8a6f2cffb895cc18882ed8fc0c382a4bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518521"
---
# <a name="ras_parameters-structure"></a><span data-ttu-id="42b17-104">Struktur der RAS- \_ Parameter</span><span class="sxs-lookup"><span data-stu-id="42b17-104">RAS\_PARAMETERS structure</span></span>

<span data-ttu-id="42b17-105">\[Die Struktur der **RAS- \_ Parameter** wird ab Windows Vista nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="42b17-105">\[The **RAS\_PARAMETERS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="42b17-106">Die Struktur der **RAS- \_ Parameter** wird von der [**rasadminportgetinfo**](rasadminportgetinfo.md) -Funktion verwendet, um den Namen und den Wert eines medienspezifischen Parameters zurückzugeben, der einem Port auf einem RAS-Server zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="42b17-106">The **RAS\_PARAMETERS** structure is used by the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function to return the name and value of a media-specific parameter associated with a port on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b17-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="42b17-107">Syntax</span></span>


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="42b17-108">Member</span><span class="sxs-lookup"><span data-stu-id="42b17-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="42b17-109">**P- \_ Taste**</span><span class="sxs-lookup"><span data-stu-id="42b17-109">**P\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="42b17-110">Gibt den Namen des Schlüssels an, der den medienspezifischen Parameter darstellt, z. b. maxconnectbit/s.</span><span class="sxs-lookup"><span data-stu-id="42b17-110">Specifies the name of the key that represents the media-specific parameter, such as MAXCONNECTBPS.</span></span>

</dd> <dt>

<span data-ttu-id="42b17-111">**P- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="42b17-111">**P\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="42b17-112">Identifiziert den Typ der Daten, die dem-Parameter zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="42b17-112">Identifies the type of data associated with the parameter.</span></span> <span data-ttu-id="42b17-113">Dieser Member kann einer der folgenden Werte aus der RAS- [**\_ parametriams- \_ formatenumeration**](ras-params-format-str.md) sein.</span><span class="sxs-lookup"><span data-stu-id="42b17-113">This member can be one of the following values from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration.</span></span>



| <span data-ttu-id="42b17-114">Wert</span><span class="sxs-lookup"><span data-stu-id="42b17-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="42b17-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="42b17-115">Meaning</span></span>                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <span data-ttu-id="42b17-116"><dt>**ParamNumber**</dt></span><span class="sxs-lookup"><span data-stu-id="42b17-116"><dt>**ParamNumber**</dt></span></span> </dl> | <span data-ttu-id="42b17-117">Gibt an, dass die dem Schlüssel zugeordneten Daten eine Zahl sind.</span><span class="sxs-lookup"><span data-stu-id="42b17-117">Indicates that the data associated with the key is a number.</span></span><br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <span data-ttu-id="42b17-118"><dt>**ParamString**</dt></span><span class="sxs-lookup"><span data-stu-id="42b17-118"><dt>**ParamString**</dt></span></span> </dl> | <span data-ttu-id="42b17-119">Gibt an, dass die dem Schlüssel zugeordneten Daten eine Zeichenfolge sind.</span><span class="sxs-lookup"><span data-stu-id="42b17-119">Indicates that the data associated with the key is a string.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="42b17-120">**P- \_ Attribute**</span><span class="sxs-lookup"><span data-stu-id="42b17-120">**P\_Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="42b17-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="42b17-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="42b17-122">**P- \_ Wert**</span><span class="sxs-lookup"><span data-stu-id="42b17-122">**P\_Value**</span></span>
</dt> <dd>

<span data-ttu-id="42b17-123">Gibt den Wert an, der dem Parameter zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="42b17-123">Specifies the value associated with the parameter.</span></span> <span data-ttu-id="42b17-124">Dieser Member ist ein [**RAS-Parameter \_ \_ Wert**](ras-params-value-str.md) Union.</span><span class="sxs-lookup"><span data-stu-id="42b17-124">This member is a [**RAS\_PARAMS\_VALUE**](ras-params-value-str.md) union.</span></span> <span data-ttu-id="42b17-125">Wenn der **P- \_ Typmember** eine paramnumber ist, enthält der **Number** -Member der Union den Wert.</span><span class="sxs-lookup"><span data-stu-id="42b17-125">If the **P\_Type** member is ParamNumber, the **Number** member of the union contains the value.</span></span> <span data-ttu-id="42b17-126">Wenn der **P- \_ Typ** paramString ist, enthält der **Zeichen** folgen Member der Union den Wert.</span><span class="sxs-lookup"><span data-stu-id="42b17-126">If **P\_Type** is ParamString, the **String** member of the union contains the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42b17-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42b17-127">Requirements</span></span>



| <span data-ttu-id="42b17-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42b17-128">Requirement</span></span> | <span data-ttu-id="42b17-129">Wert</span><span class="sxs-lookup"><span data-stu-id="42b17-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42b17-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42b17-130">Minimum supported client</span></span><br/> | <span data-ttu-id="42b17-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42b17-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="42b17-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42b17-132">Minimum supported server</span></span><br/> | <span data-ttu-id="42b17-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42b17-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="42b17-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="42b17-134">End of client support</span></span><br/>    | <span data-ttu-id="42b17-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="42b17-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="42b17-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="42b17-136">End of server support</span></span><br/>    | <span data-ttu-id="42b17-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42b17-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="42b17-138">Header</span><span class="sxs-lookup"><span data-stu-id="42b17-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="42b17-139"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="42b17-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42b17-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42b17-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b17-141">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="42b17-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="42b17-142">RAS-Server-Verwaltungsstrukturen</span><span class="sxs-lookup"><span data-stu-id="42b17-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="42b17-143">**Rasadminakzeptnewconnection**</span><span class="sxs-lookup"><span data-stu-id="42b17-143">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="42b17-144">**Rasadminconnectionhangupnotification**</span><span class="sxs-lookup"><span data-stu-id="42b17-144">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="42b17-145">**Rasadminportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="42b17-145">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





