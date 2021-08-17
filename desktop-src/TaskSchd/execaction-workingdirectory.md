---
title: ExecAction.WorkingDirectory (Eigenschaft)
description: Für die Skripterstellung ruft das Verzeichnis ab, das entweder die ausführbare Datei oder die dateien enthält, die von der ausführbaren Datei verwendet werden, oder legt es fest.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- WorkingDirectory-Taskplaner
- WorkingDirectory-Eigenschaft Taskplaner , ExecAction-Objekt
- ExecAction-Objekt Taskplaner , WorkingDirectory-Eigenschaft
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 362b6cbb977e66a92425da1355f0747660d867f67aec0ad684f7e8e3956edc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139443"
---
# <a name="execactionworkingdirectory-property"></a>ExecAction.WorkingDirectory (Eigenschaft)

Für die Skripterstellung ruft das Verzeichnis ab, das entweder die ausführbare Datei oder die dateien enthält, die von der ausführbaren Datei verwendet werden, oder legt es fest.

## <a name="syntax"></a>Syntax


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>Eigenschaftswert

Das Verzeichnis, das entweder die ausführbare Datei oder die dateien enthält, die von der ausführbaren Datei verwendet werden.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML wird das Arbeitsverzeichnis der Anwendung im [**WorkingDirectory-Element**](taskschedulerschema-workingdirectory-exectype-element.md) des Taskplaner angegeben.

Der Pfad wird überprüft, um sicherzustellen, dass er gültig ist, wenn der Task registriert wird, nicht, wenn diese Eigenschaft festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





