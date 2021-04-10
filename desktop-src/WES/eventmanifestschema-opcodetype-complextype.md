---
title: Komplexer OpCodeType-Typ
description: Definiert einen Vorgang innerhalb einer Komponente der Anwendung.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- Typ des komplexen OpCodeType-Typs EventLog
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5abaa11373086fe7f1237e10daf3e0a3df1cdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106023"
---
# <a name="opcodetype-complex-type"></a><span data-ttu-id="70f74-104">Komplexer OpCodeType-Typ</span><span class="sxs-lookup"><span data-stu-id="70f74-104">OpcodeType Complex Type</span></span>

<span data-ttu-id="70f74-105">Definiert einen Vorgang innerhalb einer Komponente der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="70f74-105">Defines an operation within a component of the application.</span></span> <span data-ttu-id="70f74-106">Wird in Verbindung mit einer-Aufgabe verwendet, um den Abschnitt der Anwendung zu identifizieren, der das Ereignis protokolliert.</span><span class="sxs-lookup"><span data-stu-id="70f74-106">Used in conjunction with a task to identify the section of the application that is logging the event.</span></span>

``` syntax
<xs:complexType name="OpcodeType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="mofValue"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="70f74-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="70f74-107">Attributes</span></span>



| <span data-ttu-id="70f74-108">Name</span><span class="sxs-lookup"><span data-stu-id="70f74-108">Name</span></span>     | <span data-ttu-id="70f74-109">type</span><span class="sxs-lookup"><span data-stu-id="70f74-109">Type</span></span>                                                              | <span data-ttu-id="70f74-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70f74-110">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f74-111">message</span><span class="sxs-lookup"><span data-stu-id="70f74-111">message</span></span>  | [<span data-ttu-id="70f74-112">**"Strauch"**</span><span class="sxs-lookup"><span data-stu-id="70f74-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="70f74-113">Der lokalisierte Anzeige Name für den Opcode.</span><span class="sxs-lookup"><span data-stu-id="70f74-113">The localized display name for the opcode.</span></span> <span data-ttu-id="70f74-114">Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests.</span><span class="sxs-lookup"><span data-stu-id="70f74-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                     |
| <span data-ttu-id="70f74-115">MUF-Wert</span><span class="sxs-lookup"><span data-stu-id="70f74-115">mofValue</span></span> | [<span data-ttu-id="70f74-116">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="70f74-116">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="70f74-117">Nur für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="70f74-117">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="70f74-118">name</span><span class="sxs-lookup"><span data-stu-id="70f74-118">name</span></span>     | <span data-ttu-id="70f74-119">**QName**</span><span class="sxs-lookup"><span data-stu-id="70f74-119">**QName**</span></span>                                                         | <span data-ttu-id="70f74-120">Der Name des OpCodes.</span><span class="sxs-lookup"><span data-stu-id="70f74-120">The name of the opcode.</span></span> <span data-ttu-id="70f74-121">Dieser Name muss innerhalb des Gültigkeits Bereichs dieses Anbieters eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="70f74-121">This name must be unique within the scope of this provider.</span></span> <br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="70f74-122">Symbol</span><span class="sxs-lookup"><span data-stu-id="70f74-122">symbol</span></span>   | [<span data-ttu-id="70f74-123">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="70f74-123">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="70f74-124">Das Symbol, das für den Verweis auf den Opcode in der Anwendung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="70f74-124">The symbol to use to reference the opcode in your application.</span></span> <span data-ttu-id="70f74-125">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Opcode in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="70f74-125">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the opcode in the header file that the compiler generates.</span></span> <span data-ttu-id="70f74-126">Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.</span><span class="sxs-lookup"><span data-stu-id="70f74-126">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="70f74-127">value</span><span class="sxs-lookup"><span data-stu-id="70f74-127">value</span></span>    | [<span data-ttu-id="70f74-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="70f74-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="70f74-129">Der opcodewert.</span><span class="sxs-lookup"><span data-stu-id="70f74-129">The opcode value.</span></span> <span data-ttu-id="70f74-130">Sie können Werte im Bereich 10 und 239 angeben.</span><span class="sxs-lookup"><span data-stu-id="70f74-130">You can specify values in the range 10 and 239.</span></span> <span data-ttu-id="70f74-131">Eine Liste der vordefinierten opcodewerte finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="70f74-131">For a list of predefined opcode values, see Remarks.</span></span><br/>                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="70f74-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70f74-132">Remarks</span></span>

<span data-ttu-id="70f74-133">Im folgenden sind die vordefinierten Opcode-Werte enthalten, die Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="70f74-133">The following are the predefined opcode values that you can use.</span></span> <span data-ttu-id="70f74-134">Diese Werte werden in der Winmeta.xml-Datei definiert, die in der Windows SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="70f74-134">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="70f74-135">Name</span><span class="sxs-lookup"><span data-stu-id="70f74-135">Name</span></span>          | <span data-ttu-id="70f74-136">Wert</span><span class="sxs-lookup"><span data-stu-id="70f74-136">Value</span></span> | <span data-ttu-id="70f74-137">Symbol</span><span class="sxs-lookup"><span data-stu-id="70f74-137">Symbol</span></span>                      | <span data-ttu-id="70f74-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="70f74-138">Description</span></span>                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f74-139">Win: info</span><span class="sxs-lookup"><span data-stu-id="70f74-139">win:Info</span></span>      | <span data-ttu-id="70f74-140">0</span><span class="sxs-lookup"><span data-stu-id="70f74-140">0</span></span>     | <span data-ttu-id="70f74-141">WinEvent- \_ Opcode- \_ Informationen</span><span class="sxs-lookup"><span data-stu-id="70f74-141">WINEVENT\_OPCODE\_INFO</span></span>      | <span data-ttu-id="70f74-142">Ein Informationsereignis.</span><span class="sxs-lookup"><span data-stu-id="70f74-142">An informational event.</span></span>                                                                                |
| <span data-ttu-id="70f74-143">Win: Start</span><span class="sxs-lookup"><span data-stu-id="70f74-143">win:Start</span></span>     | <span data-ttu-id="70f74-144">1</span><span class="sxs-lookup"><span data-stu-id="70f74-144">1</span></span>     | <span data-ttu-id="70f74-145">WinEvent- \_ Opcode \_ starten</span><span class="sxs-lookup"><span data-stu-id="70f74-145">WINEVENT\_OPCODE\_START</span></span>     | <span data-ttu-id="70f74-146">Ein Ereignis, das das Starten einer Aktivität darstellt.</span><span class="sxs-lookup"><span data-stu-id="70f74-146">An event that represents starting an activity.</span></span>                                                         |
| <span data-ttu-id="70f74-147">Win: beendet</span><span class="sxs-lookup"><span data-stu-id="70f74-147">win:Stop</span></span>      | <span data-ttu-id="70f74-148">2</span><span class="sxs-lookup"><span data-stu-id="70f74-148">2</span></span>     | <span data-ttu-id="70f74-149">WinEvent \_ Opcode wird \_ beendet.</span><span class="sxs-lookup"><span data-stu-id="70f74-149">WINEVENT\_OPCODE\_STOP</span></span>      | <span data-ttu-id="70f74-150">Ein Ereignis, das das Beenden einer Aktivität darstellt.</span><span class="sxs-lookup"><span data-stu-id="70f74-150">An event that represents stopping an activity.</span></span> <span data-ttu-id="70f74-151">Das Ereignis entspricht dem letzten nicht paarweise zugeordneten Start Ereignis.</span><span class="sxs-lookup"><span data-stu-id="70f74-151">The event corresponds to the last unpaired start event.</span></span> |
| <span data-ttu-id="70f74-152">Win: DC- \_ Start</span><span class="sxs-lookup"><span data-stu-id="70f74-152">win:DC\_Start</span></span> | <span data-ttu-id="70f74-153">3</span><span class="sxs-lookup"><span data-stu-id="70f74-153">3</span></span>     | <span data-ttu-id="70f74-154">WinEvent- \_ Opcode- \_ DC- \_ Start</span><span class="sxs-lookup"><span data-stu-id="70f74-154">WINEVENT\_OPCODE\_DC\_START</span></span> | <span data-ttu-id="70f74-155">Ein Ereignis, das das Starten der Datensammlung darstellt.</span><span class="sxs-lookup"><span data-stu-id="70f74-155">An event that represents data collection starting.</span></span> <span data-ttu-id="70f74-156">Dabei handelt es sich um Rundown-Ereignis Typen.</span><span class="sxs-lookup"><span data-stu-id="70f74-156">These are rundown event types.</span></span>                      |
| <span data-ttu-id="70f74-157">Win: DC- \_ Beendigung</span><span class="sxs-lookup"><span data-stu-id="70f74-157">win:DC\_Stop</span></span>  | <span data-ttu-id="70f74-158">4</span><span class="sxs-lookup"><span data-stu-id="70f74-158">4</span></span>     | <span data-ttu-id="70f74-159">WinEvent- \_ Opcode-DC-Vorgang \_ \_ beendet</span><span class="sxs-lookup"><span data-stu-id="70f74-159">WINEVENT\_OPCODE\_DC\_STOP</span></span>  | <span data-ttu-id="70f74-160">Ein Ereignis, das das Beenden der Datensammlung darstellt.</span><span class="sxs-lookup"><span data-stu-id="70f74-160">An event that represents data collection stopping.</span></span> <span data-ttu-id="70f74-161">Dabei handelt es sich um Rundown-Ereignis Typen.</span><span class="sxs-lookup"><span data-stu-id="70f74-161">These are rundown event types.</span></span>                      |
| <span data-ttu-id="70f74-162">Win: Erweiterung</span><span class="sxs-lookup"><span data-stu-id="70f74-162">win:Extension</span></span> | <span data-ttu-id="70f74-163">5</span><span class="sxs-lookup"><span data-stu-id="70f74-163">5</span></span>     | <span data-ttu-id="70f74-164">WinEvent- \_ Opcode- \_ Erweiterung</span><span class="sxs-lookup"><span data-stu-id="70f74-164">WINEVENT\_OPCODE\_EXTENSION</span></span> | <span data-ttu-id="70f74-165">Ein Erweiterungsereignis.</span><span class="sxs-lookup"><span data-stu-id="70f74-165">An extension event.</span></span>                                                                                    |
| <span data-ttu-id="70f74-166">Win: Reply</span><span class="sxs-lookup"><span data-stu-id="70f74-166">win:Reply</span></span>     | <span data-ttu-id="70f74-167">6</span><span class="sxs-lookup"><span data-stu-id="70f74-167">6</span></span>     | <span data-ttu-id="70f74-168">WinEvent- \_ Opcode- \_ Antwort</span><span class="sxs-lookup"><span data-stu-id="70f74-168">WINEVENT\_OPCODE\_REPLY</span></span>     | <span data-ttu-id="70f74-169">Ein Antwort Ereignis.</span><span class="sxs-lookup"><span data-stu-id="70f74-169">A reply event.</span></span>                                                                                         |
| <span data-ttu-id="70f74-170">Win: Resume</span><span class="sxs-lookup"><span data-stu-id="70f74-170">win:Resume</span></span>    | <span data-ttu-id="70f74-171">7</span><span class="sxs-lookup"><span data-stu-id="70f74-171">7</span></span>     | <span data-ttu-id="70f74-172">Wiederaufnahme von WinEvent- \_ Opcode \_</span><span class="sxs-lookup"><span data-stu-id="70f74-172">WINEVENT\_OPCODE\_RESUME</span></span>    | <span data-ttu-id="70f74-173">Ein Ereignis, das eine Aktivität darstellt, die nach dem aussetzen fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="70f74-173">An event that represents an activity resuming after being suspended.</span></span>                                   |
| <span data-ttu-id="70f74-174">Win: Suspend</span><span class="sxs-lookup"><span data-stu-id="70f74-174">win:Suspend</span></span>   | <span data-ttu-id="70f74-175">8</span><span class="sxs-lookup"><span data-stu-id="70f74-175">8</span></span>     | <span data-ttu-id="70f74-176">WinEvent \_ Opcode \_ Suspend</span><span class="sxs-lookup"><span data-stu-id="70f74-176">WINEVENT\_OPCODE\_SUSPEND</span></span>   | <span data-ttu-id="70f74-177">Ein Ereignis, das die angehaltene Aktivität darstellt, die den Abschluss einer anderen Aktivität aussteht.</span><span class="sxs-lookup"><span data-stu-id="70f74-177">An event that represents the activity being suspended pending another activity's completion.</span></span>           |
| <span data-ttu-id="70f74-178">Win: Send</span><span class="sxs-lookup"><span data-stu-id="70f74-178">win:Send</span></span>      | <span data-ttu-id="70f74-179">9</span><span class="sxs-lookup"><span data-stu-id="70f74-179">9</span></span>     | <span data-ttu-id="70f74-180">WinEvent \_ Opcode \_ Send</span><span class="sxs-lookup"><span data-stu-id="70f74-180">WINEVENT\_OPCODE\_SEND</span></span>      | <span data-ttu-id="70f74-181">Ein Ereignis, das die Übertragung von Aktivitäten an eine andere Komponente darstellt.</span><span class="sxs-lookup"><span data-stu-id="70f74-181">An event that represents transferring activity to another component.</span></span>                                   |
| <span data-ttu-id="70f74-182">Win: empfangen</span><span class="sxs-lookup"><span data-stu-id="70f74-182">win:Receive</span></span>   | <span data-ttu-id="70f74-183">240</span><span class="sxs-lookup"><span data-stu-id="70f74-183">240</span></span>   | <span data-ttu-id="70f74-184">WinEvent- \_ Opcode \_ empfangen</span><span class="sxs-lookup"><span data-stu-id="70f74-184">WINEVENT\_OPCODE\_RECEIVE</span></span>   | <span data-ttu-id="70f74-185">Ein Ereignis, das den Empfang einer Aktivitäts Übertragung von einer anderen Komponente darstellt.</span><span class="sxs-lookup"><span data-stu-id="70f74-185">An event that represents receiving an activity transfer from another component.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="70f74-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70f74-186">Requirements</span></span>



| <span data-ttu-id="70f74-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70f74-187">Requirement</span></span> | <span data-ttu-id="70f74-188">Wert</span><span class="sxs-lookup"><span data-stu-id="70f74-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="70f74-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70f74-189">Minimum supported client</span></span><br/> | <span data-ttu-id="70f74-190">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70f74-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="70f74-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70f74-191">Minimum supported server</span></span><br/> | <span data-ttu-id="70f74-192">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70f74-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





