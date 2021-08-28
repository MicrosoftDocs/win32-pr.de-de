---
title: Komplexer EventDefinitionType-Typ
description: Definiert ein Ereignis, das Ihr Anbieter schreiben kann.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- 'EventDefinitionType : Komplexer Typ EventLog'
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42959edd4c7f7f49c3ced305b5b9bd1072f721a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482986"
---
# <a name="eventdefinitiontype-complex-type"></a>Komplexer EventDefinitionType-Typ

Definiert ein Ereignis, das Ihr Anbieter schreiben kann.

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




| Name | type | BESCHREIBUNG | 
|------|------|-------------|
| Kanal | token | Ein Bezeichner, der den Kanal identifiziert, in den das Ereignis geschrieben wird. Geben Sie einen Kanalbezeichner für einen der Kanäle an, die Sie definiert oder importiert haben. Wenn der Kanal keinen Kanalbezeichner angibt, verwenden Sie den Namen des Kanals. Ausführliche Informationen zum Definieren oder Importieren eines Kanals finden Sie im komplexen <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType-Typ.</strong></a><br /> Wenn Sie keinen Kanal angeben, wird das Ereignis nicht in einen Kanal geschrieben. In der Regel ist der einzige Grund, keinen Kanal anzugeben, wenn Sie Ereignisse nur in eine ETW-Sitzung schreiben. Weitere Informationen finden Sie unter Erstellen einer ETW-Sitzung unter <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Steuern von Ereignisablaufverfolgungssitzungen.</a><br /> | 
| keywords | <a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a> | Eine durch Leerzeichen getrennte Liste von Schlüsselwortnamen, die die Kategorie der Ereignisse identifizieren, zu denen dieses Ereignis gehört. Geben Sie einen Schlüsselwortnamen aus der Liste der von Ihnen definierten Schlüsselwörter an. Ausführliche Informationen zum Definieren von Schlüsselwörtern finden Sie im komplexen <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType-Typ.</strong></a><br /> Wenn Sie keine Schlüsselwörter angeben, enthält der Ereignisdeskriptor 0 (null) für Schlüsselwörter.<br /> | 
| Level | <strong>QName</strong> | Der Ausführlichkeitsgrad, der beim Schreiben des Ereignisses verwendet werden soll. Geben Sie den Namen einer Ebene an, die Sie im Manifest definiert haben, oder eine der Ebenen, die in der \Include\Winmeta.xml-Datei definiert sind, die im Windows SDK enthalten ist. Ausführliche Informationen zum Definieren einer Ebene finden Sie unter Komplexer <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType-Typ.</strong></a><br /> Wenn Sie keine Ebene angeben, enthält der Ereignisdeskriptor eine Null für level.<br /> Sie müssen eine Ebene angeben, wenn der Kanaltyp, in den das Ereignis geschrieben wird, Admin ist. die Ebene muss eine der folgenden Ebenen sein, die in Winmeata.xml definiert sind:<ul><li>win:Critical</li><li>win:Error</li><li>win:Warning</li><li>win:Informational</li></ul><br /> | 
| message | <a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a> | Die lokalisierte Nachricht für das Ereignis. Die Meldungszeichenfolge verweist auf eine lokalisierte Zeichenfolge im <a href="eventmanifestschema-stringtable-resources-element.md"><strong>StringTable-Abschnitt</strong></a> des Manifests.<br /> Sie müssen eine Meldung angeben, wenn der Kanaltyp, in den das Ereignis geschrieben wird, Admin ist.<br /> | 
| nicht protokolliert | boolean | Bestimmt, ob der Anbieter dieses Ereignis protokolliert. Geben Sie true an, wenn der Anbieter dieses Ereignis protokolliert. andernfalls FALSE. Verwenden Sie dieses Attribut, um anzugeben, dass der Anbieter dieses Ereignis nicht mehr protokolliert, anstatt das Ereignis aus dem Manifest zu entfernen. Wenn das Ereignis im Manifest beibehalten wird, können Consumer ältere etl-Dateien decodieren, die das Ereignis enthalten.<br /><strong>Windows Server 2008 und Windows Vista:</strong> Dieses Attribut wird nicht in Versionen des Nachrichtencompiler unterstützt, die vor Windows 7 Version des Windows SDK ausgeliefert wurden.<br /> | 
| Opcode | <strong>QName</strong> | Der Name eines Opcodes, der einen Vorgang innerhalb der Aufgabe identifiziert. Geben Sie den Namen eines Opcodes an, den Sie im Manifest definiert haben, oder einen der in Winmeta.xml definierten Opcodes. Ausführliche Informationen zum Definieren eines Opcodes finden Sie unter Dem komplexen <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType-Typ.</strong></a><br /> Wenn die Aufgabe, auf die Sie verweisen, taskspezifische (lokale) Opcodes enthält, können Sie einen der aufgabenspezifischen Opcodes oder einen opcode angeben, der auf Anbieterebene definiert ist (ein globaler Opcode). Wenn Sie einen globalen Opcode angeben, kann der Wert des globalen Opcodes nicht mit einem der lokalen Opcodes für den Task identisch sein.<br /> Wenn Sie auf einen lokalen Opcode verweisen, muss das Aufgabenattribut auf die Aufgabe verweisen, zu der der lokale Opcode gehört.<br /> Wenn Sie keinen Opcode angeben, enthält der Ereignisdeskriptor eine Null für opcode.<br /> | 
| Symbol | <a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a> | Das Symbol, das verwendet werden soll, um auf den Ereignisdeskriptor für dieses Ereignis in Ihrer Anwendung zu verweisen. Der <a href="message-compiler--mc-exe-.md"><strong>Nachrichtencompiler (MC.exe)</strong></a> verwendet das Symbol, um eine Konstante für den Ereignisdeskriptor in der Headerdatei zu erstellen, die der Compiler generiert. Wenn Sie kein Symbol angeben, generiert der Compiler ein Symbol für Sie. Sie verwenden den Deskriptor, wenn Sie die <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite-Funktion</strong></a> aufrufen, um das Ereignis zu schreiben.<br /> | 
| task | <strong>QName</strong> | Der Name einer Aufgabe, die die Komponente oder Unterkomponente identifiziert, die dieses Ereignis generiert. Geben Sie den Namen einer Aufgabe an, die Sie im Manifest definiert haben. Ausführliche Informationen zum Definieren einer Aufgabe finden Sie unter Komplexer <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType-Typ.</strong></a><br /> Wenn Sie keine Aufgabe angeben, enthält der Ereignisdeskriptor eine 0 (null) für die Aufgabe.<br /> | 
| Vorlage | token | Der Vorlagenbezeichner der Vorlage, die die Datenelemente definiert, die dieses Ereignis enthält. Geben Sie den Bezeichner einer Vorlage an, die Sie im Manifest definiert haben. Ausführliche Informationen zum Definieren einer Vorlage finden Sie unter Dem komplexen <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType-Typ.</strong></a><br /> | 
| Wert | <a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a> | Der Ereignisbezeichner. Der Bezeichner muss innerhalb der Liste der von Ihnen definierten Ereignisse eindeutig sein.<br /> | 
| version | unsignedByte | Eine 1-Byte-Versionsnummer der Ereignisdefinition.<br /> | 




## <a name="remarks"></a>Hinweise

Wenn Sie [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) verwenden, um die Nachrichtenzeichenfolge für das Ereignis zu formatieren (oder die Ereignisanzeige zum Anzeigen der Meldungszeichenfolge verwenden), kann die Nachrichtenzeichenfolge Einfügezeichenfolgen und beliebige Formatzeichenfolgen enthalten, die von der Win32 **FormatMessage-Funktion** unterstützt werden. Die Einfügezeichenfolgen sind auf %*n* oder %*n*!s! beschränkt. (z.B. %1), wobei *n* der 1-basierte Verweis auf die in der Vorlage des Ereignisses definierten Datenelemente ist. Die Meldungszeichenfolge kann auch Parametereinfügungszeichenfolgen im Format %%*n* (z.B. %%4) enthalten. Die maximale Anzahl von Einfügezeichenfolgen, die die Nachricht enthalten kann, beträgt 100.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

