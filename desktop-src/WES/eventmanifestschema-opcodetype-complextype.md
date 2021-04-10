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
# <a name="opcodetype-complex-type"></a>Komplexer OpCodeType-Typ

Definiert einen Vorgang innerhalb einer Komponente der Anwendung. Wird in Verbindung mit einer-Aufgabe verwendet, um den Abschnitt der Anwendung zu identifizieren, der das Ereignis protokolliert.

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

## <a name="attributes"></a>Attributes



| Name     | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message  | [**"Strauch"**](eventmanifestschema-strtableref-simpletype.md) | Der lokalisierte Anzeige Name für den Opcode. Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests. <br/>                                                                                                     |
| MUF-Wert | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Nur für die interne Verwendung vorgesehen.<br/>                                                                                                                                                                                                                                                                           |
| name     | **QName**                                                         | Der Name des OpCodes. Dieser Name muss innerhalb des Gültigkeits Bereichs dieses Anbieters eindeutig sein. <br/>                                                                                                                                                                                                                      |
| Symbol   | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das für den Verweis auf den Opcode in der Anwendung verwendet werden soll. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Opcode in der vom Compiler generierten Header Datei zu erstellen. Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.<br/> |
| value    | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Der opcodewert. Sie können Werte im Bereich 10 und 239 angeben. Eine Liste der vordefinierten opcodewerte finden Sie unter "Hinweise".<br/>                                                                                                                                                                                    |



## <a name="remarks"></a>Bemerkungen

Im folgenden sind die vordefinierten Opcode-Werte enthalten, die Sie verwenden können. Diese Werte werden in der Winmeta.xml-Datei definiert, die in der Windows SDK enthalten ist.



| Name          | Wert | Symbol                      | BESCHREIBUNG                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| Win: info      | 0     | WinEvent- \_ Opcode- \_ Informationen      | Ein Informationsereignis.                                                                                |
| Win: Start     | 1     | WinEvent- \_ Opcode \_ starten     | Ein Ereignis, das das Starten einer Aktivität darstellt.                                                         |
| Win: beendet      | 2     | WinEvent \_ Opcode wird \_ beendet.      | Ein Ereignis, das das Beenden einer Aktivität darstellt. Das Ereignis entspricht dem letzten nicht paarweise zugeordneten Start Ereignis. |
| Win: DC- \_ Start | 3     | WinEvent- \_ Opcode- \_ DC- \_ Start | Ein Ereignis, das das Starten der Datensammlung darstellt. Dabei handelt es sich um Rundown-Ereignis Typen.                      |
| Win: DC- \_ Beendigung  | 4     | WinEvent- \_ Opcode-DC-Vorgang \_ \_ beendet  | Ein Ereignis, das das Beenden der Datensammlung darstellt. Dabei handelt es sich um Rundown-Ereignis Typen.                      |
| Win: Erweiterung | 5     | WinEvent- \_ Opcode- \_ Erweiterung | Ein Erweiterungsereignis.                                                                                    |
| Win: Reply     | 6     | WinEvent- \_ Opcode- \_ Antwort     | Ein Antwort Ereignis.                                                                                         |
| Win: Resume    | 7     | Wiederaufnahme von WinEvent- \_ Opcode \_    | Ein Ereignis, das eine Aktivität darstellt, die nach dem aussetzen fortgesetzt wird.                                   |
| Win: Suspend   | 8     | WinEvent \_ Opcode \_ Suspend   | Ein Ereignis, das die angehaltene Aktivität darstellt, die den Abschluss einer anderen Aktivität aussteht.           |
| Win: Send      | 9     | WinEvent \_ Opcode \_ Send      | Ein Ereignis, das die Übertragung von Aktivitäten an eine andere Komponente darstellt.                                   |
| Win: empfangen   | 240   | WinEvent- \_ Opcode \_ empfangen   | Ein Ereignis, das den Empfang einer Aktivitäts Übertragung von einer anderen Komponente darstellt.                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





