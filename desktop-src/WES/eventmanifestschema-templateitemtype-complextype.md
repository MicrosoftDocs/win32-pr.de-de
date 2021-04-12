---
title: Komplexer templateitemtype-Typ
description: Eine Vorlage, die die Daten definiert, die in einem Ereignis enthalten sein sollen. | Komplexer templateitemtype-Typ
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- "\"Templateitemtype Complex Type Event Log\""
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94ae108ceed3285fe7e57461611d94b1147d94e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219270"
---
# <a name="templateitemtype-complex-type"></a>Komplexer templateitemtype-Typ

Eine Vorlage, die die Daten definiert, die in einem Ereignis enthalten sein sollen.

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                   | type                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ärer**](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | Nur für die interne Verwendung vorgesehen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Vorrats**](eventmanifestschema-data-templateitemtype-element.md)         | [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md)     | Definiert ein Datenelement, das Sie mit dem-Ereignis einschließen möchten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**struct**](eventmanifestschema-struct-templateitemtype-element.md)     | [**StructDefinitionType**](eventmanifestschema-structdefinitiontype-complextype.md) | Definiert eine-Struktur, die ein oder mehrere Datenelemente enthält, die Sie mit dem-Ereignis einschließen möchten. Anbieter schreiben die Struktur als BLOB und nicht als einzelne Member der Struktur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) | [**XmlType**](eventmanifestschema-xmltype-complextype.md)                           | Ein XML-Fragment, das zum Rendering der Ereignisdaten verwendet wird. Wenn Sie das Fragment nicht einschließen, werden die Ereignisdaten in der Reihenfolge gerendert, in der die Datenelemente in der Vorlage definiert sind. Der Inhalt dieses Elements ist ein beliebiges gültiges XML-Fragment. Das Fragment darf nur einen Knoten der obersten Ebene enthalten, und der Knoten der obersten Ebene muss einen eigenen Namespace angeben. <br/> Wenn Sie auf ein Datenelement im Fragment verweisen möchten, legen Sie den Textkörper für einen Knoten im Fragment auf%*n* fest, wobei *n* der einbasierte Index der Datenelemente der obersten Ebene in der Liste der Datenelemente ist (Sie können nicht auf Member einer Struktur verweisen). Der Indexwert, den Sie angeben, darf nicht größer sein als die Anzahl der Datenelemente der obersten Ebene in der Vorlage.<br/> Dieses Element folgt allen **Daten** -und **Struktur** Elementen. <br/> |



## <a name="attributes"></a>Attributes



| Name | type   | BESCHREIBUNG                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name | Zeichenfolge | Nur für die interne Verwendung vorgesehen.<br/>                                                                                                                                                            |
| name | Zeichenfolge | Der Name der Vorlage.<br/>                                                                                                                                                                  |
| tid  | token  | Ein Bezeichner, der die Vorlage eindeutig in der Liste der Vorlagen identifiziert, die der Anbieter definiert. Verwenden Sie diesen Namen, um auf die Vorlage zu verweisen, wenn Sie die Ereignis Definition definieren.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Vorlagen Definition muss mindestens ein untergeordnetes Daten-oder Strukturelement aufweisen. Der Anbieter muss die Ereignisdaten in der Reihenfolge der Datenelemente schreiben, die in der Vorlage definiert sind.

Die Größe aller Datenelemente in der Vorlage muss kleiner als 64 KB sein.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie eine Vorlagen Definition erstellt wird.


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





