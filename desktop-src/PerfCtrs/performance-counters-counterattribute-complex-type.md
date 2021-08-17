---
description: Definiert ein Attribut eines Zählers, das angibt, wie die Indikatordaten in einer Consumeranwendung angezeigt werden.
ms.assetid: 3749501b-4f3e-42e5-b1d5-2700b6d4a48a
title: counterAttribute Complex Type
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 333024a9681f58c3db7c271ceaf4c14c6d06aef68817ea4ca8ee211fa261e79e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793734"
---
# <a name="counterattribute-complex-type"></a>counterAttribute Complex Type

Definiert ein Attribut eines Zählers, das angibt, wie die Indikatordaten in einer Consumeranwendung angezeigt werden.

``` syntax
<xs:complexType name="counterAttribute">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                use="required"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="xs:string"
                    >
                        <xs:enumeration
                            value="reference"
                         />
                        <xs:enumeration
                            value="noDisplay"
                         />
                        <xs:enumeration
                            value="noDigitGrouping"
                         />
                        <xs:enumeration
                            value="displayAsHex"
                         />
                        <xs:enumeration
                            value="displayAsReal"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributes



| Name | type | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name |      | Der Name des anzuwendenden Anzeigeattributs. Sie können einen der folgenden Namen angeben:<br/> <dl> <dt><span id="reference"></span><span id="REFERENCE"></span>Verweis</dt> <dd> Rufen Sie den Wert des Zählers nach Verweis und nicht nach Wert ab.<br/> </dd> <dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>noDisplay</dt> <dd> Zeigen Sie den Indikatorwert nicht an. In der Regel verwenden Sie dieses Attribut, wenn die Daten des Indikators als Eingabe zum Berechnen des Werts eines anderen Indikators verwendet werden. <br/> </dd> <dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt> <dd> Consumer- oder Überwachungsanwendungen sollten beim Anzeigen von Indikatorwerten keine Zifferntrennzeichen verwenden. <br/> </dd> <dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt> <dd> Consumer- oder Überwachungsanwendungen sollten den Indikatorwert als Hexadezimalwert anstelle des ganzzahligen Standardwerts anzeigen.<br/> </dd> <dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt> <dd> Consumer- oder Überwachungsanwendungen sollten den Indikatorwert als echte Zahl anstelle des ganzzahligen Standardwerts anzeigen. <br/> </dd> </dl> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




