---
description: Exportiert eine Verweispunktauflistung in eine Datei. Die Verweispunktauflistung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourceneinstellungen werden in der resultierenden Datei beibehalten.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: ExportReferencePoint-Methode der Msvm_CollectionReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3084cdecdd9a5c5808884a609b6bd91f4d50b814d64a96c8ea9e7470c9ece728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681900"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>ExportReferencePoint-Methode der Msvm \_ CollectionReferencePointService-Klasse

Exportiert eine Verweispunktauflistung in eine Datei. Die Verweispunktauflistung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourceneinstellungen werden in der resultierenden Datei beibehalten.

## <a name="syntax"></a>Syntax


```mof
uint32 ExportReferencePoint(
  [in]  CIM_Collection  REF ReferencePointCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ReferencePointCollection* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**\_ CIM-Auflistung,**](cim-collection.md) die die zu exportierende Verweispunktauflistung darstellt.

</dd> <dt>

*ExportDirectory* \[ In\]
</dt> <dd>

Der vollqualifizierte Pfad des Verzeichnisses, in das die Verweispunktauflistung exportiert werden soll.

</dd> <dt>

*ExportSettingData* \[ In\]
</dt> <dd>

Eine Instanz von [**Msvm \_ CollectionReferencePointExportSettingData,**](msvm-collectionreferencepointexportsettingdata.md) die die Einstellungen für den Exportvorgang darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Ein optionaler Verweis, der zurückgegeben wird, wenn der Vorgang asynchron ausgeführt wird. Falls vorhanden, kann der zurückgegebene Verweis auf eine Instanz von [**CIM \_ ConcreteJob**](cim-concretejob.md) verwendet werden, um den Fortschritt zu überwachen und das Ergebnis der Methode abzurufen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode synchron ausgeführt wird, wird bei Erfolg 0 zurückgegeben. Wenn diese Methode asynchron ausgeführt wird, wird 4096 zurückgegeben, und der Job-Ausgabeparameter kann verwendet werden, um den Fortschritt des asynchronen Vorgangs nachzuverfolgen. Jeder andere Rückgabewert gibt einen Fehler an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




