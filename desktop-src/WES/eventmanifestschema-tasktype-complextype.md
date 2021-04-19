---
title: Komplexer TaskType-Typ
description: Definiert eine Komponente oder eine Unterkomponente einer Anwendung. | Komplexer TaskType-Typ
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- TaskType komplexer Typ EventLog
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106353693"
---
# <a name="tasktype-complex-type"></a>Komplexer TaskType-Typ

Definiert eine Komponente oder eine Unterkomponente einer Anwendung.

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
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
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                         | type                                                                     | BESCHREIBUNG                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**OpCodes**](eventmanifestschema-opcodes-tasktype-element.md) | [**Opcodelisttype**](eventmanifestschema-opcodelisttype-complextype.md) | Definiert eine Liste von aufgabenspezifischen OpCodes. Die in Winmeta.xml definierten opcodewerte können nicht für aufgabenspezifische Opcodes verwendet werden.<br/> |



## <a name="attributes"></a>Attributes



| Name      | type                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| eventguid | [**Guidtype**](eventmanifestschema-guidtype-simpletype.md)       | Eine Globally Unique Identifier im Registrierungs Format, die die Aufgabe identifiziert. Dieses Attribut ist erforderlich, wenn Sie das-MOF-Nachrichten Compiler-Argument verwenden, um eine MOF-Klasse für die Unterstützung von downlevels zu generieren.<br/>                                                                                                   |
| message   | [**"Strauch"**](eventmanifestschema-strtableref-simpletype.md) | Der lokalisierte Anzeige Name für die Aufgabe. Die Meldungs Zeichenfolge verweist auf eine lokalisierte Zeichenfolge im [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) -Abschnitt des Manifests. <br/>                                                                                                   |
| name      | **QName**                                                         | Der Name der Aufgabe.<br/>                                                                                                                                                                                                                                                                                 |
| Symbol    | [**Csymboltype**](eventmanifestschema-csymboltype-simpletype.md) | Das Symbol, das verwendet werden soll, um auf die Aufgabe in Ihrer Anwendung zu verweisen. Der [**Nachrichten Compiler (MC.exe)**](message-compiler--mc-exe-.md) verwendet das Symbol, um eine Konstante für den Task in der vom Compiler generierten Header Datei zu erstellen. Wenn Sie kein Symbol angeben, generiert der Compiler einen für Sie.<br/> |
| value     | [**UInt16Type**](eventmanifestschema-hexint16type-simpletype.md) | Ein numerischer Wert, der diese Aufgabe innerhalb der Liste der vom Anbieter definierten Aufgaben eindeutig identifiziert. Der Wert muss zwischen 1 und 239 liegen.<br/>                                                                                                                                             |



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie eine Aufgabe angegeben wird.


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





