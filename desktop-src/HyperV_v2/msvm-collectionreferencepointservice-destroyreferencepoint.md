---
description: Zerstört eine vorhandene Verweis Punkt Auflistung. Diese Methode kann als Nebeneffekt andere Verweis Punkte zerstören, die von der betroffenen Verweis Punkt Auflistung abhängig sind.
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: Destroyreferencepoint-Methode der Msvm_CollectionReferencePointService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d7fb3fd9168778854518022744f1a0c5ba3c5f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132016"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Destroyreferencepoint-Methode der MSVM \_ collectionreferencepointservice-Klasse

Zerstört eine vorhandene Verweis Punkt Auflistung. Diese Methode kann als Nebeneffekt andere Verweis Punkte zerstören, die von der betroffenen Verweis Punkt Auflistung abhängig sind.

## <a name="syntax"></a>Syntax


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Affectedreferencepointcollection* \[ in\]
</dt> <dd>

Verweis auf die betroffene Verweis Punkt Auflistung des virtuellen Systems.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang lange ausgeführt wird, kann optional ein Auftrag zurückgegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, wird entweder 0 (kein Fehler) oder 4096 (Auftrag gestartet) zurückgegeben. Andernfalls wird ein Fehler zurückgegeben.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

Fehler **(2** )
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**Ungültiger Status** (5)
</dt> <dt>

**Ungültiger Typ** (6)
</dt> <dt>

**DMTF reserviert** (..)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097.32767)
</dt> <dt>

**Hersteller spezifisch** (32768.65535)
</dt> </dl>

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

 

 




