---
description: Exportiert eine Momentaufnahmesammlung virtueller Computersysteme in eine Datei. Die Momentaufnahmesammlung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourceneinstellungen werden in der resultierenden Datei beibehalten.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: ExportSnapshot-Methode der Msvm_CollectionSnapshotService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ec61899e92da562250bf392077468adef14a35eda72d89d28ad9b3ddc3da2f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426840"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>ExportSnapshot-Methode der Msvm \_ CollectionSnapshotService-Klasse

Exportiert eine Momentaufnahmesammlung virtueller Computersysteme in eine Datei. Die Momentaufnahmesammlung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourceneinstellungen werden in der resultierenden Datei beibehalten.

## <a name="syntax"></a>Syntax


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SnapshotCollection* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**\_ CIM-Sammlung,**](cim-collection.md) die die zu exportierende Momentaufnahmesammlung darstellt.

</dd> <dt>

*ExportDirectory* \[ In\]
</dt> <dd>

Der vollqualifizierte Pfad des Verzeichnisses, in das die Sammlung des virtuellen Systems exportiert werden soll. Wenn die **CreateVmExportSubdirectory-Eigenschaft** im *ExportSettingData-Parameter* auf **True** festgelegt ist, kann dieses Verzeichnis zum Exportieren mehrerer virtueller Systemsammlungen wiederverwendet werden, und diese Methode platziert jede Definition der Sammlung virtueller Systeme in einem separaten Unterverzeichnis unter diesem Pfad.

</dd> <dt>

*ExportSettingData* \[ In\]
</dt> <dd>

Eine Instanz von [**Msvm \_ CollectionSnapshotExportSettingData,**](msvm-collectionsnapshotexportsettingdata.md) die die Einstellungen für den Exportvorgang darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein optionaler Verweis, der zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird. Falls vorhanden, kann der zurückgegebene Verweis auf eine Instanz von [**CIM \_ ConcreteJob**](cim-concretejob.md) verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der -Methode zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode synchron ausgeführt wird, gibt sie 0 zurück, wenn sie erfolgreich ist. Wenn diese Methode asynchron ausgeführt wird, wird 4096 zurückgegeben, und der Job-Ausgabeparameter kann zum Nachverfolgen des Fortschritts des asynchronen Vorgangs verwendet werden. Jeder andere Rückgabewert gibt einen Fehler an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




