---
description: Registriert Instanzanbieter in WMI.
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: __InstanceProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
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
ms.openlocfilehash: 45923c0c3ea3bfc28e67634e3b447e46b62765f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347706"
---
# <a name="__instanceproviderregistration-class"></a>\_\_Instanceproviderregistration-Klasse

Die **\_ \_ instanceproviderregistration** -System Klasse registriert Instanzanbieter in WMI.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>Member

Die **\_ \_ instanceproviderregistration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ instanceproviderregistration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Interaktionstyp**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, dass ein Klassen-oder Instanzanbieter Daten bereitstellt, oder ruft Daten aus WMI und dem Common Information Model (CIM)-Repository ab. Pull-Anbieter unterstützen den dynamischen Zugriff auf Ihre Daten. und pushanbieter speichern Ihre Daten im CIM-Repository und verwenden WMI, um den Zugriff darauf zu ermöglichen. Weitere Informationen finden Sie unter [bestimmen des Push-oder Pull-Status](determining-push-or-pull-status.md). Der Standardwert ist 0 (null).

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

Der Anbieter ist ein Push-Verify-Anbieter. Beachten Sie, dass Push-Verify-Anbieter derzeit nicht unterstützt werden.

</dd> </dl>

</dd> <dt>

**ab**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Anbieter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine Instanz des [**\_ \_ Anbieters**](--provider.md) , die den Objekt Pfad zum Instanzanbieter darstellt. Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.

</dd> <dt>

**Querysupportlevels**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Array der Typen der Anbieter bezogenen Unterstützung für die Abfrage Verarbeitung. Klassen Anbieter unterstützen nicht alle Abfrage Typen. Instanzanbieter können **querysupportlevels** auf **null** festlegen, wenn Sie die Abfrage Verarbeitung nicht unterstützen. Anbieter, die Abfragen unterstützen, implementieren die [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) -Methode, und legen Sie diese Eigenschaft auf einen oder mehrere der folgenden Werte fest.

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

**Supportsbatching**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Nicht verwendet.

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Anbieter das Löschen von Daten unterstützt.

<dt>

Richtig
</dt> <dd>

Der Anbieter unterstützt das Löschen von Klassen oder Instanzen durch Implementieren von [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (Klassen Anbieter) oder [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (Instanzanbieter).

</dd> <dt>

False
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

**True** gibt an, dass der Anbieter datenenumeration unterstützt.

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

**True** gibt an, dass der Klassen-oder Instanzanbieter den Datenabruf unterstützt.

<dt>

Richtig
</dt> <dd>

Der Anbieter unterstützt den Datenabruf durch Implementieren von [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

</dd> <dt>

False
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

**True** gibt an, dass der Klassen-oder Instanzanbieter die Datenänderung unterstützt.

<dt>



 Fall


</dt> <dd>

Der Anbieter unterstützt die Änderung von Klassen oder Instanzen durch Implementieren einer der folgenden Methoden: [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (Klassen Anbieter) oder [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (Klassen Anbieter).

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

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ instanceproviderregistration** -Klasse wird von [**\_ \_ objectproviderregistration**](--objectproviderregistration.md)abgeleitet, das von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet ist. Nur Administratoren können einen Instanzanbieter registrieren, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und **\_ \_ instanceproviderregistration** erstellen. Nur Administratoren können einen Anbieter löschen.

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
</dt> </dl>

 

