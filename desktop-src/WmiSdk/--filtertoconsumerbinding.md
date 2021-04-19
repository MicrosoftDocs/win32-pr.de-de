---
description: Wird bei der Registrierung von permanenten Ereignisconsumern verwendet, um eine Instanz von \_ \_ eventconsumer mit einer Instanz von \_ \_ EventFilter zu verknüpfen.
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: __FilterToConsumerBinding-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0fd9b7f3cf60d14d27fdf5b5014b57e6f599d67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355366"
---
# <a name="__filtertoconsumerbinding-class"></a>\_\_Filtertoconsumerbinding-Klasse

Die System Klasse **\_ \_ filtertoconsumerbinding** wird bei der Registrierung von permanenten Ereignisconsumer verwendet, um eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) mit einer Instanz von [**\_ \_ EventFilter**](--eventfilter.md)zu verknüpfen.**\_ \_ "Filtertoconsumerbinding** " ist eine Association-Klasse.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a>Member

Die **\_ \_ filtertoconsumerbinding** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ filtertoconsumerbinding** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Consumer**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ eventconsumer**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Verweis auf eine Instanz von [**\_ \_ eventconsumer**](--eventconsumer.md) , die den Objekt Pfad zu einem logischen Consumer, den Empfänger eines Ereignisses, darstellt. Ein logischer Consumer ist eine Instanz einer Klasse, die von **\_ \_ eventconsumer** abgeleitet ist.

</dd> <dt>

**"Kreatorsid"**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Sicherheits-ID (SID), die den Benutzer eindeutig identifiziert, der die Bindung erstellt hat. Abhängig vom Betriebssystem speichert WMI die Administrator-SID oder die SID des Benutzers, der eine Instanz von " **\_ \_ filtertoconsumerbinding**" erstellt. Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md) und über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.

</dd> <dt>

**Deliversynchron**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Veraltet. Verwenden Sie stattdessen die Eigenschaft **deliveryqos** anstelle dieser Eigenschaft, denn wenn **deliversynchron** auf **true** festgelegt ist, überschreibt es die Einstellung der **deliveryqos** -Eigenschaft.

</dd> <dt>

**Deliveryqos**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Quality of Service für ein Abonnement. Wenn die **deliversynchron** -Eigenschaft auf **true** festgelegt ist, überschreibt Sie die-Einstellung der **deliveryqos** -Eigenschaft.

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**Wmimsg \_ \_QoS \_ synchron markieren** (0)


</dt> <dd>

Synchrone Übermittlung

**False**. Das Ereignis wird synchron an den logischen Consumer übermittelt.

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**Wmimsg \_ Flag \_ QoS \_ Express** (1)


</dt> <dd>

Express-Übermittlung

**True**. Das Ereignis wird asynchron an den logischen Consumer übermittelt.

</dd> </dl>

</dd> <dt>

**Filter**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ EventFilter**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Verweis auf eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md) , die den Objekt Pfad zu einem Ereignis Filter darstellt, bei dem es sich um eine Abfrage handelt, die den Ereignistyp angibt, der empfangen werden soll.

</dd> <dt>

**Wart SecurityContext**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass die Ereignisse im gleichen Sicherheitskontext übermittelt werden, in dem sich der Anbieter bei der Bereitstellung befunden hat.

> [!Note]  
> Nur ein Consumer, der als DLL (ein Prozess interner Consumer) implementiert ist, kann Ereignisse im Sicherheitskontext des Anbieters empfangen. Weitere Informationen zu Prozess internen Anbietern und zur Sicherheit finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md). Weitere Informationen und Beispiele finden Sie unter ersetzen:[sicheres empfangen von Ereignissen](receiving-events-securely.md).

 

</dd> <dt>

**Slowdownproviders**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass die Anbieter verlangsamt werden, wenn dieser Consumer nicht in der Einrichtung bleiben kann.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ filtertoconsumerbinding** -Klasse wird von " [**\_ \_ indicationrelated**](--indicationrelated.md)" abgeleitet, die keine Eigenschaften hat.

Permanente Ereignisconsumer verwenden die **\_ \_ filtertoconsumerbinding** -System Klasse, um Ereignis Filter an endgültige Consumer zu binden. Nachdem der Filter und der Consumer zusammengebunden wurden, kann WMI Ereignisse, die mit dem Filter übereinstimmen, an den entsprechenden Consumer weiterleiten.

## <a name="examples"></a>Beispiele

Das PowerShell-Beispiel zur [Erstellung dauerhafter WMI-Ereignis Registrierung zum Überwachen von Dateien](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) in der TechNet Gallery verwendet **\_ \_ filtertoconsumerbinding** als Teil eines komplexen Skripts, um eine permanente WMI-Ereignis Registrierung einzurichten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Indicationrelated**](--indicationrelated.md)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[Überwachen von und reagieren auf Ereignisse mit Standard Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Überwachen von Ereignissen](monitoring-events.md)
</dt> <dt>

[Erstellen eines Ereignis Filters](creating-an-event-filter.md)
</dt> <dt>

[Sichern von WMI-Ereignissen](securing-wmi-events.md)
</dt> </dl>

 

 




