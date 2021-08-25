---
title: GetProcessHandleFromHwnd-Funktion
description: Ruft ein Prozesshand handle aus einem Fensterhand handle ab.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- GetProcessHandleFromHwnd-Funktion Windows Barrierefreiheit
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4096f77b4295e9567f17f747a5aee1edae1b592cb49c89547102cb6d017b7814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860350"
---
# <a name="getprocesshandlefromhwnd-function"></a>GetProcessHandleFromHwnd-Funktion

Ruft ein Prozesshand handle aus einem Fensterhand handle ab.

## <a name="syntax"></a>Syntax


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwnd* \[ In\]
</dt> <dd>

Typ: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

Das Fensterhandle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HANDLE**](/windows/desktop/WinProg/windows-data-types)**

Bei Erfolg wird das Handle des Prozesses zurückgegeben, der das Fenster besitzt.

Wenn dies nicht erfolgreich ist, wird **NULL zurückgegeben.**

## <a name="remarks"></a>Hinweise

In früheren Versionen des Betriebssystems konnte ein Prozess einen anderen Prozess (z. B. für den Zugriff auf den Arbeitsspeicher) mithilfe von [**OpenProcess öffnen.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) Diese Funktion ist erfolgreich, wenn der Aufrufer über entsprechende Berechtigungen verfügt. In der Regel müssen der Aufrufer und der Zielprozess derselbe Benutzer sein.

Unter Windows Vista schlägt [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) jedoch in dem Szenario fehl, in dem der Aufrufer ÜBER UIAccess verfügt und der Zielprozess erhöht ist. In diesem Fall befindet sich der Besitzer des Zielprozesses in der Gruppe Administratoren, aber der aufrufende Prozess wird mit dem eingeschränkten Token ausgeführt, verfügt also nicht über eine Mitgliedschaft in dieser Gruppe und wird dem Zugriff auf den Prozess mit erhöhten Rechten verweigert. Wenn der Aufrufer jedoch über UIAccess verfügt, kann er einen Windows-Hook verwenden, um Code in den Zielprozess einzujizieren, und innerhalb des Zielprozesses ein Handle zurück an den Aufrufer senden.

**GetProcessHandleFromHwnd** ist eine Komfortfunktion, die diese Technik verwendet, um das Handle des Prozesses zu erhalten, der das angegebene HWND besitzt. Beachten Sie, dass dies nur in Fällen erfolgreich ist, in denen der Aufrufer und der Zielprozess als derselbe Benutzer ausgeführt werden. Das zurückgegebene Handle verfügt über die folgenden Berechtigungen: PROCESS \_ DUP \_ HANDLE PROCESS VM OPERATION PROCESS VM READ PROCESS VM \| WRITE \_ \_ \| \_ \_ \| \_ \_ \| SYNCHRONIZE. Wenn andere Berechtigungen erforderlich sind, kann es erforderlich sein, die Hookmethode explizit zu implementieren, anstatt diese Funktion zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Oleacc.dll</dt> </dl> |



 

