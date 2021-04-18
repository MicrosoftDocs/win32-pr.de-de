---
title: Komplexer EventDefinitionType-Typ
description: Definiert ein Ereignis, das von Ihrem Anbieter geschrieben werden kann.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- EventDefinitionType komplexer Typ (Ereignisprotokoll)
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7719abea1e97cae88edd47d176e5c578d73f0b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343891"
---
# <a name="eventdefinitiontype-complex-type"></a>Komplexer EventDefinitionType-Typ

Definiert ein Ereignis, das von Ihrem Anbieter geschrieben werden kann.

``` syntax
<xs:complexType name="EventDefinitionType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="level"
                type="QName"
                use="optional"
             />
            <xs:attribute name="template"
                type="token"
                use="optional"
             />
            <xs:attribute name="channel"
                type="token"
                use="optional"
             />
            <xs:attribute name="keywords"
                type="QNameList"
                use="optional"
             />
            <xs:attribute name="task"
                type="QName"
                use="optional"
             />
            <xs:attribute name="opcode"
                type="QName"
                use="optional"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="version"
                type="unsignedByte"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="notLogged"
                type="boolean"
                use="optional"
                default="false"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

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
<td>Kanal</td>
<td>token</td>
<td>Ein Bezeichner, der den Kanal identifiziert, an den das Ereignis geschrieben wird. Geben Sie einen Kanal Bezeichner für einen der Kanäle an, den Sie definiert oder importiert haben. Wenn der Kanal keinen channelbezeichner angibt, verwenden Sie den Namen des Kanals. Ausführliche Informationen zum Definieren oder Importieren eines Kanals finden Sie unter der komplexe Typ " <a href="eventmanifestschema-channellisttype-complextype.md"><strong>channelellisttype</strong></a> ".<br/> Wenn Sie keinen Kanal angeben, wird das Ereignis nicht in einen Channel geschrieben. In der Regel ist der einzige Grund für die Angabe eines Kanals, dass Sie nur Ereignisse in eine ETW-Sitzung schreiben. Weitere Informationen finden Sie unter Erstellen einer ETW-Sitzung, siehe <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Steuern von Ereignis Ablauf Verfolgungs Sitzungen</a>.<br/></td>
</tr>
<tr class="even">
<td>keywords</td>
<td><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>Qnamelist</strong></a></td>
<td>Eine durch Leerzeichen getrennte Liste von Schlüsselwort Namen, die die Kategorie der Ereignisse identifizieren, zu denen dieses Ereignis gehört. Geben Sie einen Schlüsselwort Namen aus der Liste der Schlüsselwörter an, die Sie definieren. Ausführliche Informationen zum Definieren von Schlüsselwörtern finden Sie unter der komplexe Typ " <a href="eventmanifestschema-keywordtype-complextype.md"><strong>keywordtype</strong></a> ".<br/> Wenn Sie keine Schlüsselwörter angeben, enthält der Ereignis Deskriptor eine 0 (null) für Schlüsselwörter.<br/></td>
</tr>
<tr class="odd">
<td>Level</td>
<td><strong>QName</strong></td>
<td>Die Ebene der Ausführlichkeit, die beim Schreiben des Ereignisses verwendet werden soll. Geben Sie den Namen einer Ebene an, die Sie im Manifest definiert haben, oder eine der Ebenen, die in der \Include\Winmeta.xml-Datei definiert sind, die im Windows SDK enthalten ist. Ausführliche Informationen zum Definieren einer Ebene finden Sie unter dem komplexen <a href="eventmanifestschema-leveltype-complextype.md"><strong>leveltype</strong></a> -Typ.<br/> Wenn Sie keine Ebene angeben, enthält der Ereignis Deskriptor eine 0 (null) für die Ebene.<br/> Sie müssen eine Ebene angeben, wenn der Kanaltyp, auf den das Ereignis geschrieben ist, admin ist. die Ebene muss eine der folgenden Ebenen sein, die in Winmeata.xml definiert sind:
<ul>
<li>win:Critical</li>
<li>win:Error</li>
<li>win:Warning</li>
<li>win:Informational</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>message</td>
<td><a href="eventmanifestschema-strtableref-simpletype.md"><strong>"Strauch"</strong></a></td>
<td>Die lokalisierte Meldung für das Ereignis. Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> -Abschnitt des Manifests.<br/> Sie müssen eine Meldung angeben, wenn der Kanaltyp, für den das Ereignis geschrieben ist, admin ist.<br/></td>
</tr>
<tr class="odd">
<td>nicht protokolliert</td>
<td>boolean</td>
<td>Bestimmt, ob der Anbieter dieses Ereignis protokolliert. Geben Sie true an, wenn der Anbieter dieses Ereignis protokolliert. andernfalls false. Verwenden Sie dieses Attribut, um anzugeben, dass der Anbieter dieses Ereignis nicht mehr protokolliert, anstatt das Ereignis aus dem Manifest zu entfernen. Durch die Beibehaltung des Ereignisses im Manifest können Consumer ältere ETL-Dateien decodieren, die das Ereignis enthalten.<br/> <strong>Windows Server 2008 und Windows Vista:</strong> Dieses Attribut wird in Versionen des Nachrichten Compilers, die vor der Windows 7-Version des Windows SDK ausgeliefert wurden, nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td>OpCode</td>
<td><strong>QName</strong></td>
<td>Der Name eines Opcodes, der einen Vorgang innerhalb der Aufgabe identifiziert. Geben Sie den Namen eines Opcodes an, den Sie im Manifest definiert haben, oder einen der OpCodes, die in Winmeta.xml definiert sind. Ausführliche Informationen zum Definieren eines Opcodes finden Sie unter der komplexe <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpCodeType</strong></a> -Typ.<br/> Wenn der Task, auf den Sie verweisen, aufgabenspezifische (lokale) Opcodes enthält, können Sie einen der aufgabenspezifischen Opcodes oder einen Opcode angeben, der auf der Anbieter Ebene (globaler OpCode) definiert ist. Wenn Sie einen globalen Opcode angeben, darf der Wert des globalen Opcodes nicht mit einem der lokalen Opcodes für die Aufgabe identisch sein.<br/> Wenn Sie auf einen lokalen Opcode verweisen, muss das Task-Attribut auf die Aufgabe verweisen, zu der der lokale Opcode gehört.<br/> Wenn Sie keinen Opcode angeben, enthält der Ereignis Deskriptor für Opcode eine NULL.<br/></td>
</tr>
<tr class="odd">
<td>Symbol</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>Csymboltype</strong></a></td>
<td>Das Symbol, mit dem auf den Ereignis Deskriptor für dieses Ereignis in der Anwendung verwiesen werden soll. Der <a href="message-compiler--mc-exe-.md"><strong>Nachrichten Compiler (MC.exe)</strong></a> verwendet das Symbol, um eine Konstante für den Ereignis Deskriptor in der vom Compiler generierten Header Datei zu erstellen. Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie. Sie verwenden den Deskriptor, wenn Sie die <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> -Funktion zum Schreiben des Ereignisses aufruft.<br/></td>
</tr>
<tr class="even">
<td>task</td>
<td><strong>QName</strong></td>
<td>Der Name eines Tasks, der die Komponente oder Unterkomponente identifiziert, die dieses Ereignis generiert. Geben Sie den Namen einer Aufgabe an, die Sie im Manifest definiert haben. Ausführliche Informationen zum Definieren einer Aufgabe finden Sie unter <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> Complex Type.<br/> Wenn Sie keine Aufgabe angeben, enthält der Ereignis Deskriptor eine NULL für den Task.<br/></td>
</tr>
<tr class="odd">
<td>Vorlage</td>
<td>token</td>
<td>Der Vorlagen Bezeichner der Vorlage, mit der die Datenelemente definiert werden, die in diesem Ereignis enthalten sind. Geben Sie den Bezeichner einer Vorlage an, die Sie im Manifest definiert haben. Ausführliche Informationen zum Definieren einer Vorlage finden Sie unter der komplexe Typ " <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>templateitemtype</strong></a> ".<br/></td>
</tr>
<tr class="even">
<td>value</td>
<td><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></td>
<td>Der Ereignisbezeichner. Der Bezeichner muss innerhalb der Liste von Ereignissen, die Sie definieren, eindeutig sein.<br/></td>
</tr>
<tr class="odd">
<td>version</td>
<td>unsignedByte</td>
<td>Eine 1-Byte-Versionsnummer der Ereignis Definition.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Wenn Sie [**evtformatmessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) verwenden, um die Meldungs Zeichenfolge für das Ereignis zu formatieren (oder die Ereignisanzeige zum Anzeigen der Meldungs Zeichenfolge verwenden), kann die Meldungs Zeichenfolge Einfügungs Zeichenfolgen und alle Format Zeichenfolgen enthalten, die die Win32 **FormatMessage** Die Einfügezeichenfolgen sind auf%*n* oder%*n*! s! beschränkt. (z. b. %1), wobei *n* der einbasierte Verweis auf die Datenelemente ist, die in der-Vorlage des Ereignisses definiert sind. Die Meldungs Zeichenfolge kann auch Parameter Einfügungs Zeichenfolgen im Format%%*n* (z. b .% %4) enthalten. Die maximale Anzahl von Einfügezeichenfolgen, die die Nachricht enthalten kann, ist 100.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

