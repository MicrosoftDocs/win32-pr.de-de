---
description: Wird in der Methode queryguestclusterinformation in der MSVM \_ VssService-Klasse verwendet, um Informationen über das Gast Cluster abzurufen, zu dem der virtuelle Computer gehört.
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
ms.openlocfilehash: ee7fa33f142e47b9493e53aa5bc4779623d6ef40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347807"
---
# <a name="msvm_guestclusterinformation-class"></a>MSVM \_ guestclusterinformation-Klasse

Wird in der Methode [**queryguestclusterinformation**](msvm-vssservice-queryguestclusterinformation.md) in der [**MSVM \_ VssService**](msvm-vssservice.md) -Klasse verwendet, um Informationen über das Gast Cluster abzurufen, zu dem der virtuelle Computer gehört.

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

Die **MSVM \_ guestclusterinformation** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ guestclusterinformation** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**ClusterId**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Bezeichner des Failoverclusters, zu dem das Gast Betriebssystem der VM gehört.

</dd> <dt>

**Cluster size**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der Knoten im Cluster, zu denen das Gast Betriebssystem der VM gehört.

</dd> <dt>

**Isactiveactive**
</dt> <dd> <dl> <dt>

Datentyp: **Boolesches** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array von booleschen Werten, die jeder freigegebenen virtuellen Festplatte entsprechen und angeben, ob die zugehörige Datenträger Ressource im Gast Cluster von virtuellen Computern im aktiv/aktiv-Modus gemeinsam genutzt wird.

</dd> <dt>

**IsClustered**
</dt> <dd> <dl> <dt>

Datentyp: **Boolesches** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array von booleschen Werten, die jeder freigegebenen virtuellen Festplatte entsprechen und angeben, ob es sich bei dem entsprechenden Datenträger um eine Cluster Ressource im Gast Cluster handelt.

</dd> <dt>

**IsOnline**
</dt> <dd> <dl> <dt>

Datentyp: **Boolesches** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array von booleschen Werten, die jeder freigegebenen virtuellen Festplatte entsprechen und angeben, ob die entsprechende Datenträger Ressource im Gast Cluster online ist.

</dd> <dt>

**Isowned**
</dt> <dd> <dl> <dt>

Datentyp: **Boolesches** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array von booleschen Werten, die jeder freigegebenen virtuellen Festplatte entsprechen und angeben, ob die zugehörige Datenträger Ressource im Gast Cluster im Besitz dieses virtuellen Computers ist.

</dd> <dt>

**Lastresourcemuvetime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Takt Anzahl, wenn eine der freigegebenen Datenträger Ressourcen zuletzt verschoben wurde.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10, Version 1703 und Windows Server 2016 hinzugefügt.

 

</dd> <dt>

**Sharedvirtualharddiskpath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array von freigegebenen virtuellen Festplatten Pfaden, die mit dem virtuellen Computer verbunden sind.

</dd> <dt>

**Sharedvirtualharddisks**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array von Ressourcen Zuordnungs Einstellungsdaten (rasd), die die freigegebenen virtuellen Festplatten darstellen, die mit dem virtuellen Computer verbunden sind.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

