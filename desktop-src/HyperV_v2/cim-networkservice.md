---
description: Diese Klasse ist veraltet. Stattdessen wird empfohlen, von der CIM-Dienstklasse \_ zu ableiten.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: CIM_NetworkService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cfb2ea7b122516cc3b62f675684649e22577171f713856638f97985d9713e8d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694690"
---
# <a name="cim_networkservice-class"></a>CIM \_ NetworkService-Klasse

Diese Klasse ist veraltet. Stattdessen wird empfohlen, von der [**CIM-Dienstklasse \_ zu**](cim-service.md) ableiten.

## <a name="syntax"></a>Syntax

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a>Member

Die **CIM \_ NetworkService-Klasse** verfügt über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ NetworkService-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Schlüsselwörter**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Kein Wert")
</dt> </dl>

Diese Eigenschaft ist veraltet und sollte nicht verwendet werden.

> [!Note]  
> Veraltete Beschreibung: Ein Array von Schlüsselwörtern, die in Abfragen verwendet werden können.

 

</dd> <dt>

**ServiceURL**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ ServiceAccessURI")
</dt> </dl>

Diese Eigenschaft ist veraltet. Stattdessen wird die **CIM \_ ServiceAccessURI-Klasse** empfohlen.

> [!Note]  
> Veraltete Beschreibung: Eine URL, die das Protokoll, den Netzwerkspeicherort und andere dienstspezifische Informationen enthält, die für den Zugriff auf den Dienst erforderlich sind.

 

</dd> <dt>

**StartupConditions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Kein Wert")
</dt> </dl>

Diese Eigenschaft ist veraltet und sollte nicht verwendet werden.

> [!Note]  
> Veraltete Beschreibung: Die Voraussetzungen, die erfüllt sein müssen, damit dieser Dienst ordnungsgemäß gestartet werden kann.

 

</dd> <dt>

**StartupParameters**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Kein Wert")
</dt> </dl>

Diese Eigenschaft ist veraltet und sollte nicht verwendet werden.

> [!Note]  
> Veraltete Beschreibung: Die Parameter, die für die **StartService-Methode** angegeben werden müssen, damit dieser Dienst ordnungsgemäß gestartet werden kann.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Dienst**](cim-service.md)
</dt> </dl>

 

