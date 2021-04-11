---
title: RAS_PARAMS_VALUE Union (rassapi. h)
description: Die RAS- \_ \_ Parameterwert-Union wird in der Struktur der RAS- \_ Parameter verwendet, um die Daten zu speichern, die mit einem medienspezifischen Parameter verknüpft sind.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS_PARAMS_VALUE Union RAS
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f8cc6d693b32b1bbe6f05e8d32ca31a48cfb29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102831"
---
# <a name="ras_params_value-union"></a><span data-ttu-id="44e0a-104">RAS-Parameter \_ \_ Wert Union</span><span class="sxs-lookup"><span data-stu-id="44e0a-104">RAS\_PARAMS\_VALUE union</span></span>

<span data-ttu-id="44e0a-105">\[Die **RAS- \_ parametriams- \_ Wert** Union wird ab Windows Vista nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="44e0a-105">\[The **RAS\_PARAMS\_VALUE** union is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="44e0a-106">Die **RAS- \_ \_ Parameterwert** -Union wird in der Struktur der [**RAS- \_ Parameter**](ras-parameters-str.md) verwendet, um die Daten zu speichern, die mit einem medienspezifischen Parameter verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="44e0a-106">The **RAS\_PARAMS\_VALUE** union is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to store the data associated with a media-specific parameter.</span></span> <span data-ttu-id="44e0a-107">Der P-Typmember der **RAS \_ -Parameter** Struktur verwendet einen Wert aus der RAS- **\_ parameterformatenumeration** , um den Typ des Werts anzugeben, der derzeit in einem RAS-Parameter **\_ \_ Wert** gespeichert wird. [**\_ \_**](ras-params-format-str.md)</span><span class="sxs-lookup"><span data-stu-id="44e0a-107">The **P\_Type** member of the **RAS\_PARAMETERS** structure uses a value from the [**RAS\_PARAMS\_FORMAT**](ras-params-format-str.md) enumeration to indicate the type of value currently stored in **RAS\_PARAMS\_VALUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e0a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="44e0a-108">Syntax</span></span>


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a><span data-ttu-id="44e0a-109">Member</span><span class="sxs-lookup"><span data-stu-id="44e0a-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="44e0a-110">**Number**</span><span class="sxs-lookup"><span data-stu-id="44e0a-110">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="44e0a-111">Wenn der **P- \_ Typmember** der [**RAS- \_ Parameter**](ras-parameters-str.md) Struktur paramnumber ist, enthält der **Number** -Member den Wert des medienspezifischen Parameters.</span><span class="sxs-lookup"><span data-stu-id="44e0a-111">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="44e0a-112">Beispielsweise ist der maxconnectbps-Parameter vom Typ paramnumber, und der Wert kann 19200 lauten.</span><span class="sxs-lookup"><span data-stu-id="44e0a-112">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

<span data-ttu-id="44e0a-113">Wenn der **P- \_ Typmember** der [**RAS- \_ Parameter**](ras-parameters-str.md) Struktur paramnumber ist, enthält der **Number** -Member den Wert des medienspezifischen Parameters.</span><span class="sxs-lookup"><span data-stu-id="44e0a-113">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamNumber, the **Number** member contains the value of the media-specific parameter.</span></span> <span data-ttu-id="44e0a-114">Beispielsweise ist der maxconnectbps-Parameter vom Typ paramnumber, und der Wert kann 19200 lauten.</span><span class="sxs-lookup"><span data-stu-id="44e0a-114">For example, the MAXCONNECTBPS parameter is of type ParamNumber, and the value might be 19200.</span></span>

</dd> <dt>

<span data-ttu-id="44e0a-115">**String**</span><span class="sxs-lookup"><span data-stu-id="44e0a-115">**String**</span></span>
</dt> <dd>

<span data-ttu-id="44e0a-116">Wenn der **P- \_ Typmember** der [**RAS- \_ Parameter**](ras-parameters-str.md) Struktur paramString ist, enthält der **Zeichen** folgen Member den Wert des medienspezifischen Parameters.</span><span class="sxs-lookup"><span data-stu-id="44e0a-116">If the **P\_Type** member of the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure is ParamString, the **String** member contains the value of the media-specific parameter.</span></span>

<dl> <dt>

<span data-ttu-id="44e0a-117">**Länge**</span><span class="sxs-lookup"><span data-stu-id="44e0a-117">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="44e0a-118">Gibt die Länge der Zeichenfolge, auf die vom **Datenmember** verwiesen wird, in Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="44e0a-118">Specifies the length, in characters, of the string pointed to by the **Data** member.</span></span>

</dd> <dt>

<span data-ttu-id="44e0a-119">**Daten**</span><span class="sxs-lookup"><span data-stu-id="44e0a-119">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="44e0a-120">Ein Zeiger auf einen Puffer, der den Zeichen folgen Wert eines medienspezifischen Parameters enthält.</span><span class="sxs-lookup"><span data-stu-id="44e0a-120">Pointer to a buffer that contains the string value of a media-specific parameter.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44e0a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44e0a-121">Requirements</span></span>



| <span data-ttu-id="44e0a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44e0a-122">Requirement</span></span> | <span data-ttu-id="44e0a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="44e0a-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44e0a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44e0a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="44e0a-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44e0a-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="44e0a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44e0a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="44e0a-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44e0a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="44e0a-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="44e0a-128">End of client support</span></span><br/>    | <span data-ttu-id="44e0a-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="44e0a-129">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="44e0a-130">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="44e0a-130">End of server support</span></span><br/>    | <span data-ttu-id="44e0a-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="44e0a-131">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="44e0a-132">Header</span><span class="sxs-lookup"><span data-stu-id="44e0a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="44e0a-133"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="44e0a-133"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44e0a-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44e0a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e0a-135">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="44e0a-135">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="44e0a-136">RAS-Server Verwaltung (Union)</span><span class="sxs-lookup"><span data-stu-id="44e0a-136">RAS Server Administration Union</span></span>](ras-server-administration-union.md)
</dt> <dt>

[<span data-ttu-id="44e0a-137">**RAS- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="44e0a-137">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="44e0a-138">**Format des RAS- \_ Parametern \_**</span><span class="sxs-lookup"><span data-stu-id="44e0a-138">**RAS\_PARAMS\_FORMAT**</span></span>](ras-params-format-str.md)
</dt> </dl>

 

 





