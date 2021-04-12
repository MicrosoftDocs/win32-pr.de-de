---
title: Komplexer QueryType-Typ
description: Definiert einen Satz von Auswahl-und Unterdrückungs Abfragen, die verwendet werden, um Ereignisse in das Resultset einzuschließen oder Ereignisse aus dem Resultset auszuschließen.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- QueryType Complex-Typ EventLog
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50c0779b90a6f2e74a873b13d79c6e2083afd0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103575"
---
# <a name="querytype-complex-type"></a>Komplexer QueryType-Typ

Definiert einen Satz von Auswahl-und Unterdrückungs Abfragen, die verwendet werden, um Ereignisse in das Resultset einzuschließen oder Ereignisse aus dem Resultset auszuschließen.

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                    | type | BESCHREIBUNG                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Select**](queryschema-select-querytype-element.md)     |      | Eine XPath-Abfrage, die die Ereignisse identifiziert, die im Resultset der Abfrage enthalten sein sollen. Geben Sie den XPath im Textkörper dieses Elements an. Der XPath ist auf 32-Ausdrücke beschränkt.<br/>   |
| [**Suppress**](queryschema-suppress-querytype-element.md) |      | Eine XPath-Abfrage, die die aus dem Abfrageresultset auszuschließenden Ereignisse identifiziert. Geben Sie den XPath im Textkörper dieses Elements an. Der XPath ist auf 32-Ausdrücke beschränkt.<br/> |



## <a name="attributes"></a>Attributes



| Name | type   | BESCHREIBUNG                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id   | long   | Ein Bezeichner, der diese Abfrage in der Liste der Abfragen eindeutig identifiziert. Der Bezeichner ist NULL basiert. Sie müssen einen Bezeichner angeben, wenn die Abfrage Liste mehr als eine Abfrage enthält.<br/> |
| Pfad | anyURI | Der Name des Kanals oder der Pfad zu der Protokolldatei, in der die Ereignisse enthalten sind.<br/>                                                                                                            |
| Pfad | anyURI | Der Name des Kanals oder der Pfad zu der Protokolldatei, in der die Ereignisse enthalten sind.<br/>                                                                                                            |
| Pfad | anyURI | Nicht verwendet.<br/>                                                                                                                                                                                |



## <a name="remarks"></a>Bemerkungen

Die Abfrage muss mindestens eine SELECT-Anweisung enthalten. Für jede unterdrückte Anweisung muss mindestens eine SELECT-Anweisung vorhanden sein, die denselben Pfad angibt. Wenn die SELECT-und Unterdrückung-Abfrage dieselben Ereignisse zurückgibt, hat die Unterdrückung-Anweisung Vorrang. Wenn Sie Ereignisse aus mehreren Quellen auswählen, werden die Ereignisse in der Reihenfolge der Zeitstempel zurückgegeben. Wenn Sie den Systemzeitstempel verwenden und die Rate der Ereignisse hoch ist, kann es vorkommen, dass mehr als ein Ereignis denselben Zeitstempel hat. Wenn dies auftritt, wird die Reihenfolge von Ereignissen mehrdeutig, und die Ereignisse werden möglicherweise nicht in der richtigen Reihenfolge angezeigt.

Wenn Sie einen Pfad für eine der Abfragen in der Abfrage Liste angeben, muss für alle Abfragen ein Pfad angegeben werden. Wenn Sie keinen Pfad für alle Abfragen angeben, müssen Sie den Pfad angeben, wenn Sie die [**evtquery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) -oder [**evtsubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





