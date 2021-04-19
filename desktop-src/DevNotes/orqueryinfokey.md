---
description: Ruft Informationen über den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur ab.
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: Orqueryinfokey-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b38a0dd35b1fe1755fbcbc3bcac3da379ee57e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367703"
---
# <a name="orqueryinfokey-function"></a><span data-ttu-id="a0fd5-103">Orqueryinfokey-Funktion</span><span class="sxs-lookup"><span data-stu-id="a0fd5-103">ORQueryInfoKey function</span></span>

<span data-ttu-id="a0fd5-104">Ruft Informationen über den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-104">Retrieves information about the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0fd5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0fd5-105">Syntax</span></span>


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="a0fd5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0fd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0fd5-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0fd5-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd5-108">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd5-109">*lpclass* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0fd5-109">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd5-110">Ein Zeiger auf einen Puffer, der die Schlüssel Klasse empfängt.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-110">A pointer to a buffer that receives the key class.</span></span> <span data-ttu-id="a0fd5-111">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd5-112">*lpcclass* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0fd5-112">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd5-113">Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, auf den der *lpclass* -Parameter zeigt (in Zeichen).</span><span class="sxs-lookup"><span data-stu-id="a0fd5-113">A pointer to a variable that specifies the size of the buffer pointed to by the *lpClass* parameter, in characters.</span></span>

<span data-ttu-id="a0fd5-114">Die Größe sollte das abschließende Null-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-114">The size should include the terminating null character.</span></span> <span data-ttu-id="a0fd5-115">Wenn die Funktion zurückgibt, enthält diese Variable die Größe der Klassen Zeichenfolge, die im Puffer gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-115">When the function returns, this variable contains the size of the class string that is stored in the buffer.</span></span> <span data-ttu-id="a0fd5-116">Die zurückgegebene Anzahl umfasst nicht das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-116">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="a0fd5-117">Wenn der Puffer nicht groß genug ist, gibt die Funktion Fehler \_ Weitere \_ Daten zurück, und die Variable enthält die Größe der Zeichenfolge (in Zeichen), ohne das abschließende Null-Zeichen zu zählen.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-117">If the buffer is not big enough, the function returns ERROR\_MORE\_DATA, and the variable contains the size of the string, in characters, without counting the terminating null character.</span></span>

<span data-ttu-id="a0fd5-118">Wenn *lpclass* **null** ist, kann *lpcclass* **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-118">If *lpClass* is **NULL**, *lpcClass* can be **NULL**.</span></span>

