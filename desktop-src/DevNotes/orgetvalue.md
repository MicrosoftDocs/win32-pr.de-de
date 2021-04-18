---
description: Ruft den Typ und die Daten für den angegebenen Registrierungs Wert in einer Offline Registrierungs Struktur ab.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: Orgetvalue-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 375dae37e2e6b6299a7bf1fd36f9b950d0433d89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368545"
---
# <a name="orgetvalue-function"></a><span data-ttu-id="8d06b-103">Orgetvalue-Funktion</span><span class="sxs-lookup"><span data-stu-id="8d06b-103">ORGetValue function</span></span>

<span data-ttu-id="8d06b-104">Ruft den Typ und die Daten für den angegebenen Registrierungs Wert in einer Offline Registrierungs Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="8d06b-104">Retrieves the type and data for the specified registry value in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d06b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d06b-105">Syntax</span></span>


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="8d06b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d06b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d06b-107">*Handle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d06b-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d06b-108">Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="8d06b-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="8d06b-109">*lpsubkey* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8d06b-109">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d06b-110">Der Name des Registrierungsschlüssels.</span><span class="sxs-lookup"><span data-stu-id="8d06b-110">The name of the registry key.</span></span> <span data-ttu-id="8d06b-111">Dieser Schlüssel muss ein Unterschlüssel des Schlüssels sein, der durch den *handle* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8d06b-111">This key must be a subkey of the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="8d06b-112">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="8d06b-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="8d06b-113">Bei Schlüsselnamen wird Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="8d06b-113">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="8d06b-114">*lpValue* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8d06b-114">*lpValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d06b-115">Der Name des Registrierungs Werts.</span><span class="sxs-lookup"><span data-stu-id="8d06b-115">The name of the registry value.</span></span> <span data-ttu-id="8d06b-116">Wenn dieser Parameter **null** oder eine leere Zeichenfolge ("") ist, ruft die Funktion den Typ und die Daten für den unbenannten oder Standardwert des Schlüssels ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8d06b-116">If this parameter is **NULL** or an empty string, "", the function retrieves the type and data for the key's unnamed or default value, if any.</span></span> <span data-ttu-id="8d06b-117">Weitere Informationen finden Sie unter [Größenbeschränkungen für das Registrierungs Element](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="8d06b-117">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="8d06b-118">Schlüssel haben nicht automatisch einen unbenannten oder Standardwert.</span><span class="sxs-lookup"><span data-stu-id="8d06b-118">Keys do not automatically have an unnamed or default value.</span></span> <span data-ttu-id="8d06b-119">Unbenannte Werte können von einem beliebigen Typ sein.</span><span class="sxs-lookup"><span data-stu-id="8d06b-119">Unnamed values can be of any type.</span></span>

<span data-ttu-id="8d06b-120">Bei Werten Namen wird die Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="8d06b-120">Value names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="8d06b-121">*pdwtype* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="8d06b-121">*pdwType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d06b-122">Ein Zeiger auf eine Variable, die einen Code empfängt, der den Typ der im angegebenen Wert gespeicherten Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="8d06b-122">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="8d06b-123">Eine Liste der möglichen Typcodes finden Sie unter [Registrierungs Werttypen](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="8d06b-123">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="8d06b-124">Dieser Parameter kann **null** sein, wenn der Typ nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8d06b-124">This parameter can be **NULL** if the type is not required.</span></span>

</dd> <dt>

<span data-ttu-id="8d06b-125">*pvData* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="8d06b-125">*pvData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d06b-126">Ein Zeiger auf einen Puffer, der die Daten des Werts empfängt.</span><span class="sxs-lookup"><span data-stu-id="8d06b-126">A pointer to a buffer that receives the value's data.</span></span> <span data-ttu-id="8d06b-127">Dieser Parameter kann **null** sein, wenn die Daten nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8d06b-127">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="8d06b-128">Wenn es sich bei den Daten um eine Zeichenfolge handelt, prüft die Funktion auf ein abschließendes NULL-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8d06b-128">If the data is a string, the function checks for a terminating null character.</span></span> <span data-ttu-id="8d06b-129">Wenn eine solche nicht gefunden wird, wird die Zeichenfolge mit einem NULL-Terminator gespeichert, wenn der Puffer groß genug ist, um das zusätzliche Zeichen aufnehmen zu können.</span><span class="sxs-lookup"><span data-stu-id="8d06b-129">If one is not found, the string is stored with a null terminator if the buffer is large enough to accommodate the extra character.</span></span> <span data-ttu-id="8d06b-130">Andernfalls schlägt die Funktion fehl und gibt Fehlermeldungen zurück \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8d06b-130">Otherwise, the function fails and returns ERROR\_MORE\_DATA.</span></span>

