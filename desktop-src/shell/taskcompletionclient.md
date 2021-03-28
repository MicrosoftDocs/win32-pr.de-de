---
description: Aktiviert die Aufgaben Vervollständigung.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: Taskcompletionclient-Schnittstelle
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
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217684"
---
# <a name="taskcompletionclient-interface"></a>Taskcompletionclient-Schnittstelle

Aktiviert die Aufgaben Vervollständigung.

## <a name="members"></a>Member

Die **taskcompletionclient** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Taskcompletionclient** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **taskcompletionclient** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                    | BESCHREIBUNG                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [**Applytaskcompletion**](taskcompletionclient-applytaskcompletion.md)   | Startet den Abschluss der Aufgabe.<br/> |
| [**Revoketaskcompletion**](taskcompletionclient-revoketaskcompletion.md) | Beendet den Abschluss der Aufgabe.<br/>   |



 

## <a name="remarks"></a>Bemerkungen

Die GUID für diese Schnittstelle lautet "E97D552D-9ae9-46aa-9151-D2DA4BBB5E96".

Diese API ist veraltet und wird in zukünftigen Versionen von Windows möglicherweise nicht mehr verfügbar sein. Apps sollten stattdessen die APIs im [**Windows. applicationmodel. extendedexecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) -Namespace verwenden.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
