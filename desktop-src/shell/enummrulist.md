---
description: Listet den Inhalt der Liste der zuletzt verwendeten (MRU) auf. Ruft optional ein Element aus der-Enumeration ab.
title: Enummrulistw-Funktion
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
ms.openlocfilehash: 6b6e9588588e44a2c3b40f6ac012b11f21c875e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867748"
---
# <a name="enummrulistw-function"></a><span data-ttu-id="3bd79-104">Enummrulistw-Funktion</span><span class="sxs-lookup"><span data-stu-id="3bd79-104">EnumMRUListW function</span></span>

<span data-ttu-id="3bd79-105">\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3bd79-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="3bd79-106">Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3bd79-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="3bd79-107">\]</span><span class="sxs-lookup"><span data-stu-id="3bd79-107">\]</span></span>

<span data-ttu-id="3bd79-108">Listet den Inhalt der Liste der zuletzt verwendeten (MRU) auf.</span><span class="sxs-lookup"><span data-stu-id="3bd79-108">Enumerates the contents of the most recently used (MRU) list.</span></span> <span data-ttu-id="3bd79-109">Ruft optional ein Element aus der-Enumeration ab.</span><span class="sxs-lookup"><span data-stu-id="3bd79-109">Optionally retrieves an item from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd79-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bd79-110">Syntax</span></span>


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a><span data-ttu-id="3bd79-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bd79-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bd79-112">*hmru* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bd79-112">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd79-113">Typ: **handle**</span><span class="sxs-lookup"><span data-stu-id="3bd79-113">Type: **HANDLE**</span></span>

<span data-ttu-id="3bd79-114">Das Handle der MRU-Liste, das beim Erstellen der Liste abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="3bd79-114">The handle of the MRU list, obtained when the list was created.</span></span>

</dd> <dt>

<span data-ttu-id="3bd79-115">*nitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bd79-115">*nItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd79-116">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="3bd79-116">Type: **int**</span></span>

<span data-ttu-id="3bd79-117">Das zurück zugebende Element.</span><span class="sxs-lookup"><span data-stu-id="3bd79-117">The item to return.</span></span> <span data-ttu-id="3bd79-118">Wenn dieser Wert kleiner als 0 ist, gibt die Funktion die Anzahl der Elemente in der MRU-Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="3bd79-118">If this value is less than 0, the function returns the number of items in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="3bd79-119">*lpdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3bd79-119">*lpData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd79-120">Geben Sie Folgendes ein: \**void \** _</span><span class="sxs-lookup"><span data-stu-id="3bd79-120">Type: \**void\** _</span></span>

<span data-ttu-id="3bd79-121">Ein Zeiger auf einen Puffer, der das in _nItem \* angeforderte Element empfängt.</span><span class="sxs-lookup"><span data-stu-id="3bd79-121">A pointer to a buffer that receives the item requested in _nItem\*.</span></span> <span data-ttu-id="3bd79-122">Wenn *nitem* kleiner als 0 ist, ist der Inhalt dieses Puffers unverändert.</span><span class="sxs-lookup"><span data-stu-id="3bd79-122">If *nItem* is less than 0, the contents of this buffer are unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="3bd79-123">*uLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bd79-123">*uLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd79-124">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="3bd79-124">Type: **UINT**</span></span>

<span data-ttu-id="3bd79-125">Die Größe des Puffers, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="3bd79-125">The size of the buffer, including the terminating null character.</span></span> <span data-ttu-id="3bd79-126">Wenn die MRU-Liste mit dem **MRU- \_ Binärflag** erstellt wurde, ist dies die Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3bd79-126">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="3bd79-127">Andernfalls ist es die Größe in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3bd79-127">Otherwise, it is the size in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bd79-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bd79-128">Return value</span></span>

<span data-ttu-id="3bd79-129">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="3bd79-129">Type: **int**</span></span>

<span data-ttu-id="3bd79-130">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3bd79-130">Returns one of the following values.</span></span>

-   <span data-ttu-id="3bd79-131">Gibt die Anzahl der Elemente in der Enumeration zurück, wenn *nitem* kleiner als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="3bd79-131">Returns the number of items in the enumeration, if *nItem* is less than 0.</span></span>
-   <span data-ttu-id="3bd79-132">Gibt-1 zurück, wenn ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3bd79-132">Returns -1 if an error occurred.</span></span>
-   <span data-ttu-id="3bd79-133">Andernfalls wird die Größe der in *lpdata* zurückgegebenen Zeichenfolge zurückgegeben, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="3bd79-133">Otherwise, returns the size of the string returned in *lpData*, including the terminating null character.</span></span> <span data-ttu-id="3bd79-134">Wenn die MRU-Liste mit dem **MRU- \_ Binärflag** erstellt wurde, ist dies die Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3bd79-134">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="3bd79-135">Andernfalls ist es die Größe in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="3bd79-135">Otherwise, it is the size in characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bd79-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3bd79-136">Remarks</span></span>

<span data-ttu-id="3bd79-137">Diese Funktion ist nicht in einem öffentlichen Header oder einer Bibliothek enthalten.</span><span class="sxs-lookup"><span data-stu-id="3bd79-137">This function is not included in a public header or library.</span></span> <span data-ttu-id="3bd79-138">Der Zugriff darauf erfolgt über [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) oder das Extrahieren aus comctl32.dll durch die Ordnungszahl, die 403 für **enummrulistw** ist.</span><span class="sxs-lookup"><span data-stu-id="3bd79-138">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 403 for **EnumMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bd79-139">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3bd79-139">Requirements</span></span>



| <span data-ttu-id="3bd79-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bd79-140">Requirement</span></span> | <span data-ttu-id="3bd79-141">Wert</span><span class="sxs-lookup"><span data-stu-id="3bd79-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd79-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3bd79-142">Minimum supported client</span></span><br/> | <span data-ttu-id="3bd79-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bd79-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3bd79-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3bd79-144">Minimum supported server</span></span><br/> | <span data-ttu-id="3bd79-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bd79-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3bd79-146">DLL</span><span class="sxs-lookup"><span data-stu-id="3bd79-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bd79-147"><dt>Comctl32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="3bd79-147"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="3bd79-148">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="3bd79-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3bd79-149">**Enummrulistw** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="3bd79-149">**EnumMRUListW** (Unicode)</span></span><br/>                                                                          |



## <a name="see-also"></a><span data-ttu-id="3bd79-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3bd79-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd79-151">**"Kreatemrulistw"**</span><span class="sxs-lookup"><span data-stu-id="3bd79-151">**CreateMRUListW**</span></span>](createmrulist.md)
</dt> <dt>

[<span data-ttu-id="3bd79-152">**Mruinfo**</span><span class="sxs-lookup"><span data-stu-id="3bd79-152">**MRUINFO**</span></span>](mruinfo.md)
</dt> </dl>

 

 
