---
description: Registriert Klassen Anbieter in WMI.
ms.assetid: 1af7d9ed-c5e4-47e4-839d-53d579ef7cea
ms.tgt_platform: multiple
title: __ClassProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
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
ms.openlocfilehash: 32442122624035ec376bed3be8b3ef20c80f8524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760459"
---
# <a name="__classproviderregistration-class"></a>\_\_Classproviderregistration-Klasse

Die **\_ \_ classproviderregistration** -System Klasse registriert Klassen Anbieter in WMI.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __ClassProviderRegistration : __ObjectProviderRegistration
{
  boolean        SupportsBatching;
  datetime       CacheRefreshInterval;
  sint32         InteractionType = 0;
  __Provider REF provider;
  boolean        PerUserSchema;
  string         QuerySupportLevels[];
  string         ReferencedSetQueries[];
  string         ResultSetQueries[];
  boolean        ReSynchroniseOnNamespaceOpen;
  boolean        SuppportsBatching;
  boolean        SupportsEnumeration = False;
  boolean        SupportsDelete = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
  string         UnsupportedQueries[];
  uint32         Version;
};
```

## <a name="members"></a>Member

Die **\_ \_ classproviderregistration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ classproviderregistration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**CacheRefreshInterval**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Interaktionstyp**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der Klassen-oder Instanzanbieter Daten bereitstellt, oder ob er sich auf WMI und das Common Information Model (CIM)-Repository stützt. Pull-Anbieter unterstützen den dynamischen Zugriff auf Daten, und pushanbieter speichern Daten im CIM-Repository und basieren auf WMI, um Zugriff darauf zu ermöglichen. Der Standardwert ist 0 (null). Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt. Weitere Informationen finden Sie unter [bestimmen des Push-oder Pull-Status](determining-push-or-pull-status.md).

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)


</dt> <dd>

Der Anbieter ist ein Pull-Anbieter.

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)


</dt> <dd>

Der Anbieter ist ein Push-Anbieter.

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**Pushverify** (2)


</dt> <dd>

Der Anbieter ist ein Push-Verify-Anbieter. Beachten Sie, dass **pushverify** -Anbieter zurzeit nicht unterstützt werden.

</dd> </dl>

</dd> <dt>

**Peruserschema**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**ab**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Anbieter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Objekt Pfad zu einem Klassen Anbieter. Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.

</dd> <dt>

**Querysupportlevels**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Array der Typen der Anbieter bezogenen Unterstützung für die Abfrage Verarbeitung. Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt. Klassen Anbieter sind erforderlich, um mindestens einen Abfragetyp zu unterstützen. Instanzanbieter können **querysupportlevels** auf **null** festlegen, wenn Sie die Abfrage Verarbeitung nicht unterstützen. Anbieter, die Abfragen unterstützen, implementieren die [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) -Methode, und legen Sie diese Eigenschaft auf einen oder mehrere der folgenden Werte fest:

<dt>



 ("WQL: unaryselect")


</dt> <dd></dd> <dt>



 ("WQL: Verweise")


</dt> <dd></dd> <dt>



 ("WQL: assoziatoren")


</dt> <dd></dd> <dt>



 ("WQL: V1ProviderDefined")


</dt> <dd></dd> </dl>

</dd> <dt>

**Referencedsetqueries**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Eine oder mehrere Abfragen, die den Satz der referenzierten Klassen beschreiben, die von einem Klassen Anbieter unterstützt werden. Anbieter, die Zuordnungs Klassen bereitstellen können, müssen mindestens eine Abfrage in diese Eigenschaft einschließen.

</dd> <dt>

**Resultsetqueries**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Eine oder mehrere Abfragen, die den Satz aller Klassen beschreiben, die vom Klassen Anbieter bereitgestellt werden können, oder eine übergeordnete Gruppe dieser Klassen. Diese Eigenschaft gibt nie eine Teilmenge der unterstützten Klassen an.

</dd> <dt>

**Resynchronisierung-namespaceopen**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Supportsbatching**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt.

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Anbieter das Löschen von Daten unterstützt. Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt.

<dt>



 Fall


</dt> <dd>

Der Anbieter unterstützt das Löschen von Klassen oder Instanzen durch Implementieren eines der beiden folgenden [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (Klassen Anbieter) oder [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (Instanzanbieter).

</dd> <dt>



 Alarm


</dt> <dd>

Der Anbieter unterstützt keine Daten Löschung und gibt den **WBEM E-Anbieter zurück, der \_ \_ \_ nicht \_** von [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) oder [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)unterstützt werden kann.

</dd> </dl>

</dd> <dt>

**Supportsenumeration**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Anbieter datenenumeration unterstützt. Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt.

<dt>



 Fall


</dt> <dd>

Der Anbieter unterstützt die datenenumeration durch Implementieren eines der beiden Typen [**IWbemServices:: | ateclassenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (Klassen Anbieter) oder [**IWbemServices:: feateinstanceenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (Instanzanbieter).

</dd> <dt>



 Alarm


</dt> <dd>

Der Anbieter unterstützt keine datenenumeration und gibt [](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)den **WBEM \_ E- \_ Anbieter \_ \_** zurück, [**der**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) nicht in der Lage ist, von "" aus "", "", "", "", "", ""

</dd> </dl>

</dd> <dt>

**Supportsget**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Klassen-oder Instanzanbieter den Datenabruf unterstützt. Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt.

<dt>



 Fall


</dt> <dd>

Der Anbieter unterstützt den Datenabruf durch Implementieren von [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>



 Alarm


</dt> <dd>

Der Anbieter unterstützt nicht das Abrufen von Daten und gibt den **WBEM E-Anbieter zurück, der \_ \_ \_ nicht \_** von [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)unterstützt werden kann.

</dd> </dl>

</dd> <dt>

**Supportsput**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Klassen-oder Instanzanbieter die Datenänderung unterstützt. Diese Eigenschaft wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)geerbt.

<dt>



 Fall


</dt> <dd>

Der Anbieter unterstützt die Änderung von Klassen oder Instanzen durch Implementieren eines der beiden [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (Klassen Anbieter) oder [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (Klassen Anbieter).

</dd> <dt>



 Alarm


</dt> <dd>

Der Anbieter unterstützt keine Datenänderungen und gibt den **WBEM E-Anbieter zurück, der \_ nicht \_ \_ \_** von [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) oder [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)unterstützt werden kann.

</dd> </dl>

</dd> <dt>

**SupportsTransactions**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Suppportsbatching**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**Nicht supportedqueries**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Eine oder mehrere Abfragen, die den Satz von Klassen beschreiben, den der Klassen Anbieter nicht unterstützt. Verwenden Sie diese Eigenschaft, um den von **resultsetqueries** impliziten Satz von Klassen zu subtrahieren.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Version dieses Klassen Anbieters.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ classproviderregistration** -Klasse wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)abgeleitet, das von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet ist.

Die von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md) geerbten Eigenschaften geben an, ob der Klassen Anbieter Datenabruf, Änderung, Löschung, Enumeration und Abfrage Verarbeitung unterstützt. Die **interaktiontype** -Eigenschaft gibt an, ob der Klassen Anbieter als Pull-oder pushanbieter konzipiert ist. Weitere Informationen finden Sie unter [bestimmen des Push-oder Pull-Status](determining-push-or-pull-status.md).

Die [**\_ \_ providerregistration**](--providerregistration.md) -Klasse definiert die [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) -Eigenschaft. Nur Administratoren können einen Anbieter registrieren, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und **\_ \_ classproviderregistration** erstellen. Nur Administratoren können einen Anbieter löschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Objectproviderregistration**](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[Registrieren eines Klassen Anbieters](registering-a-class-provider.md)
</dt> <dt>

[Registrieren eines Instanzanbieters](registering-an-instance-provider.md)
</dt> <dt>

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 

