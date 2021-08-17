---
description: Das NOTIFICATION-TYPE-Makro enthält die folgenden Elemente.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: NOTIFICATION-TYPE-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e50146d6a6fc71cc78baccd97a7dffc9e4ed4e7091373dd52ae42b2fbc6b66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992740"
---
# <a name="notification-type-macro"></a>NOTIFICATION-TYPE-Makro

Das NOTIFICATION-TYPE-Makro enthält die folgenden Elemente.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

## <a name="components"></a>Komponenten

<dl> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Objektdeskriptor
</dt> <dd>

Fügt einen Namen an ein SNMP-Ereignis in einem NOTIFICATION-TYPE-Makro an. In der folgenden Liste sind die Regeln zum Zuordnen des Objektdeskriptors aufgeführt.



| type                        | Concatenate                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gekapselter CIM-Klassenname | "SNMP" \_<br/> Identitätsname des MIB-Moduls<br/> Unterstrich ( \_ )<br/> Objektdeskriptor<br/> \_"Benachrichtigung"<br/> Beispiel: Die **vtpServerDisabled-Benachrichtigung** von **CISCO-VTP-MIB** wird **SNMP \_ CISCO \_ VTP \_ MIB \_ vtpServerDisabled \_ Notification** zugeordnet.<br/>                 |
| Referenz-CIM-Klassenname     | "SNMP" \_<br/> Identitätsname des MIB-Moduls<br/> Unterstrich ( \_ )<br/> Objektdeskriptor<br/> \_"ExtendedNotification"<br/> Beispiel: Die **vtpServerDisabled-Benachrichtigung** von **CISCO-VTP-MIB** wird **SNMP \_ CISCO \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification** zugeordnet.<br/> |



 

</dd> <dt>

<span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>OBJECTS-Klausel
</dt> <dd>

Listet den Satz von -Objekten auf, die dem Benachrichtigungsobjekt zugeordnet sind.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE-Klausel
</dt> <dd>

Bezieht sich auf ein anderes Dokument, das weitere Informationen zum -Objekt enthält. Sie wird dem CIM-Klassenqualifizierer **Reference** zugeordnet, der vom Typ String ist.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION-Klausel
</dt> <dd>

Beschreibt das betreffende Objekt. Sie wird dem CIM-Klassenqualifizierer **Description** zugeordnet, der vom Typ "String" ist.

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS-Klausel
</dt> <dd>

Gibt an, ob das -Objekt unterstützt werden muss. Wenn der Status entweder **veraltet** oder **veraltet** ist, wird die Benachrichtigung aus der Zuordnung verworfen. Andernfalls wird diese Klausel dem CIM-Klassenqualifizierer **Status** zugeordnet, der vom Typ **Zeichenfolge** ist.

Für SNMPv1 ist der bevorzugte Wert von **Status** entweder **obligatorisch** oder **optional,** aber der Qualifizierer kann einen anderen Wert enthalten. Für SNMPv2C ist der bevorzugte Wert von **Status** entweder **aktuell** oder **veraltet,** aber der Qualifizierer kann einen anderen Wert enthalten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der SNMP-Anbieter ordnet das **NOTIFICATION-TYPE-Makro** einer gekapselten oder referenziellen Klassendefinition zu.

Eine gekapselte Klassendefinition macht die dem MIB-Objekt zugeordneten Instanzinformationen nicht verfügbar. Stattdessen codiert die Klassendefinition die OBJECTS-Klausel als eine Reihe von Eigenschaften der CIM-Ereignisklasse. Jede CIM-Eigenschaft gibt den Namen, den Typ und den Wert des entsprechenden MIB-Objekts in der OBJECTS-Klausel wieder. Wenn Sie Instanzinformationen benötigen, müssen Sie einer Referenzklasse zuordnen. Eine gekapselte Klassendefinition wird der [SnmpNotification-Klasse](snmpnotification.md) zugeordnet.

Eine referenzielle Klasse definiert ein MIB-Objekt und die Instanzinformationen, die zum Abrufen des Objekts verwendet werden. Die Klassendefinition codiert die OBJECTS-Klausel als eine Reihe von Eigenschaften der CIM-Ereignisklasse. Jede CIM-Eigenschaft spiegelt den Namen des entsprechenden MIB-Objekts in der OBJECTS-Klausel und den Typ als eingebettetes Objekt wider, das eine Instanz der Klasse wiedergibt, die diesem MIB-Objekt zugeordnet ist. Der Anbieter generiert dann eine Klasse, die dem MIB-Objekt zugeordnet ist. IfIndex  wird beispielsweise einer eingebetteten Klasse namens **SNMP \_ RFC1213 \_ MIB \_ ifIndex** zugeordnet. Weitere Informationen zu diesem Typ von Klasse finden Sie unter [OBJECT-TYPE Macro](object-type-macro.md).

 

 




