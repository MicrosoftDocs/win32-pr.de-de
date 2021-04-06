---
title: TaskDefinition.XmlText-Eigenschaft
description: Ruft bei der Skripterstellung die XML-formatierte Definition der Aufgabe ab oder legt diese fest.
ms.assetid: b10dd3cd-51b5-4e0e-a6cb-3b6794afb4cd
keywords:
- XmlText-Eigenschaft Taskplaner
- XmlText-Eigenschaft Taskplaner, Taskdefinition-Objekt
- Taskdefinition-Objekt Taskplaner, XmlText-Eigenschaft
topic_type:
- apiref
api_name:
- TaskDefinition.XmlText
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b736e3c90dea08ca201a992634d388da87c9d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742432"
---
# <a name="taskdefinitionxmltext-property"></a>TaskDefinition.XmlText-Eigenschaft

Ruft bei der Skripterstellung die XML-formatierte Definition der Aufgabe ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
TaskDefinition.XmlText As String
```



## <a name="property-value"></a>Eigenschaftswert

Die XML-formatierte Definition der Aufgabe.

## <a name="remarks"></a>Bemerkungen

Der XML-Code für eine Aufgabe wird durch das [Taskplaner Schema](task-scheduler-schema.md)definiert. Ein Beispiel für eine XML-Aufgabe finden Sie unter Beispiel für den täglichen-Vorgang [(XML)](daily-trigger-example--xml-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





