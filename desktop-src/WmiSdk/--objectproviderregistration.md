---
description: Fungiert als übergeordnete Klasse für Klassen, die zum Registrieren von Klassen-und instanzanbietern in WMI verwendet werden.
ms.assetid: f7c569be-8927-42a4-b96a-abe4b7e3e23c
ms.tgt_platform: multiple
title: __ObjectProviderRegistration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderRegistration
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
ms.openlocfilehash: a60b24278fb235cec38c127e7ebbbb481e49a140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345899"
---
# <a name="__objectproviderregistration-class"></a>\_\_Objectproviderregistration-Klasse

Die abstrakte System Klasse **\_ \_ objectproviderregistration** fungiert als übergeordnete Klasse für Klassen, die zum Registrieren von Klassen-und instanzanbietern in WMI verwendet werden.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __ObjectProviderRegistration : __ProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a>Member

Die **\_ \_ objectproviderregistration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ objectproviderregistration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Interaktionstyp**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt an, ob der Klassen-oder Instanzanbieter seine eigenen Daten bereitstellt, oder stützt sich auf WMI und das Common Information Model (CIM)-Repository. Pull-Anbieter unterstützen den dynamischen Zugriff auf Ihre Daten, und pushanbieter speichern Ihre Daten im CIM-Repository und basieren auf WMI, um Zugriff darauf zu ermöglichen. Weitere Informationen finden Sie unter [bestimmen des Push-oder Pull-Status](determining-push-or-pull-status.md). Der Standardwert ist 0 (null).

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

Der Anbieter ist ein Push-Verify-Anbieter. Beachten Sie, dass Push-Verify zurzeit nicht unterstützt wird.

</dd> </dl>

</dd> <dt>

**ab**
</dt> <dd> <dl> <dt>

Datentyp: **\_ \_ Anbieter**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf eine Instanz des [**\_ \_ Anbieters**](--provider.md) , die einen Objekt Pfad zum Objekt Anbieter darstellt. Diese Eigenschaft wird von [**\_ \_ providerregistration**](--providerregistration.md)geerbt.

</dd> <dt>

**Querysupportlevels**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Array der Typen der Anbieter bezogenen Unterstützung für die Abfrage Verarbeitung. Klassen Anbieter unterstützen keine Typen von Abfragen. Instanzanbieter können **querysupportlevels** auf **null** festlegen, wenn Sie die Abfrage Verarbeitung nicht unterstützen. Anbieter, die Abfragen unterstützen, implementieren die [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) -Methode, und legen Sie diese Eigenschaft auf einen oder mehrere der folgenden Werte fest (der Eigenschaftentyp ist ein Array).

"WQL: unaryselect"

"WQL: Verweise"

"WQL: assoziatoren"

"WQL: V1ProviderDefined"

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

Der Anbieter unterstützt das Löschen von Klassen oder Instanzen durch Implementieren eines der beiden folgenden [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (Klassen Anbieter) oder [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (Instanzanbieter).

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

Richtig
</dt> <dd>

Der Anbieter unterstützt die datenenumeration durch Implementieren eines der beiden Typen [**IWbemServices:: | ateclassenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (Klassen Anbieter) oder [**IWbemServices:: feateinstanceenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (Instanzanbieter).

</dd> <dt>

False
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

Richtig
</dt> <dd>

Der Anbieter unterstützt die Änderung von Klassen oder Instanzen durch Implementieren eines der beiden [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (Klassen Anbieter) oder [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (Klassen Anbieter).

</dd> <dt>

False
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

Die **\_ \_ objectproviderregistration** -Klasse wird von [**\_ \_ providerregistration**](--providerregistration.md)abgeleitet.

Klassen Anbieter müssen die **supportsenumeration** -Eigenschaft auf **true** festlegen, da die Anbieter in der Lage sein müssen, WMI mit einer Liste Ihrer Klassen bereitzustellen. Wenn ein Klassen Anbieter versucht, diese Eigenschaft auf **false** festzulegen, wird die Registrierung von WMI als unzulässig gekennzeichnet. Instanzanbieter müssen die Enumeration nicht unterstützen, und Sie können festlegen, dass **supportsenumeration** auf " **true** " oder " **false**" festgelegt wird.

Ein Anbieter, der **querysupportlevels** auf "WQL: unaryselect" festlegt, kann eine Abfrage akzeptieren, die aus der grundlegenden SELECT-Anweisung besteht, wie in WMI-Version 1,0 unterstützt. Es wird erwartet, dass sowohl Klassen-als auch Instanzanbieter die **\_ \_ Klassen** System Eigenschaft verarbeiten können. Klassen Anbieter werden außerdem erwartet, dass die System Eigenschaft " **\_ \_ Superclass** " und der ISA-Operator verarbeitet werden. Der ISA-Operator wird verwendet, um ein Resultset auf abgeleitete Klassen zu erweitern. Wenn ein Anbieter eine Abfrage erhält, die er nicht interpretieren kann, fordert er an, dass WMI ihn verarbeitet, indem er den Fehlerwert **WBEM \_ E \_ zu \_ Komplex** zurückgibt. Eine Beschreibung der gültigen WQL-Syntax finden Sie unter [Querying with WQL (Abfragen mit WQL](querying-with-wql.md)).

Ein Anbieter, der **querysupportlevels** auf **WQL: V1ProviderDefined** festlegt, kann versuchen, eine größere Menge der SQL-Syntax zu unterstützen, z. b `ORDER BY` . die-Klausel. WMI interpretiert die zusätzlichen Klauseln nicht, oder es wird versucht, sicherzustellen, dass das Resultset korrekt ist.

Nur Administratoren können einen Anbieter registrieren oder löschen, indem Sie eine Instanz von [**\_ \_ Win32Provider**](--win32provider.md) erstellen und registrieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Providerregistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[Registrieren eines Anbieters](registering-a-provider.md)
</dt> </dl>

 

