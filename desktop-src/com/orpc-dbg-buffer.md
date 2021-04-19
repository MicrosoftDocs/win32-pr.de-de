---
title: ORPC_DBG_BUFFER Struktur
description: Die ORPC \_ dbg- \_ Puffer Struktur ist das Puffer Format, das zum Mars Hallen von RPC-Daten an die Methoden der iorpcdebugnotify-Schnittstelle verwendet wird.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- COM für ORPC_DBG_BUFFER Struktur
- PORPC_DBG_BUFFER Struktur Zeiger com
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc42251b928207a2b009a18c1d88e94dcf1492a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341786"
---
# <a name="orpc_dbg_buffer-structure"></a><span data-ttu-id="c311e-105">ORPC \_ dbg- \_ Puffer Struktur</span><span class="sxs-lookup"><span data-stu-id="c311e-105">ORPC\_DBG\_BUFFER structure</span></span>

<span data-ttu-id="c311e-106">Die **ORPC \_ dbg- \_ Puffer** Struktur ist das Puffer Format, das zum Mars Hallen von RPC-Daten an die Methoden der [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c311e-106">The **ORPC\_DBG\_BUFFER** structure is the buffer format used to marshalled RPC data to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c311e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c311e-107">Syntax</span></span>


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a><span data-ttu-id="c311e-108">Member</span><span class="sxs-lookup"><span data-stu-id="c311e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c311e-109">**alwaysorbisweilen**</span><span class="sxs-lookup"><span data-stu-id="c311e-109">**alwaysOrSometimes**</span></span>
</dt> <dd>

<span data-ttu-id="c311e-110">Ein Wert, der das Erzeugen des Debuggers steuert.</span><span class="sxs-lookup"><span data-stu-id="c311e-110">A value that controls debugger spawning.</span></span> <span data-ttu-id="c311e-111">**alwaysorsometimes** kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="c311e-111">**alwaysOrSometimes** can be one of the following values:</span></span>



| <span data-ttu-id="c311e-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c311e-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="c311e-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c311e-113">Meaning</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <span data-ttu-id="c311e-114"><dt>**ORPC \_ \_Immer**</dt> <dt>0x00000000</dt> Debuggen</span><span class="sxs-lookup"><span data-stu-id="c311e-114"><dt>**ORPC\_DEBUG\_ALWAYS**</dt> <dt>0x00000000</dt></span></span> </dl>                              | <span data-ttu-id="c311e-115">Wenn diese Einstellung festgelegt ist, wird die Client-oder Server Benachrichtigung für den Empfänger immer von com erhoben.</span><span class="sxs-lookup"><span data-stu-id="c311e-115">If set, COM will always raise the client or server notification on the receiver.</span></span><br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <span data-ttu-id="c311e-116"><dt>**ORPC \_ Debuggen, \_ Wenn der \_ Hook \_ aktiviert ist**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c311e-116"><dt>**ORPC\_DEBUG\_IF\_HOOK\_ENABLED**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="c311e-117">Wenn festgelegt, wird von com nur die Client-oder Server Benachrichtigung für den Empfänger ausgegeben, wenn das com-Debuggen aktiviert wurde, indem [**dlldebugobjectrpchook**](dlldebugobjectrpchook.md) in diesem Prozess aufgerufen wird, wobei **ftrace** auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c311e-117">If set, COM will only raise the client or server notification on the receiver if COM debugging has been enabled by calling [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) in that process with **fTrace** set to **TRUE**.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="c311e-118">**verMajor**</span><span class="sxs-lookup"><span data-stu-id="c311e-118">**verMajor**</span></span>
</dt> <dd>

<span data-ttu-id="c311e-119">Die Hauptversionsnummer der Datenformat Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="c311e-119">The major version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="c311e-120">**verMinor**</span><span class="sxs-lookup"><span data-stu-id="c311e-120">**verMinor**</span></span>
</dt> <dd>

<span data-ttu-id="c311e-121">Die neben Versionsnummer der Datenformat Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="c311e-121">The minor version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="c311e-122">**cbremaineing**</span><span class="sxs-lookup"><span data-stu-id="c311e-122">**cbRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="c311e-123">Die Anzahl von Bytes (einschließlich **cbremaineing**), die in dieser-Struktur befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="c311e-123">The number of bytes, inclusive of **cbRemaining**, that follow in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="c311e-124">**guidsemantic**</span><span class="sxs-lookup"><span data-stu-id="c311e-124">**guidSemantic**</span></span>
</dt> <dd>

<span data-ttu-id="c311e-125">Eine GUID, die bestimmt, welche Member der Union unten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c311e-125">A GUID that determines which members of the union are present below.</span></span> <span data-ttu-id="c311e-126">**guidsemantic** kann einen der folgenden Werte annehmen:</span><span class="sxs-lookup"><span data-stu-id="c311e-126">**guidSemantic** can take one of the following values:</span></span>



| <span data-ttu-id="c311e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c311e-127">Value</span></span>                                                                                                           | <span data-ttu-id="c311e-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c311e-128">Meaning</span></span>                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c311e-129"><dt>9cade560-8F 43-101A-b07b-00dd01113f 11</dt></span><span class="sxs-lookup"><span data-stu-id="c311e-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span></span> </dl> | <span data-ttu-id="c311e-130">Bestimmt, ob ein Einzelschritt vom Debugger ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c311e-130">Determines if single stepping is to be performed by the debugger.</span></span> <span data-ttu-id="c311e-131">Im folgenden ist nur das **fstoponotherside** -Member der Union vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c311e-131">Only the **fStopOnOtherSide** member of the union is present below.</span></span><br/>                                             |
| <dl> <span data-ttu-id="c311e-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="c311e-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="c311e-133">Bestimmt, ob die an den Empfänger gemarshallte RPC-Daten und debugopcodes übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="c311e-133">Determines if RPC marshalled data and debugging opcodes are passed to the receiver.</span></span> <span data-ttu-id="c311e-134">Alle Member der Union sind unten mit Ausnahme von **fstoponotherside** enthalten.</span><span class="sxs-lookup"><span data-stu-id="c311e-134">All of the members of the union are present below with the exception of **fStopOnOtherSide**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c311e-135">**"f"**</span><span class="sxs-lookup"><span data-stu-id="c311e-135">**fStopOnOtherSide**</span></span>
</dt> <dd>

<span data-ttu-id="c311e-136">**True** gibt an, dass der Debugger einen Einzelschritt durchläuft und den Server ausführen und die Ausführung fortsetzen soll, sobald die andere Seite erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="c311e-136">If **TRUE**, single stepping is performed by the debugger and it should step out of the server and continue execution once the other side is reached.</span></span> <span data-ttu-id="c311e-137">Andernfalls wird ein Einzelschritt nicht durchgeführt, und die Debugger-Ausführung wird auf der anderen Seite angehalten.</span><span class="sxs-lookup"><span data-stu-id="c311e-137">Otherwise, single stepping is not performed and debugger execution stops on the other side.</span></span>

</dd> <dt>

<span data-ttu-id="c311e-138">**wdebuggingopcode**</span><span class="sxs-lookup"><span data-stu-id="c311e-138">**wDebuggingOpCode**</span></span>
</dt> <dd>

<span data-ttu-id="c311e-139">Ein Wert, mit dem eine Reihe von Vorgängen angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="c311e-139">A value that allows for one of a series of operations to be specified.</span></span> <span data-ttu-id="c311e-140">**wdebuggingopcode** kann einen der folgenden Werte annehmen:</span><span class="sxs-lookup"><span data-stu-id="c311e-140">**wDebuggingOpCode** can take one of the following values:</span></span>



| <span data-ttu-id="c311e-141">Wert</span><span class="sxs-lookup"><span data-stu-id="c311e-141">Value</span></span>                                                                             | <span data-ttu-id="c311e-142">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c311e-142">Meaning</span></span>                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c311e-143"><dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="c311e-143"><dt>0x0000</dt></span></span> </dl> | <span data-ttu-id="c311e-144">Keine Operation.</span><span class="sxs-lookup"><span data-stu-id="c311e-144">No operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="c311e-145"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c311e-145"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="c311e-146">Wenn der Wert festgelegt ist, ist die Semantik mit einem Schritt mit **fstoponotherside** identisch, wenn auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c311e-146">If set, single step semantics are identical to **fStopOnOtherSide** when set to **TRUE**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c311e-147">**cblock**</span><span class="sxs-lookup"><span data-stu-id="c311e-147">**cExtent**</span></span>
</dt> <dd>

<span data-ttu-id="c311e-148">Auffüllung.</span><span class="sxs-lookup"><span data-stu-id="c311e-148">Padding.</span></span> <span data-ttu-id="c311e-149">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c311e-149">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="c311e-150">**padding**</span><span class="sxs-lookup"><span data-stu-id="c311e-150">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="c311e-151">Auffüllung.</span><span class="sxs-lookup"><span data-stu-id="c311e-151">Padding.</span></span> <span data-ttu-id="c311e-152">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c311e-152">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="c311e-153">**betrieben**</span><span class="sxs-lookup"><span data-stu-id="c311e-153">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="c311e-154">Die Größe in Bytes der Daten in **rgbData**.</span><span class="sxs-lookup"><span data-stu-id="c311e-154">The size, in bytes of the data in **rgbData**.</span></span>

</dd> <dt>

<span data-ttu-id="c311e-155">**guidextent**</span><span class="sxs-lookup"><span data-stu-id="c311e-155">**guidExtent**</span></span>
</dt> <dd>

<span data-ttu-id="c311e-156">Eine **GUID** , die den Typ der Daten in **rgbData** bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c311e-156">A **GUID** that determines the type of data in **rgbData**.</span></span> <span data-ttu-id="c311e-157">" **guidextent** " kann einen der folgenden Werte annehmen:</span><span class="sxs-lookup"><span data-stu-id="c311e-157">**guidExtent** can take one of the following values:</span></span>



| <span data-ttu-id="c311e-158">Wert</span><span class="sxs-lookup"><span data-stu-id="c311e-158">Value</span></span>                                                                                                           | <span data-ttu-id="c311e-159">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c311e-159">Meaning</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="c311e-160"><dt>53199051-57eb-11CE-a964-00aa006c3706</dt></span><span class="sxs-lookup"><span data-stu-id="c311e-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="c311e-161">**rgbData** ist ein marshallte Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c311e-161">**rgbData** is a marshalled interface pointer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c311e-162">**rgbData**</span><span class="sxs-lookup"><span data-stu-id="c311e-162">**rgbData**</span></span>
</dt> <dd>

<span data-ttu-id="c311e-163">Ein **Byte** Puffer, der verwendet wird, um RPC-Daten zwischen den Client-und serverbuggern zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="c311e-163">A **BYTE** buffer used to pass RPC marshalled COM data between the client and server debuggers.</span></span> <span data-ttu-id="c311e-164">Der Inhalt von **rgbData** wird durch die **GUID** in " **guidextent**" bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c311e-164">The contents of **rgbData** are determined by the **GUID** in **guidExtent**.</span></span>



| <span data-ttu-id="c311e-165">Wert für "guidextent"</span><span class="sxs-lookup"><span data-stu-id="c311e-165">guidExtent Value</span></span>                     | <span data-ttu-id="c311e-166">rgbData-Inhalt</span><span class="sxs-lookup"><span data-stu-id="c311e-166">rgbData contents</span></span>                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c311e-167">53199051-57eb-11CE-a964-00aa006c3706</span><span class="sxs-lookup"><span data-stu-id="c311e-167">53199051-57EB-11ce-A964-00AA006C3706</span></span> | <span data-ttu-id="c311e-168">Ein gemarshallte Schnittstellen Zeiger, der sich aus dem Aufruf von [**comarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)ergibt.</span><span class="sxs-lookup"><span data-stu-id="c311e-168">A marshalled interface pointer that results from calling [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface).</span></span> <span data-ttu-id="c311e-169">Der Marshalling-Zeiger wird mithilfe von " [**count**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)" in den entsprechenden Schnittstellen Zeiger konvertiert.</span><span class="sxs-lookup"><span data-stu-id="c311e-169">The marshalled pointer is converted into its corresponding interface pointer using [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c311e-170">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c311e-170">Remarks</span></span>

<span data-ttu-id="c311e-171">Diese Member dieser Struktur haben eine 1-Byte-Ausrichtung und werden immer in Little-Endian-Byte Reihenfolge übertragen.</span><span class="sxs-lookup"><span data-stu-id="c311e-171">This members of this structure have 1-byte alignment and are always transmitted in little-endian byte order.</span></span>

## <a name="requirements"></a><span data-ttu-id="c311e-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c311e-172">Requirements</span></span>



| <span data-ttu-id="c311e-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c311e-173">Requirement</span></span> | <span data-ttu-id="c311e-174">Wert</span><span class="sxs-lookup"><span data-stu-id="c311e-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="c311e-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c311e-175">Minimum supported client</span></span><br/> | <span data-ttu-id="c311e-176">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c311e-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="c311e-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c311e-177">Minimum supported server</span></span><br/> | <span data-ttu-id="c311e-178">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c311e-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c311e-179">Header</span><span class="sxs-lookup"><span data-stu-id="c311e-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="c311e-180"><dt>N/V</dt></span><span class="sxs-lookup"><span data-stu-id="c311e-180"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c311e-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c311e-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c311e-182">**ORPC \_ dbg \_ alle**</span><span class="sxs-lookup"><span data-stu-id="c311e-182">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="c311e-183">**ORPC-init-Argumente \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c311e-183">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="c311e-184">**Dlldebugobjectrpchook**</span><span class="sxs-lookup"><span data-stu-id="c311e-184">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="c311e-185">**Iorpcdebug-Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="c311e-185">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





