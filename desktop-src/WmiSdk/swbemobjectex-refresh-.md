---
description: Aktualisiert die Daten für Objekte mit Daten, die von einem Leistungs Anbieter bereitgestellt werden, z. b. die Leistungsdaten. Aktualisierbare Daten können schneller und ohne einen aufzurufenden Austausch von "Swap Services. Get" abgerufen werden \_ .
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: SWbemObjectEx.Refresh_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355608"
---
# <a name="swbemobjectexrefresh_-method"></a><span data-ttu-id="d3cf3-104">Errbemubjectex. Refresh- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="d3cf3-104">SWbemObjectEx.Refresh\_ method</span></span>

<span data-ttu-id="d3cf3-105">Mit **der \_ Refresh** -Methode von " [**errbemubjectex**](swbemobjectex.md) " werden die Daten für Objekte aktualisiert, die von einem Leistungs Anbieter bereitgestellte Daten enthalten, wie z. b. die [Leistungs Leistungs](/windows/desktop/CIMWin32Prov/performance-counter-classes)Daten.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-105">The **Refresh\_** method of [**SWbemObjectEx**](swbemobjectex.md) updates the data for objects that have data supplied by a performance provider, such as the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="d3cf3-106">Aktualisierbare Daten können schneller und ohne einen aufzurufenden [**Austausch von " \_ Swap Services. Get**](swbemservices-get.md)" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-106">You can obtain updated data more quickly and without a call to [**SWbemServices.Get\_**](swbemservices-get.md).</span></span>

<span data-ttu-id="d3cf3-107">Weitere Informationen zu dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d3cf3-107">For more information about this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d3cf3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3cf3-108">Syntax</span></span>


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d3cf3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3cf3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3cf3-110">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d3cf3-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3cf3-111">Reservierte Vorgangs Flags, die, falls angegeben, 0 (null) sein müssen.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-111">Reserved operation flags which, if specified, must be 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="d3cf3-112">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d3cf3-112">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3cf3-113">Ein [**-**](swbemnamedvalueset.md) Objekt, das den Kontext für den Vorgang festlegt.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3cf3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3cf3-114">Return value</span></span>

<span data-ttu-id="d3cf3-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d3cf3-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d3cf3-116">Error codes</span></span>

<span data-ttu-id="d3cf3-117">Nach Abschluss der **Aktualisierungs \_** Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-117">After completion of the **Refresh\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d3cf3-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d3cf3-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d3cf3-119">Der Anbieter ist intern fehlgeschlagen, auch wenn der Vorgang gültig war.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-119">The provider failed internally, even though the operation was valid.</span></span>

</dd> <dt>

<span data-ttu-id="d3cf3-120">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="d3cf3-120">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="d3cf3-121">Das angeforderte Format wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-121">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="d3cf3-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d3cf3-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d3cf3-123">Einer der Parameter für den Aufruf ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-123">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="d3cf3-124">**wbemErrRefresherBusy** -2147749975 (0x80041057)</span><span class="sxs-lookup"><span data-stu-id="d3cf3-124">**wbemErrRefresherBusy** - 2147749975 (0x80041057)</span></span>
</dt> <dd>

<span data-ttu-id="d3cf3-125">Die Aktualisierungsroutine ist mit einer anderen Operation ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-125">The refresher is busy with another operation.</span></span>

</dd> <dt>

<span data-ttu-id="d3cf3-126">**wbempartialresults** -2147745808 (0x80040010)</span><span class="sxs-lookup"><span data-stu-id="d3cf3-126">**wbemPartialResults** - 2147745808 (0x80040010)</span></span>
</dt> <dd>

<span data-ttu-id="d3cf3-127">Nicht alle Objekte, Enumeratoren oder gedugten Aktualisierungs Zeichen wurden erfolgreich aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-127">Not all of the objects, enumerators, or nested refreshers were successfully updated.</span></span> <span data-ttu-id="d3cf3-128">Diese Rückgabe ist kein Fehler, aber ein Hinweis darauf, dass der Vorgang unvollständig war.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-128">This return is not an error but an indication that the operation was incomplete.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d3cf3-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3cf3-129">Examples</span></span>

<span data-ttu-id="d3cf3-130">Im folgenden Skriptcode Beispiel wird veranschaulicht, wie sowohl Rohdaten als auch gekochte Leistungsindikatoren für den System Prozess abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-130">The following script code example shows how to obtain both raw and cooked performance counters for the system process.</span></span> <span data-ttu-id="d3cf3-131">Die Objekte werden alle zwei Sekunden aktualisiert, und die angezeigten Eigenschaften werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d3cf3-131">The objects are refreshed every two seconds and the properties displayed.</span></span>


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a><span data-ttu-id="d3cf3-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3cf3-132">Requirements</span></span>



| <span data-ttu-id="d3cf3-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3cf3-133">Requirement</span></span> | <span data-ttu-id="d3cf3-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d3cf3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3cf3-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3cf3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d3cf3-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3cf3-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d3cf3-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3cf3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d3cf3-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3cf3-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d3cf3-139">Header</span><span class="sxs-lookup"><span data-stu-id="d3cf3-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3cf3-140"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3cf3-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3cf3-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d3cf3-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="d3cf3-142"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d3cf3-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d3cf3-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d3cf3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3cf3-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3cf3-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d3cf3-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="d3cf3-145">CLSID</span></span><br/>                    | <span data-ttu-id="d3cf3-146">CLSID- \_ Swap-Austausch</span><span class="sxs-lookup"><span data-stu-id="d3cf3-146">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="d3cf3-147">IID</span><span class="sxs-lookup"><span data-stu-id="d3cf3-147">IID</span></span><br/>                      | <span data-ttu-id="d3cf3-148">IID \_ iswbejebjectex</span><span class="sxs-lookup"><span data-stu-id="d3cf3-148">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d3cf3-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3cf3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3cf3-150">**Austauschen von "errbemubjectex"**</span><span class="sxs-lookup"><span data-stu-id="d3cf3-150">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="d3cf3-151">Überwachen von Leistungsdaten</span><span class="sxs-lookup"><span data-stu-id="d3cf3-151">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

