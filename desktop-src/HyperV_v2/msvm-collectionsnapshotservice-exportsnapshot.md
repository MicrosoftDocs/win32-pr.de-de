---
description: Exportiert eine Momentaufnahme Sammlung virtueller Computersysteme in eine Datei. Die Momentaufnahme Sammlung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen werden in der resultierenden Datei beibehalten.
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Exportsnapshot-Methode der Msvm_CollectionSnapshotService-Klasse
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
ms.openlocfilehash: f4dd29e001c8335477451e86151d950c25edb9b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215377"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Exportsnapshot-Methode der MSVM \_ collectionsnapshotservice-Klasse

Exportiert eine Momentaufnahme Sammlung virtueller Computersysteme in eine Datei. Die Momentaufnahme Sammlung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen werden in der resultierenden Datei beibehalten.

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

*Snapshotcollection* \[ in\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_**](cim-collection.md) -Auflistung, die die zu exportierende Momentaufnahme Auflistung darstellt.

</dd> <dt>

*Exportdirectory* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad des Verzeichnisses, in das die virtuelle System Sammlung exportiert werden soll. Wenn die Eigenschaft " **kreatevmexportsubdirectory** " im *exportsettingdata* -Parameter auf " **true** " festgelegt ist, kann dieses Verzeichnis für den Export mehrerer virtueller System Sammlungen wieder verwendet werden. bei dieser Methode werden die einzelnen Definitionen der virtuellen System Sammlung in einem separaten Unterverzeichnis unter diesem Pfad abgelegt.

</dd> <dt>

*Exportsettingdata* \[ in\]
</dt> <dd>

Eine Instanz von [**MSVM \_ collectionsnapshotexportsettingdata**](msvm-collectionsnapshotexportsettingdata.md) , die die Einstellungen für den Export Vorgang darstellt.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Ein optionaler Verweis, der zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird. Falls vorhanden, kann der zurückgegebene Verweis auf eine Instanz von [**CIM \_ concretejob**](cim-concretejob.md) verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der Methode abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode synchron ausgeführt wird, wird 0 zurückgegeben, wenn Sie erfolgreich ausgeführt wird. Wenn diese Methode asynchron ausgeführt wird, wird 4096 zurückgegeben, und der Auftrags Ausgabeparameter kann verwendet werden, um den Fortschritt des asynchronen Vorgangs zu verfolgen. Jeder andere Rückgabewert gibt einen Fehler an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ collectionsnapshotservice**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




