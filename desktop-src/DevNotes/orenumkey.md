---
description: Listet die Unterschlüssel des angegebenen geöffneten Registrierungsschlüssels in einer Offline Registrierungs Struktur auf. Die-Funktion Ruft bei jedem Aufruf Informationen zu einem Unterschlüssel ab.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: Orenkey-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 24278bc59c75f32aed92c2ea5b5428f6ef6d9b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366809"
---
# <a name="orenumkey-function"></a><span data-ttu-id="59eb7-104">Orenkey-Funktion</span><span class="sxs-lookup"><span data-stu-id="59eb7-104">OREnumKey function</span></span>

<span data-ttu-id="59eb7-105">Listet die Unterschlüssel des angegebenen geöffneten Registrierungsschlüssels in einer Offline Registrierungs Struktur auf.</span><span class="sxs-lookup"><span data-stu-id="59eb7-105">Enumerates the subkeys of the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="59eb7-106">Die-Funktion Ruft bei jedem Aufruf Informationen zu einem Unterschlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="59eb7-106">The function retrieves information about one subkey each time it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="59eb7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="59eb7-107">Syntax</span></span>


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="59eb7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="59eb7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59eb7-109">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59eb7-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59eb7-110">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="59eb7-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="59eb7-111">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59eb7-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59eb7-112">Der Index des abzurufenden unter Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="59eb7-112">The index of the subkey to retrieve.</span></span> <span data-ttu-id="59eb7-113">Dieser Parameter sollte für den ersten Aufruf der-Funktion 0 (null) sein und dann für nachfolgende Aufrufe inkrementiert werden.</span><span class="sxs-lookup"><span data-stu-id="59eb7-113">This parameter should be zero for the first call to the function and then incremented for subsequent calls.</span></span>

<span data-ttu-id="59eb7-114">Da Unterschlüssel nicht geordnet sind, verfügen alle neuen Unterschlüssel über einen beliebigen Index.</span><span class="sxs-lookup"><span data-stu-id="59eb7-114">Because subkeys are not ordered, any new subkey will have an arbitrary index.</span></span> <span data-ttu-id="59eb7-115">Dies bedeutet, dass die Funktion Unterschlüssel in beliebiger Reihenfolge zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="59eb7-115">This means that the function may return subkeys in any order.</span></span>

</dd> <dt>

<span data-ttu-id="59eb7-116">*lpname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="59eb7-116">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59eb7-117">Ein Zeiger auf einen Puffer, der den Namen des unter Schlüssels einschließlich des abschließenden NULL-Zeichens empfängt.</span><span class="sxs-lookup"><span data-stu-id="59eb7-117">A pointer to a buffer that receives the name of the subkey, including the terminating null character.</span></span> <span data-ttu-id="59eb7-118">Die-Funktion kopiert nur den Namen des unter Schlüssels, nicht die vollständige Schlüssel Hierarchie, in den Puffer.</span><span class="sxs-lookup"><span data-stu-id="59eb7-118">The function copies only the name of the subkey, not the full key hierarchy, to the buffer.</span></span> <span data-ttu-id="59eb7-119">Wenn die Funktion fehlschlägt, werden keine Informationen in diesen Puffer kopiert.</span><span class="sxs-lookup"><span data-stu-id="59eb7-119">If the function fails, no information is copied to this buffer.</span></span>

