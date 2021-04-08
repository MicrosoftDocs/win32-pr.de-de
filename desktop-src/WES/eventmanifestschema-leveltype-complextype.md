---
title: Komplexer leveltype-Typ
description: Definiert einen Schweregrad Wert, der die Ausführlichkeit der protokollierten Ereignisse bestimmt.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- "\"Leveltype\"-Ereignisprotokoll Komplex"
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 237b38890283769e9aac20c9b3a3703ff4b72d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102934"
---
# <a name="leveltype-complex-type"></a><span data-ttu-id="96434-104">Komplexer leveltype-Typ</span><span class="sxs-lookup"><span data-stu-id="96434-104">LevelType Complex Type</span></span>

<span data-ttu-id="96434-105">Definiert einen Schweregrad Wert, der die Ausführlichkeit der protokollierten Ereignisse bestimmt.</span><span class="sxs-lookup"><span data-stu-id="96434-105">Defines a severity value that determines the verbosity of the events being logged.</span></span>

``` syntax
<xs:complexType name="LevelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
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
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="96434-106">Attributes</span><span class="sxs-lookup"><span data-stu-id="96434-106">Attributes</span></span>



| <span data-ttu-id="96434-107">Name</span><span class="sxs-lookup"><span data-stu-id="96434-107">Name</span></span>    | <span data-ttu-id="96434-108">type</span><span class="sxs-lookup"><span data-stu-id="96434-108">Type</span></span>                                                              | <span data-ttu-id="96434-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96434-109">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96434-110">message</span><span class="sxs-lookup"><span data-stu-id="96434-110">message</span></span> | [<span data-ttu-id="96434-111">**"Strauch"**</span><span class="sxs-lookup"><span data-stu-id="96434-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="96434-112">Der lokalisierte Anzeige Name für die Ebene.</span><span class="sxs-lookup"><span data-stu-id="96434-112">The localized display name for the level.</span></span> <span data-ttu-id="96434-113">Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests.</span><span class="sxs-lookup"><span data-stu-id="96434-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                    |
| <span data-ttu-id="96434-114">name</span><span class="sxs-lookup"><span data-stu-id="96434-114">name</span></span>    | <span data-ttu-id="96434-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="96434-115">**QName**</span></span>                                                         | <span data-ttu-id="96434-116">Der Name, der dieser Ebene zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="96434-116">The name to assign to this level.</span></span> <span data-ttu-id="96434-117">Dieser Name muss innerhalb des Bereichs des Anbieters eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="96434-117">This name must be unique within the scope of the provider.</span></span><br/>                                                                                                                                                                                                            |
| <span data-ttu-id="96434-118">Symbol</span><span class="sxs-lookup"><span data-stu-id="96434-118">symbol</span></span>  | [<span data-ttu-id="96434-119">**Csymboltype**</span><span class="sxs-lookup"><span data-stu-id="96434-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="96434-120">Das Symbol, das verwendet werden soll, um auf die Ebene in der Anwendung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="96434-120">The symbol to use to reference the level in your application.</span></span> <span data-ttu-id="96434-121">Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für die Ebene in der vom Compiler generierten Header Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="96434-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the level in the header file that the compiler generates.</span></span> <span data-ttu-id="96434-122">Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.</span><span class="sxs-lookup"><span data-stu-id="96434-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="96434-123">value</span><span class="sxs-lookup"><span data-stu-id="96434-123">value</span></span>   | [<span data-ttu-id="96434-124">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="96434-124">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="96434-125">Der Wert der Ebene.</span><span class="sxs-lookup"><span data-stu-id="96434-125">The level value.</span></span> <span data-ttu-id="96434-126">Sie können Werte im Bereich von 16 bis 255 angeben.</span><span class="sxs-lookup"><span data-stu-id="96434-126">You can specify values in the range 16 to 255.</span></span> <span data-ttu-id="96434-127">Informationen zu vordefinierten Werten finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="96434-127">For predefined level values, see Remarks.</span></span><br/>                                                                                                                                                                                               |



## <a name="remarks"></a><span data-ttu-id="96434-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96434-128">Remarks</span></span>

<span data-ttu-id="96434-129">Im folgenden sind die vordefinierten Ebenen-Werte, die Sie verwenden können, fest.</span><span class="sxs-lookup"><span data-stu-id="96434-129">The following are the predefined level values that you can use.</span></span> <span data-ttu-id="96434-130">Diese Werte werden in der Winmeta.xml-Datei definiert, die in der Windows SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="96434-130">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="96434-131">Name</span><span class="sxs-lookup"><span data-stu-id="96434-131">Name</span></span>              | <span data-ttu-id="96434-132">Wert</span><span class="sxs-lookup"><span data-stu-id="96434-132">Value</span></span> | <span data-ttu-id="96434-133">Symbol</span><span class="sxs-lookup"><span data-stu-id="96434-133">Symbol</span></span>                    | <span data-ttu-id="96434-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="96434-134">Description</span></span>                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="96434-135">win:Critical</span><span class="sxs-lookup"><span data-stu-id="96434-135">win:Critical</span></span>      | <span data-ttu-id="96434-136">1</span><span class="sxs-lookup"><span data-stu-id="96434-136">1</span></span>     | <span data-ttu-id="96434-137">WinEvent- \_ Ebene \_ kritisch</span><span class="sxs-lookup"><span data-stu-id="96434-137">WINEVENT\_LEVEL\_CRITICAL</span></span> | <span data-ttu-id="96434-138">Identifiziert ein nicht normales Exit-oder Beendigungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="96434-138">Identifies an abnormal exit or termination event.</span></span><br/>            |
| <span data-ttu-id="96434-139">win:Error</span><span class="sxs-lookup"><span data-stu-id="96434-139">win:Error</span></span>         | <span data-ttu-id="96434-140">2</span><span class="sxs-lookup"><span data-stu-id="96434-140">2</span></span>     | <span data-ttu-id="96434-141">Fehler auf \_ winereignisebene \_</span><span class="sxs-lookup"><span data-stu-id="96434-141">WINEVENT\_LEVEL\_ERROR</span></span>    | <span data-ttu-id="96434-142">Identifiziert ein schwerwiegendes Fehler Ereignis.</span><span class="sxs-lookup"><span data-stu-id="96434-142">Identifies a severe error event.</span></span><br/>                             |
| <span data-ttu-id="96434-143">win:Warning</span><span class="sxs-lookup"><span data-stu-id="96434-143">win:Warning</span></span>       | <span data-ttu-id="96434-144">3</span><span class="sxs-lookup"><span data-stu-id="96434-144">3</span></span>     | <span data-ttu-id="96434-145">Warnung auf \_ winereignisebene \_</span><span class="sxs-lookup"><span data-stu-id="96434-145">WINEVENT\_LEVEL\_WARNING</span></span>  | <span data-ttu-id="96434-146">Identifiziert ein Warn Ereignis, z. b. einen Zuordnungs Fehler.</span><span class="sxs-lookup"><span data-stu-id="96434-146">Identifies a warning event such as an allocation failure.</span></span><br/>    |
| <span data-ttu-id="96434-147">win:Informational</span><span class="sxs-lookup"><span data-stu-id="96434-147">win:Informational</span></span> | <span data-ttu-id="96434-148">4</span><span class="sxs-lookup"><span data-stu-id="96434-148">4</span></span>     | <span data-ttu-id="96434-149">Informationen zur WinEvent- \_ Ebene \_</span><span class="sxs-lookup"><span data-stu-id="96434-149">WINEVENT\_LEVEL\_INFO</span></span>     | <span data-ttu-id="96434-150">Identifiziert ein nicht-Fehler Ereignis, z. b. ein Eingabe-oder ein Exit-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="96434-150">Identifies a non-error event such as an entry or exit event.</span></span><br/> |
| <span data-ttu-id="96434-151">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="96434-151">win:Verbose</span></span>       | <span data-ttu-id="96434-152">5</span><span class="sxs-lookup"><span data-stu-id="96434-152">5</span></span>     | <span data-ttu-id="96434-153">Verbose der WinEvent- \_ Ebene \_</span><span class="sxs-lookup"><span data-stu-id="96434-153">WINEVENT\_LEVEL\_VERBOSE</span></span>  | <span data-ttu-id="96434-154">Identifiziert ein ausführliches Ablauf Verfolgungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="96434-154">Identifies a detailed trace event.</span></span><br/>                           |



 

<span data-ttu-id="96434-155">Eine höhere Anzahl impliziert, dass Sie auch niedrigere Ebenen erhalten.</span><span class="sxs-lookup"><span data-stu-id="96434-155">Higher numbers imply that you get lower levels as well.</span></span> <span data-ttu-id="96434-156">Wenn Sie z. b. "Win: Warning" angeben, werden alle Warnungen, Fehler und kritischen Ereignisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="96434-156">For example, if you specify win:Warning, you receive all warning, error, and critical events.</span></span>

## <a name="requirements"></a><span data-ttu-id="96434-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96434-157">Requirements</span></span>



| <span data-ttu-id="96434-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96434-158">Requirement</span></span> | <span data-ttu-id="96434-159">Wert</span><span class="sxs-lookup"><span data-stu-id="96434-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="96434-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="96434-160">Minimum supported client</span></span><br/> | <span data-ttu-id="96434-161">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96434-161">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="96434-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="96434-162">Minimum supported server</span></span><br/> | <span data-ttu-id="96434-163">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="96434-163">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