<span data-ttu-id="a0fd5-119">Wenn der *lpclass* -Parameter eine gültige Adresse ist, der *lpcclass* -Parameter jedoch nicht ist (z. b. wenn der *lpcclass* -Parameter **null** ist), gibt die Funktion einen \_ ungültigen \_ Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-119">If the *lpClass* parameter is a valid address, but the *lpcClass* parameter is not (for example, if the *lpcClass* parameter is **NULL**) then the function returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd5-120">*lpcsubkeys* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0fd5-120">*lpcSubKeys* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd5-121">Ein Zeiger auf eine Variable, die die Anzahl der Unterschlüssel empfängt, die im angegebenen Schlüssel enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-121">A pointer to a variable that receives the number of subkeys that are contained by the specified key.</span></span> <span data-ttu-id="a0fd5-122">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd5-123">*lpcmaxsubkeylen* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0fd5-123">*lpcMaxSubKeyLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd5-124">Ein Zeiger auf eine Variable, die die Größe des unter Schlüssels des Schlüssels mit dem längsten Namen, in Unicode-Zeichen, ohne das abschließende Null-Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-124">A pointer to a variable that receives the size of the key's subkey with the longest name, in Unicode characters, not including the terminating null character.</span></span> <span data-ttu-id="a0fd5-125">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-125">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd5-126">*lpcmaxclasslen* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0fd5-126">*lpcMaxClassLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd5-127">Ein Zeiger auf eine Variable, die die Größe der längsten Zeichenfolge, die eine Unterschlüssel Klasse angibt, in Unicode-Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-127">A pointer to a variable that receives the size of the longest string that specifies a subkey class, in Unicode characters.</span></span> <span data-ttu-id="a0fd5-128">Die zurückgegebene Anzahl umfasst nicht das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-128">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="a0fd5-129">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-129">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd5-130">*lpcvalues* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0fd5-130">*lpcValues* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd5-131">Ein Zeiger auf eine Variable, die die Anzahl der Werte empfängt, die dem Schlüssel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-131">A pointer to a variable that receives the number of values that are associated with the key.</span></span> <span data-ttu-id="a0fd5-132">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-132">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd5-133">*lpcmaxvaluenamelen* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0fd5-133">*lpcMaxValueNameLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd5-134">Ein Zeiger auf eine Variable, die die Größe des längsten Wertnamens des Schlüssels in Unicode-Zeichen empfängt.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-134">A pointer to a variable that receives the size of the key's longest value name, in Unicode characters.</span></span> <span data-ttu-id="a0fd5-135">Die Größe umfasst nicht das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-135">The size does not include the terminating null character.</span></span> <span data-ttu-id="a0fd5-136">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd5-137">*lpcmaxvaluelen* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0fd5-137">*lpcMaxValueLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd5-138">Ein Zeiger auf eine Variable, die die Größe der längsten Daten Komponente unter den Werten des Schlüssels in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-138">A pointer to a variable that receives the size of the longest data component among the key's values, in bytes.</span></span> <span data-ttu-id="a0fd5-139">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-139">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd5-140">*lpcbsecuritydescriptor* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0fd5-140">*lpcbSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd5-141">Ein Zeiger auf eine Variable, die die Größe der Sicherheits Beschreibung des Schlüssels in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-141">A pointer to a variable that receives the size of the key's security descriptor, in bytes.</span></span> <span data-ttu-id="a0fd5-142">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-142">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0fd5-143">*lpftlastschreitezeit* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0fd5-143">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0fd5-144">Ein Zeiger auf eine [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur, die den Zeitpunkt des letzten Schreibzugriffs empfängt.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-144">A pointer to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the last write time.</span></span> <span data-ttu-id="a0fd5-145">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-145">This parameter can be **NULL**.</span></span>

<span data-ttu-id="a0fd5-146">Die-Funktion legt die Member der [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur fest, um den Zeitpunkt der letzten Änderung des Schlüssels oder seiner Wert Einträge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-146">The function sets the members of the [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to indicate the last time that the key or any of its value entries is modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0fd5-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0fd5-147">Return value</span></span>

<span data-ttu-id="a0fd5-148">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-148">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a0fd5-149">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-149">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="a0fd5-150">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-150">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="a0fd5-151">Wenn der *lpclass* -Puffer zu klein ist, um den Namen der Klasse zu erhalten, gibt die Funktion Fehler \_ Weitere \_ Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="a0fd5-151">If the *lpClass* buffer is too small to receive the name of the class, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0fd5-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0fd5-152">Requirements</span></span>



| <span data-ttu-id="a0fd5-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0fd5-153">Requirement</span></span> | <span data-ttu-id="a0fd5-154">Wert</span><span class="sxs-lookup"><span data-stu-id="a0fd5-154">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fd5-155">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="a0fd5-155">Redistributable</span></span><br/> | <span data-ttu-id="a0fd5-156">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="a0fd5-156">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="a0fd5-157">Header</span><span class="sxs-lookup"><span data-stu-id="a0fd5-157">Header</span></span><br/>          | <dl> <span data-ttu-id="a0fd5-158"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0fd5-158"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0fd5-159">DLL</span><span class="sxs-lookup"><span data-stu-id="a0fd5-159">DLL</span></span><br/>             | <dl> <span data-ttu-id="a0fd5-160"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0fd5-160"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0fd5-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0fd5-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0fd5-162">FILETIME</span><span class="sxs-lookup"><span data-stu-id="a0fd5-162">FILETIME</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="a0fd5-163">**Orkreatekey**</span><span class="sxs-lookup"><span data-stu-id="a0fd5-163">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="a0fd5-164">**Oropenkey**</span><span class="sxs-lookup"><span data-stu-id="a0fd5-164">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="a0fd5-165">**Ordeletekey**</span><span class="sxs-lookup"><span data-stu-id="a0fd5-165">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> </dl>

 

 
