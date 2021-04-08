---
description: Der Experte muss die Register-expertenfunktion implementieren. Netzwerkmonitor Ruft die Register-expertenfunktion auf, um Informationen über den Experten zu erhalten.
ms.assetid: 58cfe525-99b1-40ce-b8d8-fa1c62a20c40
title: Expertenrückruf Funktion registrieren (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 085d5c59b17b10949ad39d07354906f40e123988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864063"
---
# <a name="register-expert-callback-function"></a><span data-ttu-id="100bf-104">Expertenrückruf Funktion registrieren</span><span class="sxs-lookup"><span data-stu-id="100bf-104">Register Expert callback function</span></span>

<span data-ttu-id="100bf-105">Der Experte muss die **Register** -expertenfunktion implementieren.</span><span class="sxs-lookup"><span data-stu-id="100bf-105">The expert must implement the **Register** expert function.</span></span> <span data-ttu-id="100bf-106">Netzwerkmonitor Ruft die **Register** -expertenfunktion auf, um Informationen über den Experten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="100bf-106">Network Monitor calls the **Register** expert function to obtain information about the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="100bf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="100bf-107">Syntax</span></span>


```C++
BOOL WINAPI Register(
  _Inout_ PEXPERTENUMINFO pExpertInfo
);
```



## <a name="parameters"></a><span data-ttu-id="100bf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="100bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="100bf-109">*pexpertinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="100bf-109">*pExpertInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="100bf-110">Zeiger auf eine [**expertenuminfo**](expertenuminfo.md) -Struktur, die von Netzwerkmonitor zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="100bf-110">Pointer to an [**EXPERTENUMINFO**](expertenuminfo.md) structure that Network Monitor allocates.</span></span> <span data-ttu-id="100bf-111">Der Experte füllt die Struktur mit allen angeforderten Informationen aus.</span><span class="sxs-lookup"><span data-stu-id="100bf-111">The expert fills in the structure with all requested information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="100bf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="100bf-112">Return value</span></span>

<span data-ttu-id="100bf-113">Wenn die Funktion erfolgreich ist, ist der Rückgabewert **true**, und die Funktion gibt die angeforderten Informationen zurück.</span><span class="sxs-lookup"><span data-stu-id="100bf-113">If the function is successful, the return value is **TRUE**, and the function returns the requested information.</span></span>

<span data-ttu-id="100bf-114">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="100bf-114">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="100bf-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="100bf-115">Remarks</span></span>

<span data-ttu-id="100bf-116">Das  Versionsmember der [**expertenenuminfo**](expertenuminfo.md) -Struktur muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="100bf-116">The **Version** member of the [**EXPERTENUMINFO**](expertenuminfo.md) structure must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="100bf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="100bf-117">Requirements</span></span>



| <span data-ttu-id="100bf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="100bf-118">Requirement</span></span> | <span data-ttu-id="100bf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="100bf-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="100bf-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="100bf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="100bf-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="100bf-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="100bf-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="100bf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="100bf-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="100bf-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="100bf-124">Header</span><span class="sxs-lookup"><span data-stu-id="100bf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="100bf-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="100bf-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




