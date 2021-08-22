---
title: StartService-Methode der Win32_Service-Klasse (Remotedesktopdienste)
description: 'StartService-Methode der Win32_Service-Klasse (Remotedesktopdienste): Versucht, den Dienst, auf den verwiesen wird, in seinen Startzustand zu platzieren.'
ms.assetid: 4DA05C48-03A0-4D4B-9E69-0404393C219C
ms.tgt_platform: multiple
keywords:
- StartService-Methode Remotedesktopdienste
- StartService-Methode Remotedesktopdienste , Win32_Service-Klasse
- Win32_Service-Klasse Remotedesktopdienste , StartService-Methode
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
ms.openlocfilehash: 0a1a921f863ea2e06b7c84cf5ed66424d37f70be34f71c7c5975c95ff3d4308e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514360"
---
# <a name="startservice-method-of-the-win32_service-class-remote-desktop-services"></a>StartService-Methode der Win32_Service-Klasse (Remotedesktopdienste)

Die **StartService-Methode** versucht, den Dienst, auf den verwiesen wird, in seinen Startzustand zu platzieren.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes.](/windows/desktop/Debug/system-error-codes)

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

Der Benutzer hatte nicht den erforderlichen Zugriff.

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

Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)) ist.**State-Eigenschaft)** ist gleich 0, 1 oder 2.

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

Unbekannter Fehler beim Starten des Diensts.

</dd> <dt>

**9**
</dt> <dd>

Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.

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

Der Dienst verfügt über keinen Ausführungsthread.

</dd> <dt>

**18**
</dt> <dd>

Der Dienst weist beim Start zirkuläre Abhängigkeiten auf.

</dd> <dt>

**19**
</dt> <dd>

Ein Dienst wird unter demselben Namen ausgeführt.

</dd> <dt>

**20**
</dt> <dd>

Der Dienstname weist ungültige Zeichen auf.

</dd> <dt>

**21**
</dt> <dd>

Ungültige Parameter wurden an den Dienst übergeben.

</dd> <dt>

**22**
</dt> <dd>

Das Konto, unter dem dieser Dienst ausgeführt wird, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.

</dd> <dt>

**23**
</dt> <dd>

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**24**
</dt> <dd>

Der Dienst ist im System derzeitig angehalten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Obwohl es möglicherweise keinen praktischen Unterschied zwischen einem beendeten Dienst und einem angehaltenen Dienst gibt, werden die beiden Zustände für den SCM unterschiedlich angezeigt. Ein beendeter Dienst ist ein Dienst, der nicht ausgeführt wird und die gesamte Dienststartprozedur durchlaufen muss. Ein angehaltener Dienst wird jedoch weiterhin ausgeführt, aber seine Funktion wurde angehalten. Aus diesem Grund muss ein angehaltener Dienst nicht die gesamte Dienststartprozedur durchlaufen, sondern eine andere Prozedur, um die Funktionsweise fortzusetzen.

Sie müssen die richtige Methode verwenden, um einen angehaltenen Dienst zu starten oder einen angehaltenen Dienst fortzusetzen. Die [**Win32-Dienstmethoden \_**](/windows/desktop/CIMWin32Prov/win32-service) **StartService** und [**ResumeService**](win32-terminalservice-resumeservice.md) sollten in den folgenden Situationen verwendet werden:

-   Wenn ein Dienst derzeit beendet wird, müssen Sie ihn mithilfe der **StartService-Methode** neu starten. [**ResumeService**](win32-terminalservice-resumeservice.md) kann einen Dienst, der derzeit beendet ist, nicht starten.
-   Wenn ein Dienst angehalten wird, müssen Sie [**ResumeService**](win32-terminalservice-resumeservice.md)verwenden. Wenn Sie die **StartService-Methode** für einen angehaltenen Dienst verwenden, erhalten Sie die Meldung "Der Dienst wird bereits ausgeführt." Der Dienst bleibt jedoch angehalten, bis der Dienststeuerungscode zum Fortsetzen an ihn gesendet wird.

Wenn Sie einen beendeten Dienst starten, der von einem anderen Dienst abhängig ist, werden beide Dienste gestartet. Wenn ein Dienst mit dieser Methode gestartet wird, werden alle abhängigen Dienste nicht automatisch gestartet. Sie müssen die Zuordnungsklasse [**Win32 \_ DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) und die [Associators Of-Abfrage](/windows/desktop/WmiSdk/associators-of-statement) verwenden, um die Abhängigen zu suchen und separat zu starten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_Win32-Dienst**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Betriebssystemklassen](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[WMI-Aufgaben: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

