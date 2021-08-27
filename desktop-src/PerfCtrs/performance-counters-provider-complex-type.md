---
description: Definiert einen Anbieter und die leistungsindikatoren, die er bietet.
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: provider Complex Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94654c538cc0637e6c90e0b14d3433b979762b00
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622716"
---
# <a name="provider-complex-type"></a>provider Complex Type

Definiert einen Anbieter und die leistungsindikatoren, die er bietet.

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

## <a name="child-elements"></a>Untergeordnete Elemente



| Element        | Typ                                                                   | Beschreibung                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **Counterset** | [**man:counterSet**](performance-counters-counterset-complex-type.md) | Identifiziert den Indikatorsatz, der einen oder mehrere logisch verknüpfte Leistungsindikatoren enthält.<br/> |



## <a name="attributes"></a>Attributes



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>Typ</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Applicationidentity</td>
<td><strong>xs:string</strong></td>
<td>Der Name der Binärdatei, die die lokalisierten Ressourcenzeichenfolgen enthält, entweder eine .exe- oder .dll-Datei (ohne den Pfad zur Binärdatei).<br/> Das Lodctr.exe verwendet den Pfad aus dem optionalen Parameter [<em>path</em>] , um nach der Binärdatei zu suchen. Beispiel: <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>pfad</em>]]. Wenn Sie den [path<em>]-Parameter</em>nicht angeben, Lodctr.exe den Ordner, der das Manifest enthält, durchsucht.<br/></td>
</tr>
<tr class="even">
<td>Rückruf</td>

<td>Dieses Attribut gibt an, dass Sie eine Benachrichtigung erhalten möchten, wenn ein Consumer bestimmte Aktionen ausführt. <br/> Wenn Sie dieses Attribut angeben, verwendet das CTRPP-Tool die alternative <a href="counterinitialize.md"><strong>CounterInitialize-Funktionssignatur,</strong></a> mit der Sie den Namen Ihrer Funktion übergeben, die die <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback-Rückruffunktion</strong></a> implementiert.<br/> Alternativ zur Angabe dieses Attributs können Sie das <strong>CTRPP-Argument -NotificationCallback</strong><a href="ctrpp.md"></a> verwenden.<br/> <strong>Windows Vista:</strong> Der einzige gültige Wert für dieses Attribut ist &quot; der benutzerdefinierte &quot; . Das <a href="ctrpp.md">CTRPP-Hilfsprogramm</a> generiert die Vorlage für eine <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback-Rückruffunktion.</strong></a> Die Vorlage ist in der C-Datei enthalten, die von CTRPP generiert wurde. <br/> <br/></td>
</tr>
<tr class="odd">
<td>providerGuid</td>
<td><a href="performance-counters-guidtype-simple-type.md"><strong>man:GUIDType</strong></a></td>
<td>Zeichenfolgen-GUID, die den Anbieter im Manifest eindeutig identifiziert. Die GUID muss innerhalb des Manifests eindeutig sein.<br/> Sie müssen nur dann eine neue GUID bereitstellen, wenn sich die Version der Anwendung ändert (wenn Sie nebenseitige Installationen unterstützen).<br/></td>
</tr>
<tr class="even">
<td>providerName</td>
<td><strong>xs:string</strong></td>
<td>Der Name, der zum Erstellen des WMI-Win32_PerfRawData klassenname verwendet wird. Wenn Sie keinen Namen angeben, wird &quot; Counters &quot; als Name der Klasse verwendet.<br/></td>
</tr>
<tr class="odd">
<td>Providertype</td>

<td>Gibt an, ob der Anbieter ein Benutzermodusanbieter, Kernelmodusanbieter oder Treiberanbieter ist. Die folgenden Werte sind möglich.<br/> 
<table>
<thead>
<tr class="header">
<th>Begriff</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>Usermode<br/></td>
<td>Geben Sie diesen Modus für eine Benutzermoduskomponente an, z. B. eine Anwendung, eine DLL oder einen Benutzermodustreiber. Die typischen Erweiterungen für Benutzermoduskomponenten sind .exe oder .dll. Dies ist die Standardoption.<br/></td>
</tr>
<tr class="even">
<td><span id="kernel"></span><span id="KERNEL"></span>Kernel<br/></td>
<td>Geben Sie diesen Modus für eine Kernelmoduskomponente an, z. B. einen WDM- oder WDF-Treiber. Die typische Erweiterung für Kernelmoduskomponenten ist .sys.<br/> <strong>Windows Vista und Windows Server 2008:</strong> Dieser Wert wird erst ab 7 Windows server 2008 R2 Windows server 2008 R2 unterstützt.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>resourceBase</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></td>
<td><p>Definiert den Indexwert der Startressource, den <a href="ctrpp.md">CTRPP</a> zum Generieren der Ressourcenbezeichner verwendet.</p></td>
</tr>
<tr class="odd">
<td>Symbol</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></td>
<td><p>Ein symbolischer Name, der den Anbieter identifiziert. Das <a href="ctrpp.md">CTRPP-Tool</a> erstellt eine HANDLE-Variable, die Sie beim Aufrufen von Funktionen verwenden können, die ein Handle für den Anbieter erfordern (z. B. <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>). Der symbolische Name ist der Name der Variablen.</p>
<p>Wenn Sie das <strong>Argument -prefix beim</strong> Aufrufen von <a href="ctrpp.md">STRPP</a>angeben, wird die Präfixzeichenfolge am Anfang des symbolischen Namens hinzugefügt.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




