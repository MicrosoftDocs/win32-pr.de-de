---
description: Stellt Informationen zur Netzwerkkonnektivität für einen virtuellen Computer zur Verfügung.
ms.assetid: 59503c1b-203b-46ec-8a65-f21a746f170f
title: Msvm_NetworkConnectionDiagnosticInformation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticInformation
- Msvm_NetworkConnectionDiagnosticInformation.RoundTripTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d12109c562dff014a9864146f8ba27f4863d2249644708d550b308dbd5744a9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521020"
---
# <a name="msvm_networkconnectiondiagnosticinformation-class"></a>Msvm \_ NetworkConnectionDiagnosticInformation-Klasse

Stellt Informationen zur Netzwerkkonnektivität für einen virtuellen Computer zur Verfügung.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticInformation
{
  uint32 RoundTripTime;
};
```

## <a name="members"></a>Member

Die **Msvm \_ NetworkConnectionDiagnosticInformation-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ NetworkConnectionDiagnosticInformation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**RoundTripTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Roundtripzeit für die Pinganforderung.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1703 desktop apps only (Nur \[ Desktop-Apps der Version 1703)\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