</dd> <dt>

<span data-ttu-id="8d06b-131">*pcbData* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="8d06b-131">*pcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8d06b-132">Ein Zeiger auf eine Variable, die die Größe des Puffers angibt, auf den der *pvData* -Parameter zeigt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="8d06b-132">A pointer to a variable that specifies the size of the buffer pointed to by the *pvData* parameter, in bytes.</span></span> <span data-ttu-id="8d06b-133">Wenn die Funktion zurückgegeben wird, enthält diese Variable die Größe der Daten, die in *pvData* kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="8d06b-133">When the function returns, this variable contains the size of the data copied to *pvData*.</span></span>

<span data-ttu-id="8d06b-134">Der *pcbData* -Parameter kann nur **null** sein, wenn *pvData* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="8d06b-134">The *pcbData* parameter can be **NULL** only if *pvData* is **NULL**.</span></span>

<span data-ttu-id="8d06b-135">Wenn die Daten über das reg \_ SZ-Format, den reg \_ \_ MultiSZ-oder den reg-Typ "SZ" aufweisen \_ \_ , enthält diese Größe alle abschließenden NULL-Zeichen oder Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8d06b-135">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="8d06b-136">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="8d06b-136">For more information, see Remarks.</span></span>

<span data-ttu-id="8d06b-137">Wenn der durch den *pvData* -Parameter angegebene Puffer nicht groß genug ist, um die Daten zu speichern, gibt die Funktion Fehler \_ Weitere \_ Daten zurück und speichert die erforderliche Puffergröße in der Variablen, auf die von *pcbData* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8d06b-137">If the buffer specified by *pvData* parameter is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="8d06b-138">In diesem Fall ist der Inhalt des *pvData* -Puffers nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="8d06b-138">In this case, the contents of the *pvData* buffer are undefined.</span></span>

<span data-ttu-id="8d06b-139">Wenn *pvData* den Wert **null** hat und *pcbData* ungleich **null** ist, gibt die Funktion den Fehler Erfolg zurück \_ und speichert die Größe der Daten in Bytes in der Variablen, auf die von *pcbData* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8d06b-139">If *pvData* is **NULL**, and *pcbData* is non-**NULL**, the function returns ERROR\_SUCCESS and stores the size of the data, in bytes, in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="8d06b-140">Dies ermöglicht es einer Anwendung, die beste Methode zum Zuordnen eines Puffers für die Daten des Werts zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8d06b-140">This enables an application to determine the best way to allocate a buffer for the value's data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d06b-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d06b-141">Return value</span></span>

<span data-ttu-id="8d06b-142">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8d06b-142">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="8d06b-143">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8d06b-143">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="8d06b-144">Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8d06b-144">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d06b-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d06b-145">Remarks</span></span>

<span data-ttu-id="8d06b-146">Eine Anwendung ruft in der Regel die Funktion " [**orenvalue**](orenumvalue.md) " auf, um die Wertnamen zu bestimmen, und ruft dann die **orgetvalue** -Funktion auf, um die Daten für die Namen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8d06b-146">An application typically calls the [**OREnumValue**](orenumvalue.md) function to determine the value names and then calls the **ORGetValue** function to retrieve the data for the names.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d06b-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d06b-147">Requirements</span></span>



| <span data-ttu-id="8d06b-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d06b-148">Requirement</span></span> | <span data-ttu-id="8d06b-149">Wert</span><span class="sxs-lookup"><span data-stu-id="8d06b-149">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d06b-150">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8d06b-150">Redistributable</span></span><br/> | <span data-ttu-id="8d06b-151">Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="8d06b-151">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="8d06b-152">Header</span><span class="sxs-lookup"><span data-stu-id="8d06b-152">Header</span></span><br/>          | <dl> <span data-ttu-id="8d06b-153"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d06b-153"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d06b-154">DLL</span><span class="sxs-lookup"><span data-stu-id="8d06b-154">DLL</span></span><br/>             | <dl> <span data-ttu-id="8d06b-155"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d06b-155"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d06b-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d06b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d06b-157">**Orkreatekey**</span><span class="sxs-lookup"><span data-stu-id="8d06b-157">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="8d06b-158">**Orenkey**</span><span class="sxs-lookup"><span data-stu-id="8d06b-158">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="8d06b-159">**Orenvalue**</span><span class="sxs-lookup"><span data-stu-id="8d06b-159">**OREnumValue**</span></span>](orenumvalue.md)
</dt> <dt>

[<span data-ttu-id="8d06b-160">**Oropenkey**</span><span class="sxs-lookup"><span data-stu-id="8d06b-160">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="8d06b-161">**Orqueryinfokey**</span><span class="sxs-lookup"><span data-stu-id="8d06b-161">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
