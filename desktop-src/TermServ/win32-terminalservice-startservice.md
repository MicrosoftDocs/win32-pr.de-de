---
title: Start Service-Methode der Win32_Service-Klasse (Remotedesktopdienste)
description: Versucht, den referenzierten Dienst in seinen Startzustand zu versetzen.
ms.assetid: 4DA05C48-03A0-4D4B-9E69-0404393C219C
ms.tgt_platform: multiple
keywords:
- Start Service-Methode Remotedesktopdienste
- Start Service-Methode Remotedesktopdienste, Win32_Service-Klasse
- Win32_Service-Klasse Remotedesktopdienste, StartService-Methode
topic_type:
- apiref
api_name:
- Win32_Service.StartService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e37a17922fe0f4f3f5a3e4f1cd4d8eb67dc2858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391857"
---
# <a name="startservice-method-of-the-win32_service-class-remote-desktop-services"></a>Start Service-Methode der Win32_Service-Klasse (Remotedesktopdienste)

Die **Start Service** -Methode versucht, den Dienst, auf den verwiesen wird, in den Startzustand zu versetzen.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Die Anforderung wurde akzeptiert.

</dd> <dt>

**1**
</dt> <dd>

Die Anforderung wird nicht unterstützt.

</dd> <dt>

**2**
</dt> <dd>

Der Benutzer verfügte nicht über die erforderlichen Zugriffsrechte.

</dd> <dt>

**3**
</dt> <dd>

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**4**
</dt> <dd>

Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.

</dd> <dt>

**5**
</dt> <dd>

Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** -Eigenschaft) ist gleich 0, 1 oder 2.

</dd> <dt>

**6**
</dt> <dd>

Der Dienst wurde nicht gestartet.

</dd> <dt>

**7**
</dt> <dd>

Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.

</dd> <dt>

**8**
</dt> <dd>

Unbekannter Fehler beim Starten des Dienstanbieter.

</dd> <dt>

**9**
</dt> <dd>

Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.

</dd> <dt>

**10**
</dt> <dd>

Der Dienst wird schon ausgeführt.

</dd> <dt>

**11**
</dt> <dd>

Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.

</dd> <dt>

**12**
</dt> <dd>

Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.

</dd> <dt>

**13**
</dt> <dd>

Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.

</dd> <dt>

**14**
</dt> <dd>

Der Dienst wurde vom System deaktiviert.

</dd> <dt>

**15**
</dt> <dd>

Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.

</dd> <dt>

**16**
</dt> <dd>

Dieser Dienst wird aus dem System entfernt.

</dd> <dt>

**17**
</dt> <dd>

Der Dienst hat keinen Ausführungs Thread.

</dd> <dt>

**Jahren**
</dt> <dd>

Der Dienst weist zirkuläre Abhängigkeiten auf, wenn er gestartet wird.

</dd> <dt>

**19**
</dt> <dd>

Ein Dienst wird unter dem gleichen Namen ausgeführt.

</dd> <dt>

**20**
</dt> <dd>

Der Dienst Name enthält ungültige Zeichen.

</dd> <dt>

**21**
</dt> <dd>

An den Dienst wurden ungültige Parameter übermittelt.

</dd> <dt>

**22**
</dt> <dd>

Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.

</dd> <dt>

**23**
</dt> <dd>

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**24**
</dt> <dd>

Der Dienst ist im System derzeitig angehalten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Obwohl es möglicherweise keinen praktischen Unterschied zwischen einem beendeten Dienst und einem angehaltenen Dienst gibt, werden die beiden Zustände anders als der SCM angezeigt. Ein angehaltener Dienst ist ein Dienst, der nicht ausgeführt wird und die gesamte Dienst Start Prozedur durchlaufen muss. Ein angehaltene Dienst wird jedoch weiterhin ausgeführt, aber seine funktionstüchtig ist angehalten. Aus diesem Grund muss ein angehaltene Dienst nicht die gesamte Dienst Start Prozedur durchlaufen, sondern erfordert ein anderes Verfahren, um die Funktionsweise fortzusetzen.

Sie müssen die richtige-Methode verwenden, um einen Dienst zu starten, der angehalten wurde, oder um einen Dienst fortzusetzen, der angehalten wurde. Die [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Methoden " **StartService** " und " [**ResumeService**](win32-terminalservice-resumeservice.md) " sollten in den folgenden Situationen verwendet werden:

-   Wenn ein Dienst aktuell beendet ist, müssen Sie ihn mit der **Start Service** -Methode neu starten. [**ResumeService**](win32-terminalservice-resumeservice.md) kann einen Dienst nicht starten, der zurzeit beendet ist.
-   Wenn ein Dienst angehalten wird, müssen Sie [**ResumeService**](win32-terminalservice-resumeservice.md)verwenden. Wenn Sie die **Start Service** -Methode für einen angehaltenen Dienst verwenden, erhalten Sie die Meldung "der Dienst wird bereits ausgeführt." Der Dienst bleibt jedoch angehalten, bis der Steuerungs Code zum Fortsetzen des dienstandens an ihn gesendet wird.

Wenn Sie einen beendeten Dienst starten, der von einem anderen Dienst abhängt, werden beide Dienste gestartet. Wenn ein Dienst mit dieser Methode gestartet wird, werden alle abhängigen Dienste nicht automatisch gestartet. Sie müssen die Association-Klasse [**Win32 \_ dependentservice**](/windows/desktop/CIMWin32Prov/win32-dependentservice) und die [assoziatoren von](/windows/desktop/WmiSdk/associators-of-statement) Query verwenden, um die abhängigen Elemente zu suchen und Sie separat zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Betriebssystemklassen](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**Win32 \_ Terminalservice**](win32-terminalservice.md)
</dt> <dt>

[WMI-Tasks: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

