---
description: Definiert einen Anbieter und die Leistungsindikatoren, die er bereitstellt.
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: komplexer Anbietertyp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eec52139710d0ffafe06f22504a735e59312818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865096"
---
# <a name="provider-complex-type"></a><span data-ttu-id="4debc-103">komplexer Anbietertyp</span><span class="sxs-lookup"><span data-stu-id="4debc-103">provider Complex Type</span></span>

<span data-ttu-id="4debc-104">Definiert einen Anbieter und die Leistungsindikatoren, die er bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4debc-104">Defines a provider and the counters that it provides.</span></span>

``` syntax
<xs:complexType name="provider">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="counterSet"
            type="man:counterSet"
        >
            <xs:key name="uniqueCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@id"
                 />
            </xs:key>
            <xs:unique name="uniqueCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:unique>
            <xs:keyref name="existBaseID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@baseID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfTimeID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfTimeID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfFreqID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfFreqID"
                 />
            </xs:keyref>
            <xs:keyref name="existMultiCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@multiCounterID"
                 />
            </xs:keyref>
            <xs:key name="uniqueStructNames">
                <xs:selector
                    xpath="./man:structs/man:struct"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
            <xs:keyref name="existCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@struct"
                 />
            </xs:keyref>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="callback"
        use="optional"
        default="default"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="custom"
                 />
                <xs:enumeration
                    value="default"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerGuid"
        type="man:GUIDType"
        use="required"
     />
    <xs:attribute name="applicationIdentity"
        type="xs:string"
        use="required"
     />
    <xs:attribute name="providerType"
        use="optional"
        default="userMode"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="userMode"
                 />
                <xs:enumeration
                    value="kernelMode"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerName"
        type="xs:string"
        use="optional"
        default="Counters"
     />
    <xs:attribute name="resourceBase"
        type="man:UInt32Type"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="4debc-105">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4debc-105">Child elements</span></span>



| <span data-ttu-id="4debc-106">Element</span><span class="sxs-lookup"><span data-stu-id="4debc-106">Element</span></span>        | <span data-ttu-id="4debc-107">type</span><span class="sxs-lookup"><span data-stu-id="4debc-107">Type</span></span>                                                                   | <span data-ttu-id="4debc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4debc-108">Description</span></span>                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4debc-109">**counterSet**</span><span class="sxs-lookup"><span data-stu-id="4debc-109">**counterSet**</span></span> | [<span data-ttu-id="4debc-110">**man: CounterSet**</span><span class="sxs-lookup"><span data-stu-id="4debc-110">**man:counterSet**</span></span>](performance-counters-counterset-complex-type.md) | <span data-ttu-id="4debc-111">Identifiziert den Indikatorensatz, der mindestens einen logisch verknüpften Zähler enthält.</span><span class="sxs-lookup"><span data-stu-id="4debc-111">Identifies the counter set that contains one or more logically related counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="4debc-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="4debc-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4debc-113">Name</span><span class="sxs-lookup"><span data-stu-id="4debc-113">Name</span></span></th>
<th><span data-ttu-id="4debc-114">type</span><span class="sxs-lookup"><span data-stu-id="4debc-114">Type</span></span></th>
<th><span data-ttu-id="4debc-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4debc-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4debc-116">ApplicationIdentity</span><span class="sxs-lookup"><span data-stu-id="4debc-116">applicationIdentity</span></span></td>
<td><span data-ttu-id="4debc-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="4debc-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="4debc-118">Der Name der Binärdatei, die die lokalisierten Ressourcen Zeichenfolgen enthält, entweder eine exe-oder DLL-Datei (der Pfad zur Binärdatei ist nicht enthalten).</span><span class="sxs-lookup"><span data-stu-id="4debc-118">The name of the binary file that contains the localized resource strings, either an .exe or .dll file (do not include the path to the binary).</span></span><br/> <span data-ttu-id="4debc-119">Das Lodctr.exe-Hilfsprogramm verwendet den Pfad des optionalen [<em>path</em>]-Parameters, um die Binärdatei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="4debc-119">The Lodctr.exe utility uses the path from the optional [<em>path</em>] parameter to search for the binary file.</span></span> <span data-ttu-id="4debc-120">Beispielsweise <strong>Lodctr</strong> [<strong>/m:</strong><em>Manifest</em> [<em>path</em>]].</span><span class="sxs-lookup"><span data-stu-id="4debc-120">For example, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>path</em>]].</span></span> <span data-ttu-id="4debc-121">Wenn Sie den Parameter [<em>path</em>] nicht einschließen, durchsucht Lodctr.exe den Ordner, der das Manifest enthält.</span><span class="sxs-lookup"><span data-stu-id="4debc-121">If you do not include the [<em>path</em>] parameter, Lodctr.exe searches the folder that contains the manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4debc-122">Rückruf</span><span class="sxs-lookup"><span data-stu-id="4debc-122">callback</span></span></td>

<td><span data-ttu-id="4debc-123">Dieses Attribut gibt an, dass Sie eine Benachrichtigung erhalten möchten, wenn ein Consumer bestimmte Aktionen ausführt.</span><span class="sxs-lookup"><span data-stu-id="4debc-123">This attribute indicates that you want to receive notification when a consumer performs certain actions.</span></span> <br/> <span data-ttu-id="4debc-124">Wenn Sie dieses Attribut einschließen, verwendet das ctrpp-Tool die alternative <a href="counterinitialize.md"><strong>counterinitialize</strong></a> -Funktions Signatur, die Sie verwenden, um den Namen der Funktion zu übergeben, die die <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>controlcallback</strong></a> -Rückruffunktion implementiert.</span><span class="sxs-lookup"><span data-stu-id="4debc-124">If you include this attribute, the CTRPP tool uses the alternate <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> function signature, which you use to pass in the name of your function that implements the <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span><br/> <span data-ttu-id="4debc-125">Als Alternative zur Angabe dieses Attributs können Sie das <strong>-notificationcallback-</strong><a href="ctrpp.md">ctrpp</a> -Argument verwenden.</span><span class="sxs-lookup"><span data-stu-id="4debc-125">As an alternative to specifying this attribute, you can use the <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> argument.</span></span><br/> <span data-ttu-id="4debc-126"><strong>Windows Vista:</strong> Der einzige gültige Wert für dieses Attribut ist " &quot; Custom" &quot; .</span><span class="sxs-lookup"><span data-stu-id="4debc-126"><strong>Windows Vista:</strong> The only valid value for this attribute is &quot;custom&quot;.</span></span> <span data-ttu-id="4debc-127">Das Hilfsprogramm <a href="ctrpp.md">ctrpp</a> generiert die Vorlage für eine <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>controlcallback</strong></a> -Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="4debc-127">The <a href="ctrpp.md">CTRPP</a> utility generates the template for a <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span> <span data-ttu-id="4debc-128">Die Vorlage ist in der c-Datei enthalten, die von ctrpp generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4debc-128">The template is included in the .c file that CTRPP generated.</span></span> <br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4debc-129">ProviderGUID</span><span class="sxs-lookup"><span data-stu-id="4debc-129">providerGuid</span></span></td>
<td><span data-ttu-id="4debc-130"><a href="performance-counters-guidtype-simple-type.md"><strong>man: guidtype</strong></a></span><span class="sxs-lookup"><span data-stu-id="4debc-130"><a href="performance-counters-guidtype-simple-type.md"><strong>man:GUIDType</strong></a></span></span></td>
<td><span data-ttu-id="4debc-131">Zeichen folgen-GUID, die den Anbieter im Manifest eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4debc-131">String GUID that uniquely identifies the provider in the manifest.</span></span> <span data-ttu-id="4debc-132">Die GUID muss innerhalb des Manifests eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="4debc-132">The GUID must be unique within the manifest.</span></span><br/> <span data-ttu-id="4debc-133">Sie müssen eine neue GUID nur dann angeben, wenn sich die Version der Anwendung ändert (wenn Sie parallele Installationen unterstützen).</span><span class="sxs-lookup"><span data-stu-id="4debc-133">You need to provide a new GUID only when the version of the application changes (if you support side-by-side installations).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4debc-134">providerName</span><span class="sxs-lookup"><span data-stu-id="4debc-134">providerName</span></span></td>
<td><span data-ttu-id="4debc-135"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="4debc-135"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="4debc-136">Der Name, der verwendet wird, um den WMI-Win32_PerfRawData Klassennamen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4debc-136">The name that is used to create the WMI Win32_PerfRawData class name.</span></span> <span data-ttu-id="4debc-137">Wenn Sie keinen Namen angeben, wird der &quot; &quot; Name der Klasse als Name verwendet.</span><span class="sxs-lookup"><span data-stu-id="4debc-137">If you do not specify a name, &quot;Counters&quot; is used as the name of the class.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4debc-138">Provider Type</span><span class="sxs-lookup"><span data-stu-id="4debc-138">providerType</span></span></td>

<td><span data-ttu-id="4debc-139">Gibt an, ob der Anbieter ein benutzermodusanbieter, kernelmodusanbieter oder Treiber Anbieter ist.</span><span class="sxs-lookup"><span data-stu-id="4debc-139">Identifies whether the provider is a user-mode provider, kernel-mode provider, or driver provider.</span></span> <span data-ttu-id="4debc-140">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="4debc-140">Possible values are as follows.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4debc-141">Begriff</span><span class="sxs-lookup"><span data-stu-id="4debc-141">Term</span></span></th>
<th><span data-ttu-id="4debc-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4debc-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4debc-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode</span><span class="sxs-lookup"><span data-stu-id="4debc-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode</span></span><br/></td>
<td><span data-ttu-id="4debc-144">Geben Sie diesen Modus für eine Benutzermoduskomponente an, z. b. eine Anwendung, eine DLL oder einen Benutzermodustreiber.</span><span class="sxs-lookup"><span data-stu-id="4debc-144">Specify this mode for a user-mode component such as an application, a DLL, or a user-mode driver.</span></span> <span data-ttu-id="4debc-145">Die typischen Erweiterungen für Benutzermoduskomponenten sind exe oder dll.</span><span class="sxs-lookup"><span data-stu-id="4debc-145">The typical extensions for user-mode components are .exe or .dll.</span></span> <span data-ttu-id="4debc-146">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="4debc-146">This is the default.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4debc-147"><span id="kernel"></span><span id="KERNEL"></span>-</span><span class="sxs-lookup"><span data-stu-id="4debc-147"><span id="kernel"></span><span id="KERNEL"></span>kernel</span></span><br/></td>
<td><span data-ttu-id="4debc-148">Geben Sie diesen Modus für eine Kernelmoduskomponente an, z. b. einen WDM-oder WDF-Treiber.</span><span class="sxs-lookup"><span data-stu-id="4debc-148">Specify this mode for a kernel-mode component such as a WDM or WDF driver.</span></span> <span data-ttu-id="4debc-149">Die typische Erweiterung für Kernelmoduskomponenten ist. sys.</span><span class="sxs-lookup"><span data-stu-id="4debc-149">The typical extension for kernel-mode components is .sys.</span></span><br/> <span data-ttu-id="4debc-150"><strong>Windows Vista und Windows Server 2008:</strong> Dieser Wert wird bis Windows 7 und Windows Server 2008 R2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4debc-150"><strong>Windows Vista and Windows Server 2008:</strong> This value is not supported until Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4debc-151">resourcebase</span><span class="sxs-lookup"><span data-stu-id="4debc-151">resourceBase</span></span></td>
<td><span data-ttu-id="4debc-152"><a href="performance-counters-uint32type-simple-type.md"><strong>man: UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="4debc-152"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><p><span data-ttu-id="4debc-153">Definiert den Startwert für den Ressourcen Index, den <a href="ctrpp.md">ctrpp</a> zum Generieren der Ressourcen Bezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="4debc-153">Defines the starting resource index value that <a href="ctrpp.md">CTRPP</a> uses to generate the resource identifiers.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4debc-154">Symbol</span><span class="sxs-lookup"><span data-stu-id="4debc-154">symbol</span></span></td>
<td><span data-ttu-id="4debc-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>man: csymboltype</strong></a></span><span class="sxs-lookup"><span data-stu-id="4debc-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="4debc-156">Ein symbolischer Name, der den Anbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4debc-156">A symbolic name that identifies the provider.</span></span> <span data-ttu-id="4debc-157">Das <a href="ctrpp.md">ctrpp</a> -Tool erstellt eine Handle-Variable, die Sie verwenden können, wenn Sie Funktionen aufrufen, die ein Handle für den Anbieter erfordern (z. b. <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>perfsetulongcountervalue</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="4debc-157">The <a href="ctrpp.md">CTRPP</a> tool creates a HANDLE variable that you can use when calling functions that require a handle to the provider (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>).</span></span> <span data-ttu-id="4debc-158">Der symbolische Name ist der Name der Variablen.</span><span class="sxs-lookup"><span data-stu-id="4debc-158">The symbolic name is the name of the variable.</span></span></p>
<p><span data-ttu-id="4debc-159">Wenn Sie das <strong>-prefix-</strong> Argument beim Aufrufen von <a href="ctrpp.md">ctrpp</a>einschließen, wird die Präfix Zeichenfolge am Anfang des symbolischen Namens hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4debc-159">If you include the <strong>-prefix</strong> argument when calling <a href="ctrpp.md">CTRPP</a>, the prefix string is added to the beginning of the symbolic name.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="4debc-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4debc-160">Requirements</span></span>



| <span data-ttu-id="4debc-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4debc-161">Requirement</span></span> | <span data-ttu-id="4debc-162">Wert</span><span class="sxs-lookup"><span data-stu-id="4debc-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4debc-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4debc-163">Minimum supported client</span></span><br/> | <span data-ttu-id="4debc-164">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4debc-164">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4debc-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4debc-165">Minimum supported server</span></span><br/> | <span data-ttu-id="4debc-166">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4debc-166">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




