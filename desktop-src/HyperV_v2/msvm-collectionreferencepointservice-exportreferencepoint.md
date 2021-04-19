---
description: Exportiert eine Verweis Punkt Auflistung in eine Datei. In der resultierenden Datei werden die Verweis Punkt Auflistung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen beibehalten.
ms.assetid: 0ed61ded-b4d6-40c5-98be-e192eb934387
title: Exportreferencepoint-Methode der Msvm_CollectionReferencePointService-Klasse
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
ms.openlocfilehash: 49517da44cc7955d825792afcc475c56e37fad37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362769"
---
# <a name="exportreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Exportreferencepoint-Methode der MSVM \_ collectionreferencepointservice-Klasse

Exportiert eine Verweis Punkt Auflistung in eine Datei. In der resultierenden Datei werden die Verweis Punkt Auflistung, die zugehörigen Konfigurationseinstellungen und die zugehörigen Ressourcen Einstellungen beibehalten.

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

*Referencepointcollection* \[ in\]
</dt> <dd>

Ein Verweis auf eine [**CIM \_**](cim-collection.md) -Auflistung, die die zu exportierende Verweis Punkt Auflistung darstellt.

</dd> <dt>

*Exportdirectory* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad des Verzeichnisses, in das die Verweis Punkt Auflistung exportiert werden soll.

</dd> <dt>

*Exportsettingdata* \[ in\]
</dt> <dd>

Eine Instanz von [**MSVM \_ collectionreferencepointexportsettingdata**](msvm-collectionreferencepointexportsettingdata.md) , die die Einstellungen für den Export Vorgang darstellt.

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

[**MSVM \_ collectionreferencepointservice**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




