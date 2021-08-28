---
description: Stellt zusätzliche Informationen zur Verwendung mit der CreateReferencePoint-Methode der Msvm \_ CollectionReferencePointService-Klasse zur Verfügung.
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Msvm_CollectionReferencePointSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1164c61f9335ce900dfbcf0b317dd0c4c9a8f84c0a97aaf13b2ea851a80dbd17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130670"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a>Msvm \_ CollectionReferencePointSettingData-Klasse

Stellt zusätzliche Informationen zur Verwendung mit der [**CreateReferencePoint-Methode**](msvm-collectionreferencepointservice-createreferencepoint.md) der [**Msvm \_ CollectionReferencePointService-Klasse**](msvm-collectionreferencepointservice.md) zur Verfügung.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a>Member

Die **Msvm \_ CollectionReferencePointSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ CollectionReferencePointSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Konsistenzebene des Referenzpunkts.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Anwendungs konsistent** (1)


</dt> <dd>

Der Referenzpunkt gibt einen Zeitpunkt an, zu dem sich das virtuelle System im absturz konsistenten Zustand hatte.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Absturz konsistent** (2)


</dt> <dd>

Der Referenzpunkt gibt einen Zeitpunkt an, zu dem sich das virtuelle System im anwendungs konsistenten Zustand hatte.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




