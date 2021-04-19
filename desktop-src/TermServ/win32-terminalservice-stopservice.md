---
title: Stop Service-Methode der Win32_Service-Klasse ("sdoias. h") (Terminal Dienst)
description: Platziert den Dienst, der durch das Win32 \_ Terminalservice-Objekt dargestellt wird, im beendeten Zustand.
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- Stop Service-Methode Remotedesktopdienste
- Stop Service-Methode Remotedesktopdienste, Win32_Service-Klasse
- Win32_Service Class Remotedesktopdienste, StopService-Methode
topic_type:
- apiref
api_name:
- Win32_Service.StopService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1b21db330bb9111b96fb244200845cb83b3153
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2021
ms.locfileid: "106372017"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a>Stop Service-Methode der Win32_Service-Klasse (sdoias. h) für den Terminal Dienst

Die **StopService** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versetzt den Dienst, der durch das [**Win32 \_ Terminalservice**](win32-terminalservice.md) -Objekt dargestellt wird, in den Zustand "beendet".

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 StopService();
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

Nachdem Sie ermittelt haben, welche Dienste beendet oder angehalten werden können, können Sie die-Methode **StopService** und die [**anhaleservice**](win32-terminalservice-pauseservice.md) -Methode verwenden, um-Dienste anzuhalten und anzuhalten. Die Entscheidung, einen Dienst zu stoppen, anstatt ihn anzuhalten oder umgekehrt, hängt von mehreren Faktoren ab, einschließlich der folgenden:

-   Ist der Dienst in der Lage, angehalten zu werden? Wenn dies nicht der Wert ist, ist die einzige Option der Dienst wird beendet.
-   Müssen Sie die Verarbeitung von Client Anforderungen für alle Benutzer fortsetzen, die bereits mit dem Dienst verbunden sind? Wenn dies der Fall ist, ermöglicht das Anhalten eines Dienstanbieter in der Regel die Verarbeitung vorhandener Clients, während der Zugriff auf neue Clients verweigert Wenn Sie einen Dienst beenden, werden dagegen alle Clients sofort getrennt.
-   Müssen Sie einen Dienst neu konfigurieren, damit die Änderungen sofort wirksam werden? Obwohl Dienst Eigenschaften geändert werden können, während ein Dienst angehalten wird, werden die meisten nicht wirksam, bis der Dienst tatsächlich beendet und neu gestartet wird.

Der zum Anhalten eines Dienstanbieter erforderliche Skriptcode ist nahezu identisch mit dem Code, der zum Anhalten des Dienstanbieter erforderlich ist.

Wenn Sie versuchen, einen Dienst zu beenden, für den abhängige Dienste ausgeführt werden, schlägt die **Stop Service** -Methode mit einem Rückgabewert von 3 fehl. Die abhängigen Dienste müssen zuerst beendet werden.

Wenn Sie einen Dienst beenden, überprüfen Sie den [**Win32 \_ Terminalservice**](win32-terminalservice.md)sofort.**State** -Eigenschaft, da der Dienst möglicherweise weiterhin als wird ausgeführt angezeigt wird.

## <a name="examples"></a>Beispiele

[Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell-Beispiel legt den Dienststatus für Remote Computer fest.

Das Beispiel zum [Beenden eines Diensts und seiner abhängigen](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript beendet einen Dienst und alle abhängigen Dienste.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| Header<br/>                   | <dl> <dt>Sdoias. h</dt> </dl>     |
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
</dt> <dt>

[**PauseService**](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 

