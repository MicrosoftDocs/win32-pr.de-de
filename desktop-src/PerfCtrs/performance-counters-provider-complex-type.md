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
# <a name="provider-complex-type"></a>komplexer Anbietertyp

Definiert einen Anbieter und die Leistungsindikatoren, die er bereitstellt.

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



| Element        | type                                                                   | BESCHREIBUNG                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **counterSet** | [**man: CounterSet**](performance-counters-counterset-complex-type.md) | Identifiziert den Indikatorensatz, der mindestens einen logisch verknüpften Zähler enthält.<br/> |



## <a name="attributes"></a>Attributes



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Name</th>
<th>type</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationIdentity</td>
<td><strong>xs:string</strong></td>
<td>Der Name der Binärdatei, die die lokalisierten Ressourcen Zeichenfolgen enthält, entweder eine exe-oder DLL-Datei (der Pfad zur Binärdatei ist nicht enthalten).<br/> Das Lodctr.exe-Hilfsprogramm verwendet den Pfad des optionalen [<em>path</em>]-Parameters, um die Binärdatei zu suchen. Beispielsweise <strong>Lodctr</strong> [<strong>/m:</strong><em>Manifest</em> [<em>path</em>]]. Wenn Sie den Parameter [<em>path</em>] nicht einschließen, durchsucht Lodctr.exe den Ordner, der das Manifest enthält.<br/></td>
</tr>
<tr class="even">
<td>Rückruf</td>

<td>Dieses Attribut gibt an, dass Sie eine Benachrichtigung erhalten möchten, wenn ein Consumer bestimmte Aktionen ausführt. <br/> Wenn Sie dieses Attribut einschließen, verwendet das ctrpp-Tool die alternative <a href="counterinitialize.md"><strong>counterinitialize</strong></a> -Funktions Signatur, die Sie verwenden, um den Namen der Funktion zu übergeben, die die <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>controlcallback</strong></a> -Rückruffunktion implementiert.<br/> Als Alternative zur Angabe dieses Attributs können Sie das <strong>-notificationcallback-</strong><a href="ctrpp.md">ctrpp</a> -Argument verwenden.<br/> <strong>Windows Vista:</strong> Der einzige gültige Wert für dieses Attribut ist " &quot; Custom" &quot; . Das Hilfsprogramm <a href="ctrpp.md">ctrpp</a> generiert die Vorlage für eine <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>controlcallback</strong></a> -Rückruffunktion. Die Vorlage ist in der c-Datei enthalten, die von ctrpp generiert wurde. <br/> <br/></td>
</tr>
<tr class="odd">
<td>ProviderGUID</td>
<td><a href="performance-counters-guidtype-simple-type.md"><strong>man: guidtype</strong></a></td>
<td>Zeichen folgen-GUID, die den Anbieter im Manifest eindeutig identifiziert. Die GUID muss innerhalb des Manifests eindeutig sein.<br/> Sie müssen eine neue GUID nur dann angeben, wenn sich die Version der Anwendung ändert (wenn Sie parallele Installationen unterstützen).<br/></td>
</tr>
<tr class="even">
<td>providerName</td>
<td><strong>xs:string</strong></td>
<td>Der Name, der verwendet wird, um den WMI-Win32_PerfRawData Klassennamen zu erstellen. Wenn Sie keinen Namen angeben, wird der &quot; &quot; Name der Klasse als Name verwendet.<br/></td>
</tr>
<tr class="odd">
<td>Provider Type</td>

<td>Gibt an, ob der Anbieter ein benutzermodusanbieter, kernelmodusanbieter oder Treiber Anbieter ist. Die folgenden Werte sind möglich.<br/> 
<table>
<thead>
<tr class="header">
<th>Begriff</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode<br/></td>
<td>Geben Sie diesen Modus für eine Benutzermoduskomponente an, z. b. eine Anwendung, eine DLL oder einen Benutzermodustreiber. Die typischen Erweiterungen für Benutzermoduskomponenten sind exe oder dll. Dies ist die Standardoption.<br/></td>
</tr>
<tr class="even">
<td><span id="kernel"></span><span id="KERNEL"></span>-<br/></td>
<td>Geben Sie diesen Modus für eine Kernelmoduskomponente an, z. b. einen WDM-oder WDF-Treiber. Die typische Erweiterung für Kernelmoduskomponenten ist. sys.<br/> <strong>Windows Vista und Windows Server 2008:</strong> Dieser Wert wird bis Windows 7 und Windows Server 2008 R2 nicht unterstützt.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>resourcebase</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>man: UInt32Type</strong></a></td>
<td><p>Definiert den Startwert für den Ressourcen Index, den <a href="ctrpp.md">ctrpp</a> zum Generieren der Ressourcen Bezeichner verwendet.</p></td>
</tr>
<tr class="odd">
<td>Symbol</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>man: csymboltype</strong></a></td>
<td><p>Ein symbolischer Name, der den Anbieter identifiziert. Das <a href="ctrpp.md">ctrpp</a> -Tool erstellt eine Handle-Variable, die Sie verwenden können, wenn Sie Funktionen aufrufen, die ein Handle für den Anbieter erfordern (z. b. <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>perfsetulongcountervalue</strong></a>). Der symbolische Name ist der Name der Variablen.</p>
<p>Wenn Sie das <strong>-prefix-</strong> Argument beim Aufrufen von <a href="ctrpp.md">ctrpp</a>einschließen, wird die Präfix Zeichenfolge am Anfang des symbolischen Namens hinzugefügt.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




