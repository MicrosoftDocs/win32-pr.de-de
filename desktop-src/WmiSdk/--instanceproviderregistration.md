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
ms.openlocfilehash: 773bb54ec4d132e629f21513ffa617cbe3435d35941e7c98c55810d267f614c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821155"
---
# <a name="__instanceproviderregistration-class"></a>\_\_InstanceProviderRegistration-Klasse

Die **\_ \_ Systemklasse InstanceProviderRegistration** registriert Instanzanbieter in WMI.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ InstanceProviderRegistration-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ InstanceProviderRegistration-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**InteractionType**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, dass eine Klasse oder ein Instanzanbieter Daten angibt oder Daten aus WMI und dem cim-Repository (Common Information Model) abruft. Pullanbieter unterstützen den dynamischen Zugriff auf ihre Daten. und Pushanbieter speichern ihre Daten im CIM-Repository und verwenden WMI, um Zugriff darauf zu gewähren. Weitere Informationen finden Sie unter [Bestimmen des Push- oder Pullstatus.](determining-push-or-pull-status.md) Der Standardwert ist 0 (null).

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)


</dt> <dd>

Der Anbieter ist ein Pullanbieter.

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)


</dt> <dd>

Der Anbieter ist ein Pushanbieter.

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)


</dt> <dd>

Der Anbieter ist ein Push-Verify-Anbieter. Beachten Sie, dass Push-Verify-Anbieter derzeit nicht unterstützt werden.

</dd> </dl>

</dd> <dt>

**Anbieter**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Anbieter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine Instanz des [**\_ \_ Anbieters,**](--provider.md) die den Objektpfad zum Instanzanbieter darstellt. Diese Eigenschaft wird von [**\_ \_ ProviderRegistration**](--providerregistration.md)geerbt.

</dd> <dt>

**QuerySupportLevels**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Array der Typen der vom Anbieter enthaltenen Unterstützung für die Abfrageverarbeitung. Klassenanbieter unterstützen nicht alle Arten von Abfragen. Instanzanbieter können **QuerySupportLevels** auf **NULL** festlegen, wenn sie die Abfrageverarbeitung nicht unterstützen. Anbieter, die Abfragen unterstützen, implementieren die [**IWbemServices::ExecQueryAsync-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) und legen diese Eigenschaft auf einen oder mehrere der folgenden Werte fest.

<dt>



 ("WQL:UnarySelect")


</dt> <dd></dd> <dt>



 ("WQL:References")


</dt> <dd></dd> <dt>



 ("WQL:Associators")


</dt> <dd></dd> <dt>



 ("WQL:V1ProviderDefined")


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportsBatching**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

</dd> <dt>

**SupportsDelete**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Anbieter das Löschen von Daten unterstützt.

<dt>

True
</dt> <dd>

Der Anbieter unterstützt das Löschen von Klassen oder Instanzen, indem er entweder [**IWbemServices::D eleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (Klassenanbieter) oder [**IWbemServices::D eleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (Instanzanbieter) implementiert.

</dd> <dt>

False
</dt> <dd>

Der Anbieter unterstützt das Löschen von Daten nicht und gibt **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** aus [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) oder [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)zurück.

</dd> </dl>

</dd> <dt>

**SupportsEnumeration**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass der Anbieter die Datenenumeration unterstützt.

<dt>



 (True)


</dt> <dd>

Der Anbieter unterstützt die Datenenumeration, indem er entweder [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (Klassenanbieter) oder [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (Instanzanbieter) implementiert.

</dd> <dt>



 (False)


</dt> <dd>

Der Anbieter unterstützt keine Datenenumeration und gibt **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** aus [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) oder [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)zurück.

</dd> </dl>

</dd> <dt>

**SupportsGet**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass die Klasse oder der Instanzanbieter den Datenabruf unterstützt.

<dt>

True
</dt> <dd>

Der Anbieter unterstützt den Datenabruf, indem [**er IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)implementiert.

</dd> <dt>

False
</dt> <dd>

Der Anbieter unterstützt keinen Datenabruf und gibt **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** aus [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)zurück.

</dd> </dl>

</dd> <dt>

**SupportsPut**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

**True** gibt an, dass die Klasse oder der Instanzanbieter Datenänderungen unterstützt.

<dt>



 (True)


</dt> <dd>

Der Anbieter unterstützt die Klassen- oder Instanzänderung durch Implementierung einer der folgenden Methoden: [**IWbemServices::P utClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (Klassenanbieter) oder [**IWbemServices::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (Klassenanbieter).

</dd> <dt>



 (False)


</dt> <dd>

Der Anbieter unterstützt keine Datenänderung und gibt **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** aus [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) oder [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)zurück.

</dd> </dl>

</dd> <dt>

**SupportsTransactions**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ InstanceProviderRegistration-Klasse** wird von [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md)abgeleitet, die von [**\_ \_ ProviderRegistration**](--providerregistration.md)abgeleitet wird. Nur Administratoren können einen Instanzanbieter registrieren, indem sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) und **\_ \_ InstanceProviderRegistration** erstellen. Nur Administratoren können einen Anbieter löschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_ObjectProviderRegistration**](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[Registrieren eines Klassenanbieters](registering-a-class-provider.md)
</dt> <dt>

[Registrieren eines Instanzanbieters](registering-an-instance-provider.md)
</dt> </dl>

 

