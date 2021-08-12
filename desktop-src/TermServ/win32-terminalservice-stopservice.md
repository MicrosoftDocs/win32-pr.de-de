---
title: StopService-Methode der Win32_Service -Klasse (Sdoias.h) (Terminaldienst)
description: Platziert den Dienst, der durch das Win32 \_ TerminalService-Objekt dargestellt wird, in den Beendet-Zustand.
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- StopService-Remotedesktopdienste
- StopService-methode Remotedesktopdienste , Win32_Service-Klasse
- Win32_Service klasse Remotedesktopdienste , StopService-Methode
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
ms.openlocfilehash: 4edbdb9e3b7fa48476f70e550bf1255de344880df440381fcd48adefa2f68d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604360"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a>StopService-Methode der Win32_Service -Klasse (Sdoias.h) für den Terminaldienst

Die **StopService** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) platziert den Dienst, der durch das [**Win32 \_ TerminalService-Objekt**](win32-terminalservice.md) dargestellt wird, in den Beendet-Zustand.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehlerkonstistenzen**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT-Werte** finden Sie unter [Systemfehlercodes](/windows/desktop/Debug/system-error-codes).

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

Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService ) ist.**](/windows/desktop/CIMWin32Prov/win32-baseservice)**State-Eigenschaft)** ist gleich 0, 1 oder 2.

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

Eine Abhängigkeit, von der dieser Dienst abhängig ist, wurde aus dem System entfernt.

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

Der Dienst verfügt beim Starten über zirkuläre Abhängigkeiten.

</dd> <dt>

**19**
</dt> <dd>

Ein Dienst wird unter demselben Namen ausgeführt.

</dd> <dt>

**20**
</dt> <dd>

Der Dienstname enthält ungültige Zeichen.

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

Nachdem Sie ermittelt haben, welche Dienste beendet oder angehalten werden können, können Sie die **Methoden StopService** und [**PauseService**](win32-terminalservice-pauseservice.md) verwenden, um Dienste zu beenden und anzuhalten. Die Entscheidung, einen Dienst zu beenden, anstatt ihn anzuhalten (oder umgekehrt), hängt von mehreren Faktoren ab, z. B.:

-   Kann der Dienst angehalten werden? Wenn nicht, ist die einzige Option das Beenden des Diensts.
-   Müssen Sie weiterhin Clientanforderungen für alle Personen behandeln, die bereits mit dem Dienst verbunden sind? In diesem Beispiel ermöglicht das Anhalten eines Diensts in der Regel die Handhabung vorhandener Clients, während der Zugriff auf neue Clients verweigert wird. Wenn Sie dagegen einen Dienst beenden, werden alle Clients sofort getrennt.
-   Müssen Sie einen Dienst neu konfigurieren, damit die Änderungen sofort wirksam werden? Obwohl Diensteigenschaften geändert werden können, während ein Dienst angehalten wird, werden die meisten davon erst wirksam, wenn der Dienst tatsächlich beendet und neu gestartet wird.

Der Skriptcode, der zum Beenden eines Diensts erforderlich ist, ist fast identisch mit dem Code, der zum Anhalten des Diensts erforderlich ist.

Wenn Sie versuchen, einen Dienst zu beenden, bei dem abhängige Dienste ausgeführt werden, schlägt die **StopService-Methode** mit dem Rückgabewert 3 fehl. Die abhängigen Dienste müssen zuerst beendet werden.

Wenn Sie einen Dienst beenden, überprüfen Sie sofort [**win32 \_ TerminalService**](win32-terminalservice.md).**State-Eigenschaft,** da der Wert den Dienst weiterhin als ausgeführt anzeigen kann.

## <a name="examples"></a>Beispiele

[Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell-Beispiel: Legt den Dienststatus für Remotecomputer fest.

Das [VBScript-Beispiel](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) Zum Beenden eines Diensts und seiner abhängigen Dienste beendet einen Dienst und alle abhängigen Dienste.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| Header<br/>                   | <dl> <dt>Sdoias.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32-Dienst \_**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Betriebssystemklassen](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[WMI-Aufgaben: Dienste](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[**PauseService**](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 

