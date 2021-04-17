---
description: Die lookupwordsetstring-Funktion gibt die Zeichenfolge zurück, die dem angeforderten Wert aus einer gekennzeichneten Menge entspricht.
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: Lookupwordsetstring-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7487becb195571e1eb88044195293b2c0b226e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526762"
---
# <a name="lookupwordsetstring-function"></a><span data-ttu-id="791a6-103">Lookupwordsetstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="791a6-103">LookupWordSetString function</span></span>

<span data-ttu-id="791a6-104">Die **lookupwordsetstring** -Funktion gibt die Zeichenfolge zurück, die dem angeforderten Wert aus einer gekennzeichneten Menge entspricht.</span><span class="sxs-lookup"><span data-stu-id="791a6-104">The **LookupWordSetString** function returns the string corresponding to the requested value from a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="791a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="791a6-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a><span data-ttu-id="791a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="791a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="791a6-107">*lpset*</span><span class="sxs-lookup"><span data-stu-id="791a6-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="791a6-108">Der Satz, aus dem Sie die Bezeichnung des Werts extrahieren.</span><span class="sxs-lookup"><span data-stu-id="791a6-108">Labeled set from which you extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="791a6-109">*Wert*</span><span class="sxs-lookup"><span data-stu-id="791a6-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="791a6-110">Der Wert einer gekennzeichneten Menge.</span><span class="sxs-lookup"><span data-stu-id="791a6-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="791a6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="791a6-111">Return value</span></span>

<span data-ttu-id="791a6-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert eine Zeichenfolge, die dem angeforderten Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="791a6-112">If the function is successful, the return value is a string that corresponds to the requested value.</span></span>

<span data-ttu-id="791a6-113">Wenn die Funktion nicht erfolgreich ist, ist der angegebene Wert nicht im Satz, der Rückgabewert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="791a6-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="791a6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="791a6-114">Requirements</span></span>



| <span data-ttu-id="791a6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="791a6-115">Requirement</span></span> | <span data-ttu-id="791a6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="791a6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="791a6-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="791a6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="791a6-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="791a6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="791a6-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="791a6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="791a6-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="791a6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="791a6-121">Header</span><span class="sxs-lookup"><span data-stu-id="791a6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="791a6-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="791a6-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="791a6-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="791a6-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="791a6-124"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="791a6-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="791a6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="791a6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="791a6-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="791a6-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




