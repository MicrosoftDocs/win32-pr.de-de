---
description: Listet die Werte für den angegebenen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur auf. Die-Funktion Ruft bei jedem Aufruf der-Funktion Informationen für einen Wert unter dem angegebenen Schlüssel ab.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: Orenvalue-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b8049a5d16a88dc87bf4c0f6f5e8ef18b30beadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372069"
---
# <a name="orenumvalue-function"></a><span data-ttu-id="41585-104">Orenvalue-Funktion</span><span class="sxs-lookup"><span data-stu-id="41585-104">OREnumValue function</span></span>

<span data-ttu-id="41585-105">Listet die Werte für den angegebenen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur auf.</span><span class="sxs-lookup"><span data-stu-id="41585-105">Enumerates the values for the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="41585-106">Die-Funktion Ruft bei jedem Aufruf der-Funktion Informationen für einen Wert unter dem angegebenen Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="41585-106">The function retrieves information for one value under the specified key each time the function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="41585-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="41585-107">Syntax</span></span>


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
);
```



## <a name="parameters"></a><span data-ttu-id="41585-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="41585-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41585-109">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41585-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41585-110">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="41585-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="41585-111">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41585-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41585-112">Der Index des abzurufenden Werts.</span><span class="sxs-lookup"><span data-stu-id="41585-112">The index of the value to be retrieved.</span></span> <span data-ttu-id="41585-113">Dieser Parameter sollte für den ersten Aufruf der Funktion 0 (null) sein und dann für nachfolgende Aufrufe inkrementiert werden.</span><span class="sxs-lookup"><span data-stu-id="41585-113">This parameter should be zero for the first call to the function and then be incremented for subsequent calls.</span></span>

<span data-ttu-id="41585-114">Da die Werte nicht geordnet sind, haben alle neuen Werte einen beliebigen Index.</span><span class="sxs-lookup"><span data-stu-id="41585-114">Because values are not ordered, any new value will have an arbitrary index.</span></span> <span data-ttu-id="41585-115">Dies bedeutet, dass die Funktion Werte in beliebiger Reihenfolge zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="41585-115">This means that the function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="41585-116">*lpvaluename* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="41585-116">*lpValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41585-117">Ein Zeiger auf einen Puffer, der den Namen des Werts als NULL-terminierte Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="41585-117">A pointer to a buffer that receives the name of the value as a null-terminated string.</span></span> <span data-ttu-id="41585-118">Dieser Puffer muss groß genug sein, um das abschließende Null-Zeichen einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="41585-118">This buffer must be large enough to include the terminating null character.</span></span>

<span data-ttu-id="41585-119">Weitere Informationen finden Sie unter [Größenbeschränkungen für das Registrierungs Element](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="41585-119">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="41585-120">*lpcvaluename* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="41585-120">*lpcValueName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41585-121">Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, auf den der *lpvaluename* -Parameter zeigt (in Zeichen).</span><span class="sxs-lookup"><span data-stu-id="41585-121">A pointer to a variable that specifies the size of the buffer pointed to by the *lpValueName* parameter, in characters.</span></span> <span data-ttu-id="41585-122">Wenn die Funktion zurückgibt, empfängt die-Variable die Anzahl der im Puffer gespeicherten Zeichen, ohne das abschließende Null Zeichen.</span><span class="sxs-lookup"><span data-stu-id="41585-122">When the function returns, the variable receives the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="41585-123">*lptype* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="41585-123">*lpType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="41585-124">Ein Zeiger auf eine Variable, die einen Code empfängt, der den Typ der im angegebenen Wert gespeicherten Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="41585-124">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="41585-125">Eine Liste der möglichen Typcodes finden Sie unter [Registrierungs Werttypen](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="41585-125">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="41585-126">Der *lptype* -Parameter kann **null** sein, wenn der Typcode nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="41585-126">The *lpType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="41585-127">*lpdata* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="41585-127">*lpData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="41585-128">Ein Zeiger auf einen Puffer, der die Daten für den Wert Eintrag empfängt.</span><span class="sxs-lookup"><span data-stu-id="41585-128">A pointer to a buffer that receives the data for the value entry.</span></span> <span data-ttu-id="41585-129">Dieser Parameter kann **null** sein, wenn die Daten nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="41585-129">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="41585-130">Wenn *lpdata* den Wert **null** hat und *lpcbdata* ungleich **null** ist, speichert die Funktion die Größe der Daten in Bytes in der Variablen, auf die von *lpcbdata* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="41585-130">If *lpData* is **NULL** and *lpcbData* is non-**NULL**, the function stores the size of the data, in bytes, in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="41585-131">Dadurch kann eine Anwendung die beste Methode zum Zuordnen eines Puffers für die Daten bestimmen.</span><span class="sxs-lookup"><span data-stu-id="41585-131">This enables an application to determine the best way to allocate a buffer for the data.</span></span>

</dd> <dt>

<span data-ttu-id="41585-132">*lpcbdata* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="41585-132">*lpcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="41585-133">Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, auf den der *lpdata* -Parameter zeigt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="41585-133">A pointer to a variable that specifies the size of the buffer pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="41585-134">Wenn die Funktion zurückgegeben wird, empfängt die-Variable die Anzahl von Bytes, die im Puffer gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="41585-134">When the function returns, the variable receives the number of bytes stored in the buffer.</span></span>

<span data-ttu-id="41585-135">Dieser Parameter kann nur **null** sein, wenn *lpdata* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="41585-135">This parameter can be **NULL** only if *lpData* is **NULL**.</span></span>

<span data-ttu-id="41585-136">Wenn die Daten über das reg \_ SZ-Format, den reg \_ \_ MultiSZ-oder den reg-Typ "SZ" aufweisen \_ \_ , enthält diese Größe alle abschließenden NULL-Zeichen oder Zeichen.</span><span class="sxs-lookup"><span data-stu-id="41585-136">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="41585-137">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="41585-137">For more information, see Remarks.</span></span>

<span data-ttu-id="41585-138">Wenn der von *lpdata* angegebene Puffer nicht groß genug ist, um die Daten zu speichern, gibt die Funktion Fehler \_ Weitere \_ Daten zurück und speichert die erforderliche Puffergröße in der Variablen, auf die von *lpcbdata* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="41585-138">If the buffer specified by *lpData* is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="41585-139">In diesem Fall ist der Inhalt von *lpdata* nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="41585-139">In this case, the contents of *lpData* are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41585-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41585-140">Return value</span></span>

<span data-ttu-id="41585-141">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="41585-141">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="41585-142">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="41585-142">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="41585-143">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="41585-143">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="41585-144">Wenn der *lpdata* -Puffer zu klein ist, um den Wert zu erhalten, gibt die Funktion Fehler \_ Weitere \_ Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="41585-144">If the *lpData* buffer is too small to receive the value, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="41585-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41585-145">Remarks</span></span>

<span data-ttu-id="41585-146">Um Werte aufzuzählen, sollte eine Anwendung zunächst die Funktion " **orenvalue** " aufrufen, wobei der *dwIndex* -Parameter auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="41585-146">To enumerate values, an application should initially call the **OREnumValue** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="41585-147">Die Anwendung sollte dann *dwIndex* Inkrement erhöhen und die Funktion " **orenvalue** " so lange aufzurufen, bis keine weiteren Werte vorhanden sind (bis die Funktion "Error \_ No More Items" zurückgibt \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="41585-147">The application should then increment *dwIndex* and call the **OREnumValue** function until there are no more values (until the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="41585-148">Die Anwendung kann *dwIndex* auch auf den Index des letzten Werts beim ersten Aufrufe der Funktion festlegen und den Index verringern, bis der Wert mit Index 0 aufgezählt wird.</span><span class="sxs-lookup"><span data-stu-id="41585-148">The application can also set *dwIndex* to the index of the last value on the first call to the function and decrement the index until the value with index 0 is enumerated.</span></span> <span data-ttu-id="41585-149">Um den Index des letzten Werts abzurufen, verwenden Sie die [**orqueryinfokey**](orqueryinfokey.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="41585-149">To retrieve the index of the last value, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

<span data-ttu-id="41585-150">Bei der Verwendung von " **orenvalue**" sollte eine Anwendung keine Offline Registrierungsfunktionen aufzurufen, die möglicherweise den abgefragten Schlüssel ändern.</span><span class="sxs-lookup"><span data-stu-id="41585-150">While using **OREnumValue**, an application should not call any offline registry functions that might change the key being queried.</span></span>

<span data-ttu-id="41585-151">Wenn die Daten den "reg \_ SZ"-, "reg \_ MultiSZ"-oder "reg expand"- \_ \_ \_ Dokumenttyp aufweisen, wurde die Zeichenfolge möglicherweise nicht mit den ordnungsgemäßen NULL-abschließenden Zeichen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="41585-151">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, the string may not have been stored with the proper null-terminating characters.</span></span> <span data-ttu-id="41585-152">Daher sollte die Anwendung auch dann, wenn die Funktion Fehler erfolgreich zurückgibt \_ , sicherstellen, dass die Zeichenfolge ordnungsgemäß beendet wird, bevor Sie verwendet wird. andernfalls kann Sie einen Puffer überschreiben.</span><span class="sxs-lookup"><span data-stu-id="41585-152">Therefore, even if the function returns ERROR\_SUCCESS, the application should ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer.</span></span> <span data-ttu-id="41585-153">(Beachten Sie, dass reg \_ \_MultiSZ-Zeichen folgen sollten zwei NULL-abschließende Zeichen aufweisen.)</span><span class="sxs-lookup"><span data-stu-id="41585-153">(Note that REG\_MULTI\_SZ strings should have two null-terminating characters.)</span></span>

<span data-ttu-id="41585-154">Verwenden Sie die [**orqueryinfokey**](orqueryinfokey.md) -Funktion, um die maximale Größe des Namens und der Datenpuffer zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="41585-154">To determine the maximum size of the name and data buffers, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="41585-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41585-155">Requirements</span></span>



| <span data-ttu-id="41585-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41585-156">Requirement</span></span> | <span data-ttu-id="41585-157">Wert</span><span class="sxs-lookup"><span data-stu-id="41585-157">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41585-158">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="41585-158">Redistributable</span></span><br/> | <span data-ttu-id="41585-159">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="41585-159">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="41585-160">Header</span><span class="sxs-lookup"><span data-stu-id="41585-160">Header</span></span><br/>          | <dl> <span data-ttu-id="41585-161"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="41585-161"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="41585-162">DLL</span><span class="sxs-lookup"><span data-stu-id="41585-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="41585-163"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41585-163"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41585-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41585-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41585-165">**Orkreatekey**</span><span class="sxs-lookup"><span data-stu-id="41585-165">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="41585-166">**Orenkey**</span><span class="sxs-lookup"><span data-stu-id="41585-166">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="41585-167">**Oropenkey**</span><span class="sxs-lookup"><span data-stu-id="41585-167">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="41585-168">**Orqueryinfokey**</span><span class="sxs-lookup"><span data-stu-id="41585-168">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
