---
description: Gibt das handle frei, das der LISTE der zuletzt verwendeten (MRU) zugeordnet ist, und schreibt zwischengespeicherte Daten in die Registrierung.
title: FreeMRUList-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 7d31d261629853c3b82b9d1564c5e8755e047570
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840621"
---
# <a name="freemrulist-function"></a><span data-ttu-id="fe8b7-103">FreeMRUList-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe8b7-103">FreeMRUList function</span></span>

<span data-ttu-id="fe8b7-104">Gibt das handle frei, das der LISTE der zuletzt verwendeten (MRU) zugeordnet ist, und schreibt zwischengespeicherte Daten in die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="fe8b7-104">Frees the handle associated with the most recently used (MRU) list and writes cached data to the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe8b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe8b7-105">Syntax</span></span>


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a><span data-ttu-id="fe8b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe8b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe8b7-107">*hMRU* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe8b7-107">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe8b7-108">Typ: **HANDLE**</span><span class="sxs-lookup"><span data-stu-id="fe8b7-108">Type: **HANDLE**</span></span>

<span data-ttu-id="fe8b7-109">Das Handle der frei zu gebenden MRU-Liste.</span><span class="sxs-lookup"><span data-stu-id="fe8b7-109">The handle of the MRU list to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe8b7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe8b7-110">Return value</span></span>

<span data-ttu-id="fe8b7-111">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="fe8b7-111">Type: **int**</span></span>

<span data-ttu-id="fe8b7-112">Gibt bei Erfolg einen nicht negativen Wert zurück, andernfalls -1.</span><span class="sxs-lookup"><span data-stu-id="fe8b7-112">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe8b7-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fe8b7-113">Remarks</span></span>

<span data-ttu-id="fe8b7-114">Wenn die MRU-Liste mit dem **MRU \_ CACHEWRITE-Flag** erstellt wurde, bewirkt der Aufruf von **FreeMRUList,** dass alle Änderungen, die noch nicht in die Version der in der Registrierung gespeicherten MRU-Liste geschrieben wurden, zu diesem Zeitpunkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fe8b7-114">If the MRU list was created using the **MRU\_CACHEWRITE** flag, calling **FreeMRUList** causes any changes not yet written to the version of the MRU list stored in registry to be written at this time.</span></span>

<span data-ttu-id="fe8b7-115">Diese Funktion ist nicht in einem öffentlichen Header oder einer öffentlichen Bibliothek enthalten.</span><span class="sxs-lookup"><span data-stu-id="fe8b7-115">This function is not included in a public header or library.</span></span> <span data-ttu-id="fe8b7-116">Es muss aus der Ordnungszahl comctl32.dll 152 extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="fe8b7-116">It must be extracted from comctl32.dll by ordinal 152.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe8b7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe8b7-117">Requirements</span></span>



| <span data-ttu-id="fe8b7-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe8b7-118">Requirement</span></span> | <span data-ttu-id="fe8b7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fe8b7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8b7-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe8b7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe8b7-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe8b7-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe8b7-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe8b7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe8b7-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe8b7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fe8b7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fe8b7-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe8b7-125"><dt>Comctl32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="fe8b7-125"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




