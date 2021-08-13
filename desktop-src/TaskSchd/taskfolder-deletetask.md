---
title: TaskFolder.DeleteTask-Methode
description: Löscht für die Skripterstellung einen Task aus dem Ordner.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- DeleteTask-Methode Taskplaner
- DeleteTask-Methode Taskplaner , TaskFolder-Objekt
- TaskFolder-Objekt Taskplaner , DeleteTask-Methode
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c12b3ca9d66817972d75bd3ffbab61bcdcdff5dcc227e680ed6548f77d1b0de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119402400"
---
# <a name="taskfolderdeletetask-method"></a>TaskFolder.DeleteTask-Methode

Löscht für die Skripterstellung einen Task aus dem Ordner.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ In\]
</dt> <dd>

Der Name des Tasks, der beim Registrieren des Tasks angegeben wurde. Das Zeichen "." kann nicht zum Angeben des aktuellen Aufgabenordners und des .-Zeichens verwendet werden. -Zeichen können nicht verwendet werden, um den übergeordneten Aufgabenordner im Pfad anzugeben.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Wird nicht unterstützt. Der Wert ist 0.

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

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





