---
description: Definiert ein Attribut eines Zählers, der angibt, wie die gegen Daten in einer Consumeranwendung angezeigt werden.
ms.assetid: 3749501b-4f3e-42e5-b1d5-2700b6d4a48a
title: komplexer counterAttribute-Typ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1b34a3a802f0f7c79815956c3a364522ce0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359043"
---
# <a name="counterattribute-complex-type"></a>komplexer counterAttribute-Typ

Definiert ein Attribut eines Zählers, der angibt, wie die gegen Daten in einer Consumeranwendung angezeigt werden.

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



| Name | type | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name |      | Der Name des anzuwendenden Anzeige Attributs. Sie können einen der folgenden Namen angeben:<br/> <dl> <dt><span id="reference"></span><span id="REFERENCE"></span>Referenz</dt> <dd> Rufen Sie den Wert des Zählers als Verweis und nicht als Wert ab.<br/> </dd> <dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>nodisplay</dt> <dd> Zeigen Sie den Wert des Leistungs Zählers nicht an. In der Regel verwenden Sie dieses Attribut, wenn die Daten des Zählers als Eingabe zum Berechnen des Werts eines anderen Zählers verwendet werden. <br/> </dd> <dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>nodigit-Gruppierung</dt> <dd> Consumer-oder Überwachungsanwendungen sollten keine Ziffern Trennzeichen verwenden, wenn Sie Zählerwerte anzeigen. <br/> </dd> <dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>Display AshEx</dt> <dd> Consumer-oder Überwachungsanwendungen sollten den Wert des Zählers als Hexadezimalwert anstelle der standardmäßigen Ganzzahl anzeigen.<br/> </dd> <dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayasreal</dt> <dd> Consumer-oder Überwachungsanwendungen sollten den Wert des Zählers als reelle Zahl anstelle der standardmäßigen Ganzzahl anzeigen. <br/> </dd> </dl> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




