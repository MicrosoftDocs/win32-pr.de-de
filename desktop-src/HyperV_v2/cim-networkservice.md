---
description: Diese Klasse ist veraltet. Stattdessen wird die Ableitung von der CIM- \_ Dienstklasse empfohlen.
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
ms.openlocfilehash: b141e6e38f2fafefdf6e75670b975e0fcdd2961c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352513"
---
# <a name="cim_networkservice-class"></a>CIM- \_ NetworkService-Klasse

Diese Klasse ist veraltet. Stattdessen wird die Ableitung von der [**CIM- \_ Dienst**](cim-service.md) Klasse empfohlen.

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

Die **CIM- \_ NetworkService** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ NetworkService** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Schlüsselwörter**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert")
</dt> </dl>

Diese Eigenschaft ist veraltet und sollte nicht verwendet werden.

> [!Note]  
> Veraltete Beschreibung: ein Array von Schlüsselwörtern, die in Abfragen verwendet werden können.

 

</dd> <dt>

**ServiceUrl**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ serviceaccessuri")
</dt> </dl>

Diese Eigenschaft ist veraltet. Stattdessen wird die **CIM \_ serviceaccessuri** -Klasse empfohlen.

> [!Note]  
> Veraltete Beschreibung: eine URL, die das Protokoll, den Netzwerk Speicherort und andere Dienst spezifische Informationen bereitstellt, die erforderlich sind, um auf den Dienst zuzugreifen.

 

</dd> <dt>

**Startupconditions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert")
</dt> </dl>

Diese Eigenschaft ist veraltet und sollte nicht verwendet werden.

> [!Note]  
> Veraltete Beschreibung: die Voraussetzungen, die erfüllt sein müssen, damit dieser Dienst ordnungsgemäß gestartet wird.

 

</dd> <dt>

**StartupParameters**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("kein Wert")
</dt> </dl>

Diese Eigenschaft ist veraltet und sollte nicht verwendet werden.

> [!Note]  
> Deprecated Description: die Parameter, die für die **Start Service** -Methode bereitgestellt werden müssen, damit dieser Dienst ordnungsgemäß gestartet wird.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Dienst**](cim-service.md)
</dt> </dl>

 

