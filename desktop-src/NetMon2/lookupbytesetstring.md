---
description: Die lookupbytesetstring-Funktion gibt die Zeichenfolge zurück, die dem angegebenen Wert einer gekennzeichneten Menge entspricht.
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: Lookupbytesetstring-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7a2b5bffbfcb30ed8ec00da42fbc9ad6008fd5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372854"
---
# <a name="lookupbytesetstring-function"></a><span data-ttu-id="42021-103">Lookupbytesetstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="42021-103">LookupByteSetString function</span></span>

<span data-ttu-id="42021-104">Die **lookupbytesetstring** -Funktion gibt die Zeichenfolge zurück, die dem angegebenen Wert einer gekennzeichneten Menge entspricht.</span><span class="sxs-lookup"><span data-stu-id="42021-104">The **LookupByteSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="42021-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="42021-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a><span data-ttu-id="42021-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="42021-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42021-107">*lpset*</span><span class="sxs-lookup"><span data-stu-id="42021-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="42021-108">Ein Zeiger auf eine bezeichnete Menge, aus der die Bezeichnung des Werts extrahiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="42021-108">Pointer to a labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="42021-109">*Wert*</span><span class="sxs-lookup"><span data-stu-id="42021-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="42021-110">Der Wert einer gekennzeichneten Menge.</span><span class="sxs-lookup"><span data-stu-id="42021-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42021-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42021-111">Return value</span></span>

<span data-ttu-id="42021-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert eine Zeichenfolge, die dem bereitgestellten Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="42021-112">If the function is successful, the return value is a string corresponding to the value provided.</span></span>

<span data-ttu-id="42021-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="42021-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="42021-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42021-114">Requirements</span></span>



| <span data-ttu-id="42021-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42021-115">Requirement</span></span> | <span data-ttu-id="42021-116">Wert</span><span class="sxs-lookup"><span data-stu-id="42021-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42021-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42021-117">Minimum supported client</span></span><br/> | <span data-ttu-id="42021-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42021-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="42021-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42021-119">Minimum supported server</span></span><br/> | <span data-ttu-id="42021-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42021-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42021-121">Header</span><span class="sxs-lookup"><span data-stu-id="42021-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="42021-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="42021-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="42021-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="42021-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="42021-124"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42021-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="42021-125">DLL</span><span class="sxs-lookup"><span data-stu-id="42021-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42021-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42021-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




