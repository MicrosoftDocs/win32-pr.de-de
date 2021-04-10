---
title: RAS_PARAMS_FORMAT-Enumeration (rassapi. h)
description: Der \_ \_ Enumerationstyp "RAS-Parametertyp" wird in der Struktur der RAS- \_ Parameter verwendet, um den Datentyp anzugeben, der einem medienspezifischen Schlüssel zugeordnet ist.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS_PARAMS_FORMAT-Enumeration RAS
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104391"
---
# <a name="ras_params_format-enumeration"></a><span data-ttu-id="28646-104">RAS- \_ parametriams- \_ formatenumeration</span><span class="sxs-lookup"><span data-stu-id="28646-104">RAS\_PARAMS\_FORMAT enumeration</span></span>

<span data-ttu-id="28646-105">\[Die **RAS- \_ parametriams- \_ formatenumeration** wird ab Windows Vista nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="28646-105">\[The **RAS\_PARAMS\_FORMAT** enumeration is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="28646-106">Der Enumerationstyp " **RAS \_ \_** -Parametertyp" wird in der Struktur der [**RAS- \_ Parameter**](ras-parameters-str.md) verwendet, um den Datentyp anzugeben, der einem medienspezifischen Schlüssel zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="28646-106">The **RAS\_PARAMS\_FORMAT** enumeration type is used in the [**RAS\_PARAMETERS**](ras-parameters-str.md) structure to indicate the type of data associated with a media-specific key.</span></span>

## <a name="syntax"></a><span data-ttu-id="28646-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="28646-107">Syntax</span></span>


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="28646-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="28646-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="28646-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**Paramnumber**</span><span class="sxs-lookup"><span data-stu-id="28646-109"><span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**</span></span>
</dt> <dd>

<span data-ttu-id="28646-110">Gibt an, dass die dem Schlüssel zugeordneten Daten eine Zahl sind.</span><span class="sxs-lookup"><span data-stu-id="28646-110">Indicates that the data associated with the key is a number.</span></span>

</dd> <dt>

<span data-ttu-id="28646-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**</span><span class="sxs-lookup"><span data-stu-id="28646-111"><span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**</span></span>
</dt> <dd>

<span data-ttu-id="28646-112">Gibt an, dass die dem Schlüssel zugeordneten Daten eine Zeichenfolge sind.</span><span class="sxs-lookup"><span data-stu-id="28646-112">Indicates that the data associated with the key is a string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28646-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28646-113">Requirements</span></span>



| <span data-ttu-id="28646-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28646-114">Requirement</span></span> | <span data-ttu-id="28646-115">Wert</span><span class="sxs-lookup"><span data-stu-id="28646-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="28646-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28646-116">Minimum supported client</span></span><br/> | <span data-ttu-id="28646-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28646-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="28646-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28646-118">Minimum supported server</span></span><br/> | <span data-ttu-id="28646-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28646-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="28646-120">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="28646-120">End of client support</span></span><br/>    | <span data-ttu-id="28646-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="28646-121">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="28646-122">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="28646-122">End of server support</span></span><br/>    | <span data-ttu-id="28646-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="28646-123">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="28646-124">Header</span><span class="sxs-lookup"><span data-stu-id="28646-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="28646-125"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="28646-125"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28646-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28646-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28646-127">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="28646-127">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="28646-128">RAS-Server-Administrations Enumerationen</span><span class="sxs-lookup"><span data-stu-id="28646-128">RAS Server Administration Enumerations</span></span>](ras-server-administration-enumerations.md)
</dt> <dt>

[<span data-ttu-id="28646-129">**RAS- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="28646-129">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> </dl>

 

 





