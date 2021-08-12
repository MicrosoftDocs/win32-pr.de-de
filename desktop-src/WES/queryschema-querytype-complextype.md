---
title: Komplexer QueryType-Typ
description: Definiert einen Satz von Selektor- und Suppressorabfragen, die verwendet werden, um Ereignisse in das Resultset einzuschließen oder aus dem Resultset auszuschließen.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- Komplexer QueryType-Typ EventLog
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6585b43e1e9e48bc0be69001d471c74e52506177250d66316273ca447b38084a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587625"
---
# <a name="querytype-complex-type"></a>Komplexer QueryType-Typ

Definiert einen Satz von Selektor- und Suppressorabfragen, die verwendet werden, um Ereignisse in das Resultset einzuschließen oder aus dem Resultset auszuschließen.

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



| Element                                                    | Typ | BESCHREIBUNG                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Select**](queryschema-select-querytype-element.md)     |      | Eine XPath-Abfrage, die die Ereignisse identifiziert, die in das Abfrageresultset aufgenommen werden sollen. Geben Sie den XPath im Texttext dieses Elements an. XPath ist auf 32 Ausdrücke beschränkt.<br/>   |
| [**Suppress**](queryschema-suppress-querytype-element.md) |      | Eine XPath-Abfrage, die die Ereignisse identifiziert, die aus dem Abfrageresultset ausgeschlossen werden sollen. Geben Sie den XPath im Texttext dieses Elements an. XPath ist auf 32 Ausdrücke beschränkt.<br/> |



## <a name="attributes"></a>Attributes



| Name | Typ   | BESCHREIBUNG                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id   | long   | Ein Bezeichner, der diese Abfrage in der Liste der Abfragen eindeutig identifiziert. Der Bezeichner ist nullbasiert. Sie müssen einen Bezeichner angeben, wenn die Abfrageliste mehr als eine Abfrage enthält.<br/> |
| Pfad | anyURI | Der Name des Kanals oder der Pfad zur Protokolldatei, die die Ereignisse enthält.<br/>                                                                                                            |
| Pfad | anyURI | Der Name des Kanals oder der Pfad zur Protokolldatei, die die Ereignisse enthält.<br/>                                                                                                            |
| Pfad | anyURI | Wird nicht verwendet.<br/>                                                                                                                                                                                |



## <a name="remarks"></a>Bemerkungen

Die Abfrage muss mindestens eine SELECT-Anweisung enthalten. Für jede suppress-Anweisung muss mindestens eine select-Anweisung vorhanden sein, die denselben Pfad angibt. Wenn die Abfrage select and suppress die gleichen Ereignisse zurückgibt, hat die suppress-Anweisung Vorrang. Wenn Sie Ereignisse aus mehreren Quellen auswählen, werden die Ereignisse in Zeitstempelreihenfolge zurückgegeben. Wenn Sie den Systemzeitstempel verwenden und die Rate der Ereignisse hoch ist, ist es möglich, dass mehrere Ereignisse denselben Zeitstempel aufweisen. In diesem Fall wird die Reihenfolge der Ereignisse mehrdeutig, und die Ereignisse werden möglicherweise nicht mehr in der reihenfolgengeordneten Reihenfolge angezeigt.

Wenn Sie einen Pfad für eine der Abfragen in der Liste der Abfragen angeben, müssen alle Abfragen einen Pfad angeben. Wenn Sie keinen Pfad für alle Abfragen angeben, müssen Sie den Pfad beim Aufrufen der [**EvtQuery-**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) oder [**EvtSubscribe-Funktion**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) angeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





