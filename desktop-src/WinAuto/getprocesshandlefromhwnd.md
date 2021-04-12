---
title: Getprocesshandlefromhwnd-Funktion
description: Ruft ein Prozess handle von einem Fenster Handle ab.
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- Getprocesshandlefromhwnd-Funktion Windows-Barrierefreiheit
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
ms.openlocfilehash: bee00f36f236396816e7bb54cadbe6914f3437e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103820"
---
# <a name="getprocesshandlefromhwnd-function"></a>Getprocesshandlefromhwnd-Funktion

Ruft ein Prozess handle von einem Fenster Handle ab.

## <a name="syntax"></a>Syntax


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HWND* \[ in\]
</dt> <dd>

Typ: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

Das Fensterhandle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **handle**](/windows/desktop/WinProg/windows-data-types)**

Bei erfolgreicher Ausführung wird das Handle des Prozesses zurückgegeben, der das Fenster besitzt.

Wenn dies nicht erfolgreich ist, wird **null** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

In früheren Versionen des Betriebssystems konnte ein Prozess einen anderen Prozess (z. b. für den Zugriff auf den Arbeitsspeicher) mit [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)eröffnen. Diese Funktion ist erfolgreich, wenn der Aufrufer über entsprechende Berechtigungen verfügt. in der Regel müssen der Aufrufer und der Ziel Prozess derselbe Benutzer sein.

Bei Windows Vista schlägt [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) jedoch in dem Szenario fehl, in dem der Aufrufer UIAccess hat, und der Ziel Prozess erhöht sich. In diesem Fall befindet sich der Besitzer des Ziel Prozesses in der Gruppe "Administratoren", aber der aufrufende Prozess wird mit dem eingeschränkten Token ausgeführt, ist also nicht Mitglied dieser Gruppe und wird der Zugriff auf den erweiterten Prozess verweigert. Wenn der Aufrufer über UIAccess verfügt, kann er jedoch einen Windows-Hook verwenden, um Code in den Ziel Prozess einzufügen und innerhalb des Ziel Prozesses ein Handle zurück an den Aufrufer zu senden.

**Getprocesshandlefromhwnd** ist eine Hilfsfunktion, die diese Technik verwendet, um das Handle des Prozesses zu erhalten, der das angegebene HWND besitzt. Beachten Sie, dass Sie nur erfolgreich ist, wenn der Aufrufer und der Ziel Prozess als derselbe Benutzer ausgeführt werden. Das zurückgegebene Handle verfügt über die folgenden Berechtigungen: Prozess-DUP-handle Prozess-VM-Vorgang Prozess-VM \_ \_ \| \_ \_ \| \_ \_ \| Schreibvorgang VM \_ Schreibvorgang \_ \| synchronisieren. Wenn andere Berechtigungen erforderlich sind, ist es möglicherweise erforderlich, die einbinden-Technik explizit zu implementieren, anstatt diese Funktion zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Oleacc.dll</dt> </dl> |



 

