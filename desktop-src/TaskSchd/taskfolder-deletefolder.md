---
title: TaskFolder.DeleteFolder-Methode
description: Für die Skripterstellung löscht einen Unterordner aus dem übergeordneten Ordner.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- DeleteFolder-Taskplaner
- DeleteFolder-Methode Taskplaner , TaskFolder-Objekt
- TaskFolder-Taskplaner , DeleteFolder-Methode
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31080f017329cde376b646befd4b7e12ba02926b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387039"
---
# <a name="taskfolderdeletefolder-method"></a>TaskFolder.DeleteFolder-Methode

Für die Skripterstellung löscht einen Unterordner aus dem übergeordneten Ordner.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*folderName* \[ In\]
</dt> <dd>

Der Name des zu entfernenden Unterordners. Der Stammordner des Task wird mit einem schrägen Schrägstrich () \\ angegeben. Dieser Parameter kann ein relativer Pfad zu dem Ordner sein, den Sie löschen möchten. Ein Beispiel für einen Taskordnerpfad unter dem Stammaufgabenordner ist \\ MyTaskFolder. Das Zeichen "." kann nicht verwendet werden, um den aktuellen Taskordner und "." anzugeben. -Zeichen können nicht verwendet werden, um den übergeordneten Taskordner im Pfad anzugeben.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Wird nicht unterstützt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TaskFolder**](taskfolder.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





