---
description: Die lookupdwordsetstring-Funktion gibt die Zeichenfolge zurück, die dem angegebenen Wert einer gekennzeichneten Menge entspricht.
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: Lookupdwordsetstring-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57688edab7421f939e03322b8b244219b00d31fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752185"
---
# <a name="lookupdwordsetstring-function"></a><span data-ttu-id="8f732-103">Lookupdwordsetstring-Funktion</span><span class="sxs-lookup"><span data-stu-id="8f732-103">LookupDwordSetString function</span></span>

<span data-ttu-id="8f732-104">Die **lookupdwordsetstring** -Funktion gibt die Zeichenfolge zurück, die dem angegebenen Wert einer gekennzeichneten Menge entspricht.</span><span class="sxs-lookup"><span data-stu-id="8f732-104">The **LookupDwordSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f732-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f732-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="8f732-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f732-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f732-107">*lpset*</span><span class="sxs-lookup"><span data-stu-id="8f732-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="8f732-108">Bezeichnete Menge, aus der Sie die Bezeichnung des Werts extrahieren können.</span><span class="sxs-lookup"><span data-stu-id="8f732-108">Labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="8f732-109">*Wert*</span><span class="sxs-lookup"><span data-stu-id="8f732-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="8f732-110">Der Wert einer gekennzeichneten Menge.</span><span class="sxs-lookup"><span data-stu-id="8f732-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f732-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f732-111">Return value</span></span>

<span data-ttu-id="8f732-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Zeichenfolge, die dem angegebenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="8f732-112">If the function is successful, the return value is the string that corresponds to the specified value.</span></span>

<span data-ttu-id="8f732-113">Wenn die Funktion nicht erfolgreich ist, ist der angegebene Wert nicht im Satz, der Rückgabewert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="8f732-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f732-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f732-114">Requirements</span></span>



| <span data-ttu-id="8f732-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f732-115">Requirement</span></span> | <span data-ttu-id="8f732-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8f732-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f732-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f732-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f732-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f732-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8f732-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f732-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f732-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f732-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f732-121">Header</span><span class="sxs-lookup"><span data-stu-id="8f732-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f732-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f732-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f732-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8f732-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f732-124"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f732-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="8f732-125">DLL</span><span class="sxs-lookup"><span data-stu-id="8f732-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f732-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f732-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




