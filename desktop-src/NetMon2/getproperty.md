---
description: Die GetProperty-Funktion gibt ein Handle für eine angegebene Eigenschaft zurück.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: GetProperty-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958711"
---
# <a name="getproperty-function"></a><span data-ttu-id="44d57-103">GetProperty-Funktion</span><span class="sxs-lookup"><span data-stu-id="44d57-103">GetProperty function</span></span>

<span data-ttu-id="44d57-104">Die **GetProperty** -Funktion gibt ein Handle für eine angegebene Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="44d57-104">The **GetProperty** function returns a handle to a given property.</span></span>

## <a name="syntax"></a><span data-ttu-id="44d57-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="44d57-105">Syntax</span></span>


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a><span data-ttu-id="44d57-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="44d57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d57-107">*hprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44d57-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d57-108">Handle für das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="44d57-108">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="44d57-109">*PropertyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44d57-109">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44d57-110">Der Name der Eigenschaft (z. b. **Checksum**).</span><span class="sxs-lookup"><span data-stu-id="44d57-110">Name of the property (for example, **Checksum**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44d57-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44d57-111">Return value</span></span>

<span data-ttu-id="44d57-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert das Handle für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="44d57-112">If the function is successful, the return value is the handle to the property.</span></span>

<span data-ttu-id="44d57-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="44d57-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="44d57-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44d57-114">Remarks</span></span>

<span data-ttu-id="44d57-115">Die **GetProperty** -Funktion kann verwendet werden, um das Eigenschafts Handle abzurufen, das erforderlich ist, um Instanzen der Eigenschaft zu suchen.</span><span class="sxs-lookup"><span data-stu-id="44d57-115">The **GetProperty** function can be used to obtain the property handle needed to locate instances of the property.</span></span> <span data-ttu-id="44d57-116">Die Funktionen, die zum Auffinden von Eigenschafts Instanzen verwendet werden, sind [findpropertyinstance](findpropertyinstance.md) (das die erste Instanz sucht) und [findpropertyinstancerestart](findpropertyinstancerestart.md) (die die nächste Instanz findet).</span><span class="sxs-lookup"><span data-stu-id="44d57-116">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) (which locates the first instance) and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (which locates the next instance).</span></span>

<span data-ttu-id="44d57-117">[*Experten*](e.md) und [*Parser*](p.md) können die **GetProperty** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="44d57-117">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProperty** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="44d57-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44d57-118">Requirements</span></span>



| <span data-ttu-id="44d57-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44d57-119">Requirement</span></span> | <span data-ttu-id="44d57-120">Wert</span><span class="sxs-lookup"><span data-stu-id="44d57-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44d57-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44d57-121">Minimum supported client</span></span><br/> | <span data-ttu-id="44d57-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44d57-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="44d57-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44d57-123">Minimum supported server</span></span><br/> | <span data-ttu-id="44d57-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44d57-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="44d57-125">Header</span><span class="sxs-lookup"><span data-stu-id="44d57-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="44d57-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="44d57-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="44d57-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="44d57-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="44d57-128"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44d57-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="44d57-129">DLL</span><span class="sxs-lookup"><span data-stu-id="44d57-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44d57-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44d57-130"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44d57-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44d57-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d57-132">Findpropertyinstance</span><span class="sxs-lookup"><span data-stu-id="44d57-132">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="44d57-133">Findpropertyinstancerestart</span><span class="sxs-lookup"><span data-stu-id="44d57-133">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




