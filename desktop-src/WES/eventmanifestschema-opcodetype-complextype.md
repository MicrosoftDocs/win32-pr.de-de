---
title: Komplexer OpcodeType-Typ
description: Definiert einen Vorgang innerhalb einer Komponente der Anwendung.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- Komplexer OpcodeType-Typ EventLog
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b18fa8a7591a54877251e10448842c3cd9d2394099028bf3a2cb680aee979bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136213"
---
# <a name="opcodetype-complex-type"></a>Komplexer OpcodeType-Typ

Definiert einen Vorgang innerhalb einer Komponente der Anwendung. Wird in Verbindung mit einem Task verwendet, um den Abschnitt der Anwendung zu identifizieren, die das Ereignis protokolliert.

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



| Name     | type                                                              | Beschreibung                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message  | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Der lokalisierte Anzeigename für den Opcode. Die Meldungszeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**StringTable-Abschnitt**](eventmanifestschema-stringtable-resources-element.md) des Manifests. <br/>                                                                                                     |
| mofValue | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Nur für die interne Verwendung vorgesehen.<br/>                                                                                                                                                                                                                                                                           |
| name     | **QName**                                                         | Der Name des Opcodes. Dieser Name muss innerhalb des Bereichs dieses Anbieters eindeutig sein. <br/>                                                                                                                                                                                                                      |
| Symbol   | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf den Opcode in Ihrer Anwendung zu verweisen. Der [**Nachrichtencompiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Opcode in der Headerdatei zu erstellen, die der Compiler generiert. Wenn Sie kein Symbol angeben, generiert der Compiler ein Symbol für Sie.<br/> |
| value    | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Der Opcodewert. Sie können Werte im Bereich von 10 und 239 angeben. Eine Liste vordefinierter Opcodewerte finden Sie unter Hinweise.<br/>                                                                                                                                                                                    |



## <a name="remarks"></a>Hinweise

Im Folgenden sind die vordefinierten Opcodewerte angegeben, die Sie verwenden können. Diese Werte werden in der Winmeta.xml-Datei definiert, die im Windows SDK enthalten ist.



| Name          | Wert | Symbol                      | BESCHREIBUNG                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| win:Info      | 0     | WINEVENT \_ OPCODE \_ INFO      | Ein Informationsereignis.                                                                                |
| win:Start     | 1     | WINEVENT \_ OPCODE \_ START     | Ein Ereignis, das das Starten einer Aktivität darstellt.                                                         |
| win:Stop      | 2     | WINEVENT \_ OPCODE \_ STOP      | Ein Ereignis, das das Beenden einer Aktivität darstellt. Das Ereignis entspricht dem letzten nicht bezahlten Startereignis. |
| win:DC \_ Start | 3     | WINEVENT \_ OPCODE \_ DC \_ START | Ein Ereignis, das das Starten der Datensammlung darstellt. Dies sind Rundownereignistypen.                      |
| win:DC \_ Stop  | 4     | WINEVENT \_ OPCODE \_ DC \_ STOP  | Ein Ereignis, das das Beenden der Datensammlung darstellt. Dies sind Rundownereignistypen.                      |
| win:Extension | 5     | WINEVENT \_ \_ OPCODE-ERWEITERUNG | Ein Erweiterungsereignis.                                                                                    |
| win:Reply     | 6     | WINEVENT \_ OPCODE \_ REPLY     | Ein Antwortereignis.                                                                                         |
| win:Resume    | 7     | WINEVENT \_ OPCODE \_ RESUME    | Ein Ereignis, das eine Aktivität darstellt, die nach dem Anhalten wieder aufgenommen wird.                                   |
| win:Suspend   | 8     | WINEVENT \_ OPCODE \_ SUSPEND   | Ein Ereignis, das die angehaltene Aktivität darstellt, bis der Abschluss einer anderen Aktivität aussteht.           |
| win:Send      | 9     | WINEVENT \_ OPCODE \_ SEND      | Ein Ereignis, das die Übertragung von Aktivitäten an eine andere Komponente darstellt.                                   |
| win:Receive   | 240   | WINEVENT \_ OPCODE \_ RECEIVE   | Ein Ereignis, das den Empfang einer Aktivitätsübertragung von einer anderen Komponente darstellt.                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