<span data-ttu-id="59eb7-120">Weitere Informationen finden Sie unter [Größenbeschränkungen für das Registrierungs Element](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="59eb7-120">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="59eb7-121">*lpcname* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="59eb7-121">*lpcName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59eb7-122">Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, der durch den *lpname* -Parameter in **WCHARs** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="59eb7-122">A pointer to a variable that specifies the size of the buffer specified by the *lpName* parameter, in **WCHARs**.</span></span> <span data-ttu-id="59eb7-123">Diese Größe sollte das abschließende Null-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="59eb7-123">This size should include the terminating null character.</span></span> <span data-ttu-id="59eb7-124">Wenn die Funktion erfolgreich ausgeführt wird, enthält die Variable, auf die von *lpcname* verwiesen wird, die Anzahl von Zeichen, die im Puffer gespeichert sind, ohne das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="59eb7-124">If the function succeeds, the variable pointed to by *lpcName* contains the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="59eb7-125">*lpclass* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="59eb7-125">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="59eb7-126">Ein Zeiger auf einen Puffer, der die NULL-terminierte Klassen Zeichenfolge des enumerierten unter Schlüssels empfängt.</span><span class="sxs-lookup"><span data-stu-id="59eb7-126">A pointer to a buffer that receives the null-terminated class string of the enumerated subkey.</span></span> <span data-ttu-id="59eb7-127">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="59eb7-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="59eb7-128">*lpcclass* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="59eb7-128">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="59eb7-129">Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, der durch den *lpclass* -Parameter in **WCHARs** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="59eb7-129">A pointer to a variable that specifies the size of the buffer specified by the *lpClass* parameter, in **WCHARs**.</span></span> <span data-ttu-id="59eb7-130">Die Größe sollte das abschließende Null-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="59eb7-130">The size should include the terminating null character.</span></span> <span data-ttu-id="59eb7-131">Wenn die Funktion erfolgreich ausgeführt wird, enthält *lpcclass* die Anzahl von Zeichen, die im Puffer gespeichert sind, ohne das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="59eb7-131">If the function succeeds, *lpcClass* contains the number of characters stored in the buffer, not including the terminating null character.</span></span> <span data-ttu-id="59eb7-132">Dieser Parameter kann nur **null** sein, wenn *lpclass* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="59eb7-132">This parameter can be **NULL** only if *lpClass* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="59eb7-133">*lpftlastschreitezeit* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="59eb7-133">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="59eb7-134">Ein Zeiger auf die [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur, die die Uhrzeit empfängt, zu der der enumerierte Unterschlüssel zuletzt geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="59eb7-134">A pointer to [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the time at which the enumerated subkey was last written.</span></span> <span data-ttu-id="59eb7-135">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="59eb7-135">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59eb7-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59eb7-136">Return value</span></span>

<span data-ttu-id="59eb7-137">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="59eb7-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="59eb7-138">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="59eb7-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="59eb7-139">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="59eb7-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="59eb7-140">Folgende Fehlercodes sind möglich:</span><span class="sxs-lookup"><span data-stu-id="59eb7-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="59eb7-141">Wenn der *lpname* -Puffer zu klein ist, um den Namen des Schlüssels zu erhalten, gibt die Funktion Fehler \_ Weitere \_ Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="59eb7-141">If the *lpName* buffer is too small to receive the name of the key, the function returns ERROR\_MORE\_DATA.</span></span>
-   <span data-ttu-id="59eb7-142">Wenn keine weiteren Unterschlüssel verfügbar sind, gibt die Funktion einen Fehler \_ ohne \_ Weitere \_ Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="59eb7-142">If there are no more subkeys available, the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="remarks"></a><span data-ttu-id="59eb7-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59eb7-143">Remarks</span></span>

<span data-ttu-id="59eb7-144">Um Unterschlüssel aufzulisten, sollte eine Anwendung zunächst die Funktion " **orenkey** " aufrufen, wobei der *dwIndex* -Parameter auf 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="59eb7-144">To enumerate subkeys, an application should initially call the **OREnumKey** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="59eb7-145">Die Anwendung sollte dann den *dwIndex* -Parameter Inkrement erhöhen und " **gatumschlag Key** " aufrufen, bis keine Unterschlüssel mehr vorhanden sind (d. h., die Funktion gibt \_ einen Fehler ohne \_ Weitere \_ Elemente zurück)</span><span class="sxs-lookup"><span data-stu-id="59eb7-145">The application should then increment the *dwIndex* parameter and call **OREnumKey** until there are no more subkeys (meaning the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="59eb7-146">Die Anwendung kann *dwIndex* auch auf den Index des letzten unter Schlüssels beim ersten Aufrufe der Funktion festlegen und den Index verringern, bis der Unterschlüssel mit dem Index 0 aufgezählt wird.</span><span class="sxs-lookup"><span data-stu-id="59eb7-146">The application can also set *dwIndex* to the index of the last subkey on the first call to the function and decrement the index until the subkey with the index 0 is enumerated.</span></span> <span data-ttu-id="59eb7-147">Verwenden Sie die [**orqueryinfokey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) -Funktion, um den Index des letzten unter Schlüssels abzurufen.</span><span class="sxs-lookup"><span data-stu-id="59eb7-147">To retrieve the index of the last subkey, use the [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) function.</span></span>

<span data-ttu-id="59eb7-148">Obwohl eine Anwendung die Funktion " **atenumkey** " verwendet, sollte Sie keine Offline Registrierungsfunktionen aufrufen, die möglicherweise den aufzuzählenden Schlüssel ändern.</span><span class="sxs-lookup"><span data-stu-id="59eb7-148">While an application is using the **OREnumKey** function, it should not make calls to any offline registry functions that might change the key being enumerated.</span></span>

## <a name="requirements"></a><span data-ttu-id="59eb7-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59eb7-149">Requirements</span></span>



| <span data-ttu-id="59eb7-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59eb7-150">Requirement</span></span> | <span data-ttu-id="59eb7-151">Wert</span><span class="sxs-lookup"><span data-stu-id="59eb7-151">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59eb7-152">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="59eb7-152">Redistributable</span></span><br/> | <span data-ttu-id="59eb7-153">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="59eb7-153">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="59eb7-154">Header</span><span class="sxs-lookup"><span data-stu-id="59eb7-154">Header</span></span><br/>          | <dl> <span data-ttu-id="59eb7-155"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="59eb7-155"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="59eb7-156">DLL</span><span class="sxs-lookup"><span data-stu-id="59eb7-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="59eb7-157"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59eb7-157"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59eb7-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59eb7-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59eb7-159">**Orkreatekey**</span><span class="sxs-lookup"><span data-stu-id="59eb7-159">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="59eb7-160">**Ordeletekey**</span><span class="sxs-lookup"><span data-stu-id="59eb7-160">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="59eb7-161">**Oropenkey**</span><span class="sxs-lookup"><span data-stu-id="59eb7-161">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="59eb7-162">**Orqueryinfokey**</span><span class="sxs-lookup"><span data-stu-id="59eb7-162">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
