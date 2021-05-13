---
description: Listet den Inhalt der Liste der zuletzt verwendeten (MRU) auf. Ruft optional ein Element aus der -Enumeration ab.
title: EnumMRUListW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 1e6e4bd0820d35fec2a108a81eb1030567493e6a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843161"
---
# <a name="enummrulistw-function"></a><span data-ttu-id="b4c50-104">EnumMRUListW-Funktion</span><span class="sxs-lookup"><span data-stu-id="b4c50-104">EnumMRUListW function</span></span>

<span data-ttu-id="b4c50-105">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b4c50-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="b4c50-106">Sie kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="b4c50-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="b4c50-107">\]</span><span class="sxs-lookup"><span data-stu-id="b4c50-107">\]</span></span>

<span data-ttu-id="b4c50-108">Listet den Inhalt der Liste der zuletzt verwendeten (MRU) auf.</span><span class="sxs-lookup"><span data-stu-id="b4c50-108">Enumerates the contents of the most recently used (MRU) list.</span></span> <span data-ttu-id="b4c50-109">Ruft optional ein Element aus der -Enumeration ab.</span><span class="sxs-lookup"><span data-stu-id="b4c50-109">Optionally retrieves an item from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c50-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4c50-110">Syntax</span></span>


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a><span data-ttu-id="b4c50-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4c50-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4c50-112">*hMRU* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b4c50-112">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c50-113">Typ: **HANDLE**</span><span class="sxs-lookup"><span data-stu-id="b4c50-113">Type: **HANDLE**</span></span>

<span data-ttu-id="b4c50-114">Das Handle der MRU-Liste, das beim Erstellen der Liste abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b4c50-114">The handle of the MRU list, obtained when the list was created.</span></span>

</dd> <dt>

<span data-ttu-id="b4c50-115">*nItem* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b4c50-115">*nItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c50-116">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="b4c50-116">Type: **int**</span></span>

<span data-ttu-id="b4c50-117">Das zurückzugebende Element.</span><span class="sxs-lookup"><span data-stu-id="b4c50-117">The item to return.</span></span> <span data-ttu-id="b4c50-118">Wenn dieser Wert kleiner als 0 ist, gibt die Funktion die Anzahl der Elemente in der MRU-Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="b4c50-118">If this value is less than 0, the function returns the number of items in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="b4c50-119">*lpData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b4c50-119">*lpData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c50-120">Typ: **\* void**</span><span class="sxs-lookup"><span data-stu-id="b4c50-120">Type: **void\***</span></span>

<span data-ttu-id="b4c50-121">Ein Zeiger auf einen Puffer, der das in *nItem* angeforderte Element empfängt.</span><span class="sxs-lookup"><span data-stu-id="b4c50-121">A pointer to a buffer that receives the item requested in *nItem*.</span></span> <span data-ttu-id="b4c50-122">Wenn *nItem* kleiner als 0 ist, bleibt der Inhalt dieses Puffers unverändert.</span><span class="sxs-lookup"><span data-stu-id="b4c50-122">If *nItem* is less than 0, the contents of this buffer are unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="b4c50-123">*uLen* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b4c50-123">*uLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4c50-124">Typ: **UINT**</span><span class="sxs-lookup"><span data-stu-id="b4c50-124">Type: **UINT**</span></span>

<span data-ttu-id="b4c50-125">Die Größe des Puffers, einschließlich des beendenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="b4c50-125">The size of the buffer, including the terminating null character.</span></span> <span data-ttu-id="b4c50-126">Wenn die MRU-Liste mit dem **MRU \_ BINARY-Flag** erstellt wurde, ist dies die Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="b4c50-126">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="b4c50-127">Andernfalls ist dies die Größe in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b4c50-127">Otherwise, it is the size in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4c50-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4c50-128">Return value</span></span>

<span data-ttu-id="b4c50-129">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="b4c50-129">Type: **int**</span></span>

<span data-ttu-id="b4c50-130">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="b4c50-130">Returns one of the following values.</span></span>

-   <span data-ttu-id="b4c50-131">Gibt die Anzahl der Elemente in der Enumeration zurück, wenn *nItem* kleiner als 0 ist.</span><span class="sxs-lookup"><span data-stu-id="b4c50-131">Returns the number of items in the enumeration, if *nItem* is less than 0.</span></span>
-   <span data-ttu-id="b4c50-132">Gibt -1 zurück, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b4c50-132">Returns -1 if an error occurred.</span></span>
-   <span data-ttu-id="b4c50-133">Andernfalls gibt die Größe der in *lpData* zurückgegebenen Zeichenfolge zurück, einschließlich des beendenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="b4c50-133">Otherwise, returns the size of the string returned in *lpData*, including the terminating null character.</span></span> <span data-ttu-id="b4c50-134">Wenn die MRU-Liste mit dem **MRU \_ BINARY-Flag** erstellt wurde, ist dies die Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="b4c50-134">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="b4c50-135">Andernfalls ist dies die Größe in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b4c50-135">Otherwise, it is the size in characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4c50-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4c50-136">Remarks</span></span>

<span data-ttu-id="b4c50-137">Diese Funktion ist nicht in einem öffentlichen Header oder einer öffentlichen Bibliothek enthalten.</span><span class="sxs-lookup"><span data-stu-id="b4c50-137">This function is not included in a public header or library.</span></span> <span data-ttu-id="b4c50-138">Auf sie kann über [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) zugegriffen oder aus comctl32.dll durch ihre Ordnungszahl extrahiert werden, d. h. 403 für **EnumMRUListW.**</span><span class="sxs-lookup"><span data-stu-id="b4c50-138">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 403 for **EnumMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4c50-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4c50-139">Requirements</span></span>



| <span data-ttu-id="b4c50-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4c50-140">Requirement</span></span> | <span data-ttu-id="b4c50-141">Wert</span><span class="sxs-lookup"><span data-stu-id="b4c50-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4c50-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4c50-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b4c50-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4c50-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b4c50-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4c50-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b4c50-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4c50-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b4c50-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b4c50-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4c50-147"><dt>Comctl32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b4c50-147"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="b4c50-148">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="b4c50-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b4c50-149">**EnumMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="b4c50-149">**EnumMRUListW** (Unicode)</span></span><br/>                                                                          |



## <a name="see-also"></a><span data-ttu-id="b4c50-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4c50-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c50-151">**CreateMRUListW**</span><span class="sxs-lookup"><span data-stu-id="b4c50-151">**CreateMRUListW**</span></span>](createmrulist.md)
</dt> <dt>

[<span data-ttu-id="b4c50-152">**MRUINFO**</span><span class="sxs-lookup"><span data-stu-id="b4c50-152">**MRUINFO**</span></span>](mruinfo.md)
</dt> </dl>

 

 
