---
title: TaskFolder.DeleteFolder-Methode
description: Löscht für die Skripterstellung einen Unterordner aus dem übergeordneten Ordner.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- DeleteFolder-Methode Taskplaner
- DeleteFolder-Methode Taskplaner , TaskFolder-Objekt
- TaskFolder-Objekt Taskplaner , DeleteFolder-Methode
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
ms.openlocfilehash: a73dfe168b599de6e09d5437d0be4ec7a851d246f9fcbce0f79f662b62c56212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974900"
---
# <a name="taskfolderdeletefolder-method"></a>TaskFolder.DeleteFolder-Methode

Löscht für die Skripterstellung einen Unterordner aus dem übergeordneten Ordner.

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

Der Name des zu entfernenden Unterordners. Der Stammtaskordner wird mit einem umgekehrten Schrägstrich \\ () angegeben. Dieser Parameter kann ein relativer Pfad zu dem Ordner sein, den Sie löschen möchten. Ein Beispiel für einen Taskordnerpfad im Stammtaskordner ist \\ MyTaskFolder. Das Zeichen "." kann nicht zum Angeben des aktuellen Aufgabenordners und des .-Zeichens verwendet werden. -Zeichen können nicht verwendet werden, um den übergeordneten Aufgabenordner im Pfad anzugeben.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Wird nicht unterstützt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TaskFolder**](taskfolder.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





