---
description: Das-Benachrichtigungstyp-Makro enthält die folgenden Elemente.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: Notification-Type-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2ff7695d7ca36eeaf01115d47df496d52d68ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356835"
---
# <a name="notification-type-macro"></a>Notification-Type-Makro

Das-Benachrichtigungstyp-Makro enthält die folgenden Elemente.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

## <a name="components"></a>Komponenten

<dl> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Objekt Deskriptor
</dt> <dd>

Fügt einen Namen an ein SNMP-Ereignis in einem Notification-Type-Makro an. In der folgenden Liste werden die Regeln für die Zuordnung des Objekt Deskriptors aufgeführt.



| type                        | Concatenate                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gekapselt CIM-Klassenname | "SNMP \_ "<br/> Name der MIB-Modul Identität<br/> Unterstrich ( \_ )<br/> Objekt Deskriptor<br/> " \_ Benachrichtigung"<br/> Beispiel: die **vtpserverdeaktiviert** -Benachrichtigung von **Cisco-VTP-MIB** wird der **SNMP- \_ Cisco \_ VTP \_ MIB \_ vtpserverdeaktiviert- \_ Benachrichtigung** zugeordnet.<br/>                 |
| Name der Referenten-CIM-Klasse     | "SNMP \_ "<br/> Name der MIB-Modul Identität<br/> Unterstrich ( \_ )<br/> Objekt Deskriptor<br/> " \_ Extendednotification"<br/> Beispiel: die **vtpserverdeaktiviert** -Benachrichtigung von **Cisco-VTP-MIB** wird **SNMP \_ Cisco \_ VTP \_ MIB \_ vtpserverdeaktiviert \_ extendednotification** zugeordnet.<br/> |



 

</dd> <dt>

<span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>Objects-Klausel
</dt> <dd>

Listet die Objekte auf, die dem Benachrichtigungs Objekt zugeordnet sind.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Reference-Klausel
</dt> <dd>

Verweist auf ein anderes Dokument, das weitere Informationen zum-Objekt enthält. Sie wird dem klassenqualifizierungsverweis der CIM-Klasse zugeordnet, der vom Typ Zeichenfolge ist. 

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Description-Klausel
</dt> <dd>

Beschreibt das betreffende Objekt. Es wird der klassenqualifiziererbeschreibung der CIM-Klasse zugeordnet, die vom Typ Zeichenfolge 

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Status-Klausel
</dt> <dd>

Gibt an, ob das Objekt unterstützt werden muss. Wenn der Status entweder **veraltet** oder **veraltet** ist, wird die Benachrichtigung von der Zuordnung verworfen. Andernfalls wird diese Klausel dem gatewayklassenqualifiziererstatus zugeordnet, der vom Typ " **String**" ist. 

Der bevorzugte **Wert für SNMPv1 ist entweder** **obligatorisch** oder **optional**, aber der Qualifizierer kann einen anderen Wert enthalten. Der bevorzugte **Wert für SNMPv2C ist entweder** **Current** oder **veraltet**, aber der Qualifizierer kann einen anderen Wert enthalten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der SNMP-Anbieter ordnet das **-Benachrichtigungstyp** Makro entweder einer gekapselten oder einer Referenz Klassendefinition zu.

Eine gekapselte Klassendefinition macht die dem MIB-Objekt zugeordneten Instanzinformationen nicht verfügbar. Stattdessen codiert die Klassendefinition die Objects-Klausel als eine Reihe von Eigenschaften der CIM-Ereignisklasse. Jede CIM-Eigenschaft gibt den Namen, den Typ und den Wert des entsprechenden MIB-Objekts in der Objects-Klausel wieder. Wenn Sie Instanzinformationen benötigen, müssen Sie eine Referenzklasse zuordnen. Eine gekapselte Klassendefinition wird der [SnmpNotification](snmpnotification.md) -Klasse zugeordnet.

Eine Referenten Klasse definiert ein MIB-Objekt und die Instanzinformationen, die zum Abrufen des Objekts verwendet werden. Die Klassendefinition codiert die Objects-Klausel als eine Reihe von Eigenschaften der CIM-Ereignisklasse. Jede CIM-Eigenschaft gibt den Namen des entsprechenden MIB-Objekts in der Objects-Klausel und den Typ als eingebettetes Objekt wieder, das eine Instanz der diesem MIB-Objekt zugeordneten Klasse wieder gibt. Der Anbieter generiert dann eine Klasse, die mit dem MIB-Objekt verknüpft ist. **Ifindex** wird z. b. einer eingebetteten Klasse mit dem Namen **SNMP \_ RFC1213 \_ MIB \_ ifindex** zugeordnet. Weitere Informationen zu diesem Klassentyp finden Sie unter [Object-Type-Makro](object-type-macro.md).

 

 




