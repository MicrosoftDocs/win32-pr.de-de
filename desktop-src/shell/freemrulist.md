---
description: Gibt das der zuletzt verwendeten (MRU)-Liste zugeordnete Handle frei und schreibt zwischengespeicherte Daten in die Registrierung.
title: Freemrulist-Funktion
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
ms.openlocfilehash: 8140586d5f428a66f27a71ea665ae6761380e3a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979649"
---
# <a name="freemrulist-function"></a><span data-ttu-id="8b37b-103">Freemrulist-Funktion</span><span class="sxs-lookup"><span data-stu-id="8b37b-103">FreeMRUList function</span></span>

<span data-ttu-id="8b37b-104">Gibt das der zuletzt verwendeten (MRU)-Liste zugeordnete Handle frei und schreibt zwischengespeicherte Daten in die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="8b37b-104">Frees the handle associated with the most recently used (MRU) list and writes cached data to the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b37b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b37b-105">Syntax</span></span>


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a><span data-ttu-id="8b37b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b37b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b37b-107">*hmru* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b37b-107">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b37b-108">Typ: **handle**</span><span class="sxs-lookup"><span data-stu-id="8b37b-108">Type: **HANDLE**</span></span>

<span data-ttu-id="8b37b-109">Das Handle der MRU-Liste, die freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b37b-109">The handle of the MRU list to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b37b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b37b-110">Return value</span></span>

<span data-ttu-id="8b37b-111">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="8b37b-111">Type: **int**</span></span>

<span data-ttu-id="8b37b-112">Gibt bei erfolgreicher Ausführung einen nicht negativen Wert zurück, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="8b37b-112">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b37b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b37b-113">Remarks</span></span>

<span data-ttu-id="8b37b-114">Wenn die MRU-Liste mit dem **MRU \_ cachewrite** -Flag erstellt wurde, bewirkt das Aufrufen von **freemrulist** , dass alle Änderungen, die noch nicht in die in der Registrierung gespeicherte Version der MRU-Liste geschrieben wurden, zu diesem Zeitpunkt geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8b37b-114">If the MRU list was created using the **MRU\_CACHEWRITE** flag, calling **FreeMRUList** causes any changes not yet written to the version of the MRU list stored in registry to be written at this time.</span></span>

<span data-ttu-id="8b37b-115">Diese Funktion ist nicht in einem öffentlichen Header oder einer Bibliothek enthalten.</span><span class="sxs-lookup"><span data-stu-id="8b37b-115">This function is not included in a public header or library.</span></span> <span data-ttu-id="8b37b-116">Sie muss aus comctl32.dll durch die Ordnungszahl 152 extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="8b37b-116">It must be extracted from comctl32.dll by ordinal 152.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b37b-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="8b37b-117">Requirements</span></span>



| <span data-ttu-id="8b37b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b37b-118">Requirement</span></span> | <span data-ttu-id="8b37b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8b37b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b37b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b37b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8b37b-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b37b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8b37b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b37b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8b37b-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b37b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8b37b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8b37b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b37b-125"><dt>Comctl32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="8b37b-125"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




