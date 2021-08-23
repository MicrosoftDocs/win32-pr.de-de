---
description: Wird in der QueryGuestClusterInformation-Methode in der Msvm \_ VssService-Klasse verwendet, um Informationen über den Gastcluster abzurufen, zu dem die VM gehört.
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Msvm_GuestClusterInformation-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed353e0d9c4d3049e120b00a11bc3d1bf85e3a0b42e52deb4ed277b9bde9b96b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523294"
---
# <a name="msvm_guestclusterinformation-class"></a>Msvm \_ GuestClusterInformation-Klasse

Wird in der [**QueryGuestClusterInformation-Methode**](msvm-vssservice-queryguestclusterinformation.md) in der [**Msvm \_ VssService-Klasse**](msvm-vssservice.md) verwendet, um Informationen über den Gastcluster abzurufen, zu dem die VM gehört.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a>Member

Die **Msvm \_ GuestClusterInformation-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ GuestClusterInformation-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ClusterId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Bezeichner des Failoverclusters, zu dem das Gastbetriebssystem des virtuellen Computers gehört.

</dd> <dt>

**ClusterSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der Knoten im Cluster, zu der das Gastbetriebssystem des virtuellen Computers gehört.

</dd> <dt>

**IsActiveActive**
</dt> <dd> <dl> <dt>

Datentyp: **boolesches** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array booleischer Daten, das jeder freigegebenen virtuellen Festplatte entspricht und angibt, ob die entsprechende Datenträgerressource im Gastcluster von virtuellen Computern im Aktiv/Aktiv-Modus gemeinsam genutzt wird.

</dd> <dt>

**IsClustered**
</dt> <dd> <dl> <dt>

Datentyp: **boolesches** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array booleischer Daten, das jeder freigegebenen virtuellen Festplatte entspricht und angibt, ob der entsprechende Datenträger eine Clusterressource im Gastcluster ist.

</dd> <dt>

**IsOnline**
</dt> <dd> <dl> <dt>

Datentyp: **boolesches** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array booleischer Daten, das jeder freigegebenen virtuellen Festplatte entspricht und angibt, ob die entsprechende Datenträgerressource im Gastcluster online ist.

</dd> <dt>

**IsOwned**
</dt> <dd> <dl> <dt>

Datentyp: **boolesches** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array booleischer Daten, das jeder freigegebenen virtuellen Festplatte entspricht und angibt, ob sich die entsprechende Datenträgerressource im Gastcluster im Besitz dieses virtuellen Computers befindet.

</dd> <dt>

**LastResourceMoveTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Taktanzahl, wenn eine der freigegebenen Datenträgerressourcen zuletzt verschoben wurde.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10 Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**SharedVirtualHardDiskPaths**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array von freigegebenen virtuellen Festplattenpfaden, die mit dem virtuellen Computer verbunden sind.

</dd> <dt>

**SharedVirtualHardDisks**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array von RASD (Resource Allocation Setting Data), das die freigegebenen virtuellen Festplatten darstellt, die mit dem virtuellen Computer verbunden sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

