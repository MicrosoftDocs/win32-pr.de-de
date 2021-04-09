---
description: Versucht, einen benutzerdefinierten Steuerelement Code an einen Dienst zu senden.
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: UserControlService-Methode der Win32_BaseService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861599"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a>UserControlService-Methode der Win32 \_ baseservice-Klasse

Die [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode versucht, einen benutzerdefinierten Steuerelement Code an einen Dienst zu senden.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ControlCode* \[ in\]
</dt> <dd>

Ein-Wert, der einen Steuerungs Befehl für einen Dienst angibt. Ein Steuerelement Befehl ist beispielsweise ein Befehl zum Anhalten oder fortsetzen. Der Wert kann ein vordefinierter Code oder ein Wert und eine Aktion sein, die der Dienst definiert. Im folgenden sind die vordefinierten Kontrollcodes aufgeführt:

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**Dienst \_ Steuerung \_ fortsetzen**


</dt> <dd>

Benachrichtigt einen angehaltenen Dienst, fortgesetzt zu werden.

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**Dienst \_ Steuerungs \_ Abfrage**


</dt> <dd>

Benachrichtigt einen Dienst, die aktuellen Statusinformationen an den Dienststeuerungs-Manager zu melden.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**Dienst \_ Steuerung \_ netbindadd**


</dt> <dd>

Benachrichtigt einen Netzwerkdienst, dass eine neue Komponente für die Bindung vorhanden ist.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**Dienst \_ Steuerung \_ netbinddeaktiviert**


</dt> <dd>

Benachrichtigt einen Netzwerkdienst, dass eine seiner Bindungen deaktiviert ist.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**Dienst \_ Steuerung \_ netbindenable**


</dt> <dd>

Benachrichtigt einen Netzwerkdienst, dass eine deaktivierte Bindung aktiviert ist.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**Dienst \_ Steuerung \_ netbindremove**


</dt> <dd>

Benachrichtigt einen Netzwerkdienst, dass eine Komponente für die Bindung entfernt wurde.

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**Dienststeuerungs- \_ \_ paramchange**


</dt> <dd>

Benachrichtigt einen Dienst, dass seine Startparameter geändert werden.

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**Dienst \_ Steuerungs \_ Pause**


</dt> <dd>

Benachrichtigt einen Dienst, anzuhalten.

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**Dienst \_ Steuerungs \_ Ende**


</dt> <dd>

Benachrichtigt einen Dienst, anzuhalten.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der Werte zurück, der in der folgenden Liste aufgeführt ist, oder einen anderen Wert, um einen Fehler anzugeben.

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Die Anforderung wird akzeptiert.

</dd> <dt>

**Nicht unterstützt**
</dt> <dd>

1

Die Anforderung wird nicht unterstützt.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Der Benutzer verfügt nicht über die erforderlichen Zugriffsrechte.

</dd> <dt>

**Abhängige Dienste werden ausgeführt**
</dt> <dd>

3

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**Ungültige Dienst Kontrolle.**
</dt> <dd>

4

Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.

</dd> <dt>

**Der Dienst kann keine Steuerung akzeptieren.**
</dt> <dd>

5

Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, weil der Status des Diensts ([**Win32- \_ baseservice**](win32-baseservice.md).**State** -Eigenschaft) ist gleich 0, 1 oder 2.

</dd> <dt>

**Dienst nicht aktiv**
</dt> <dd>

6

Der Dienst wurde nicht gestartet.

</dd> <dt>

**Service Request-Timeout**
</dt> <dd>

7

Der Dienst antwortet nicht schnell auf die Start Anforderung.

</dd> <dt>

**Unbekannter Fehler.**
</dt> <dd>

8

Interaktiver Prozess.

</dd> <dt>

**Pfad nicht gefunden**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienst Datei wurde nicht gefunden.

</dd> <dt>

**Dienst wird bereits ausgeführt.**
</dt> <dd>

10

Der Dienst wird schon ausgeführt.

</dd> <dt>

**Dienst Datenbank gesperrt**
</dt> <dd>

11

Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.

</dd> <dt>

**Dienst Abhängigkeit gelöscht**
</dt> <dd>

12

Eine Abhängigkeit, von der dieser Dienst abhängt, wird aus dem System entfernt.

</dd> <dt>

**Dienst Abhängigkeitsfehler**
</dt> <dd>

13

Der Dienst findet den von einem abhängigen Dienst benötigten Dienst nicht.

</dd> <dt>

**Dienst deaktiviert**
</dt> <dd>

14

Der Dienst ist im System deaktiviert.

</dd> <dt>

**Fehler bei der Dienst Anmeldung**
</dt> <dd>

15

Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.

</dd> <dt>

**Der Dienst wurde zum Löschen markiert.**
</dt> <dd>

16

Der Dienst wird aus dem System entfernt.

</dd> <dt>

**Dienst ohne Thread**
</dt> <dd>

17

Es gibt keinen Ausführungsthread für den Dienst.

</dd> <dt>

**Status zirkuläre Abhängigkeit**
</dt> <dd>

18

Es gibt Ringabhängigkeiten beim Starten des Diensts.

</dd> <dt>

**Doppelter Name des Status**
</dt> <dd>

19

Es wird ein Dienst unter dem gleichen Namen ausgeführt.

</dd> <dt>

**Ungültiger Name**
</dt> <dd>

20

Der Name des diensdienstanbieter enthält ungültige Zeichen.

</dd> <dt>

**Ungültiger Parameter.**
</dt> <dd>

21

Ungültige Parameter wurden an den Dienst übermittelt.

</dd> <dt>

**Ungültiges Dienst Konto.**
</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt wird, ist ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.

</dd> <dt>

**Status Dienst vorhanden**
</dt> <dd>

23

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**Der Dienst wurde bereits angehalten.**
</dt> <dd>

24

Der Dienst ist im System derzeitig angehalten.

</dd> <dt>

**Andere**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ baseservice**](win32-baseservice.md)
</dt> </dl>

 

