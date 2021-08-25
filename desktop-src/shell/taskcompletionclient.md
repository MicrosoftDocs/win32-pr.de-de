---
description: Aktiviert die Aufgabenerledigung.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: TaskCompletionClient-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: d03e52a15e6689b7f1ea98a2f1021874cab6a8967dd148b7eaf685ff3984e8cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773650"
---
# <a name="taskcompletionclient-interface"></a>TaskCompletionClient-Schnittstelle

Aktiviert die Aufgabenerledigung.

## <a name="members"></a>Member

Die **TaskCompletionClient-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **TaskCompletionClient** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **TaskCompletionClient-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                    | Beschreibung                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [**ApplyTaskCompletion**](taskcompletionclient-applytaskcompletion.md)   | Beginnt den Abschluss der Aufgabe.<br/> |
| [**RevokeTaskCompletion**](taskcompletionclient-revoketaskcompletion.md) | Beendet den Abschluss der Aufgabe.<br/>   |



 

## <a name="remarks"></a>Hinweise

Die GUID für diese Schnittstelle ist "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".

Diese API ist veraltet und möglicherweise in zukünftigen Versionen von nicht mehr Windows. Apps sollten die APIs im [**Windows. Stattdessen wird der ApplicationModel.ExtendedExecution-Namespace**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
