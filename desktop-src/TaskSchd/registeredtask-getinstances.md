---
title: RegisteredTask.GetInstances-Methode
description: Für die Skripterstellung gibt alle derzeit ausgeführten Instanzen der registrierten Aufgabe zurück.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- GetInstances-Methode Taskplaner
- GetInstances-Methode Taskplaner , RegisteredTask-Objekt
- RegisteredTask-Objekt Taskplaner , GetInstances-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f9224922e70242304423950a67bf4acd866d1a551a90f4c9a6dadb94470ba1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126060"
---
# <a name="registeredtaskgetinstances-method"></a>RegisteredTask.GetInstances-Methode

Für die Skripterstellung gibt alle derzeit ausgeführten Instanzen der registrierten Aufgabe zurück.

> [!Note]  
> **RegisteredTask.GetInstances** gibt nur Instanzen der aktuell ausgeführten registrierten Aufgabe zurück, die im oder unterhalb des Sicherheitskontexts eines Benutzers ausgeführt werden. Für Mitglieder der Gruppe "Administratoren" gibt **GetInstances** beispielsweise alle Instanzen der aktuell ausgeführten registrierten Aufgabe zurück. Für Mitglieder der Gruppe Benutzer gibt **GetInstances** jedoch nur Instanzen der aktuell ausgeführten registrierten Aufgabe zurück, die im Sicherheitskontext der Gruppe Benutzer ausgeführt werden.

 

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*flags* 
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 festgelegt werden.

</dd> <dt>

*runningTasks* \[ out\]
</dt> <dd>

Ein [**RunningTaskCollection-Objekt,**](runningtaskcollection.md) das alle derzeit ausgeführten Instanzen der Aufgabe enthält.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





