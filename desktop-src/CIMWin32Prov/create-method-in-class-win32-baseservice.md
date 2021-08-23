---
description: Erstellt einen neuen Dienst.
ms.assetid: e000b896-3b49-4650-b706-548592cfe721
ms.tgt_platform: multiple
title: Create-Methode der Win32_BaseService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 827a82bf76fe78b86f97efa3aa01e0ae1106cd81430952b5d5b2849b5b3dd492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547430"
---
# <a name="create-method-of-the-win32_baseservice-class"></a>Create-Methode der Win32 \_ BaseService-Klasse

Die **Create** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) erstellt einen neuen Dienst. Der *LoadOrderGroup-Parameter* stellt eine Gruppierung von Systemdiensten dar, die Ausführungsabhängigkeiten definieren. Die Dienste müssen in der von der Lastauftragsgruppe angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern das Vorhandensein der voraussenten Dienste, damit sie ordnungsgemäß funktionieren.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

## <a name="syntax"></a>Syntax


```mof
uint32 Create(
  [in] string  Name,
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ In\]
</dt> <dd>

Name des Diensts, der in der **Create-Methode installiert werden** soll. Die maximale Zeichenfolgenlänge beträgt 256 Zeichen. Die Dienststeuerungs-Manager-Datenbank behält die Groß-/Kleinschreibung der Zeichen bei, bei Dienstnamenvergleichen wird jedoch immer die Groß-/Kleinschreibung nicht beachtet. Schrägstriche (/) und doppelte schräge Schrägstriche \\ () sind ungültige Dienstnamenzeichen.

</dd> <dt>

*DisplayName* \[ In\]
</dt> <dd>

Anzeigename des Diensts. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager beibehalten. *Bei DisplayName-Vergleichen* wird die Groß-/Kleinschreibung immer nicht beachtet.

Einschränkungen: Akzeptiert den gleichen Wert wie der *Name-Parameter.*

Beispiel: "Atdisk".

</dd> <dt>

*PathName* \[ In\]
</dt> <dd>

Vollqualifizierter Pfad zur ausführbaren Datei, die den Dienst implementiert.

Beispiel: \\ "SystemRoot \\ \\ System32-Treiber \\afd.sys".

</dd> <dt>

*ServiceType* \[ In\]
</dt> <dd>

Typ der Dienste, die für Prozesse bereitgestellt werden, die sie aufrufen. Der Wert ist eine Bitmap.

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kerneltreiber** (1)


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Dateisystemtreiber** (2)


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Recognizer Driver** (8)


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Eigener Prozess** (16)


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Freigabeprozess** (32)


</dt> <dd></dd> <dt>

256
</dt> <dd>

Interaktiver Prozess

</dd> <dt>




</dt> <dd></dd> </dl> </dd> <dt>

*ErrorControl* \[ In\]
</dt> <dd>

Schweregrad des Fehlers, wenn die **Create-Methode** nicht gestartet werden kann. Der Wert gibt die Aktion an, die vom Startprogramm ausgeführt wird, wenn ein Fehler auftritt. Alle Fehler werden vom System protokolliert.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)


</dt> <dd>

Der Benutzer wird nicht benachrichtigt.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)


</dt> <dd>

Der Benutzer wird benachrichtigt.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** (2)


</dt> <dd>

Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (3)


</dt> <dd>

Das System versucht, mit einer guten Konfiguration zu beginnen.

</dd> </dl> </dd> <dt>

*StartMode* \[ In\]
</dt> <dd>

Startmodus des Windows Basisdiensts.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Startstart** ("Start")


</dt> <dd>

Vom Betriebssystemlader gestarteter Gerätetreiber. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Systemstart** ("System")


</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungsprozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Automatischer Start** ("Automatisch")


</dt> <dd>

Der Dienst soll während des Systemstarts automatisch vom Dienstkontroll-Manager gestartet werden.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manuell")


</dt> <dd>

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService-Methode**](startservice-method-in-class-win32-service.md) aufruft.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("Deaktiviert")


</dt> <dd>

Dienst, der nicht mehr gestartet werden kann.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ In\]
</dt> <dd>

True **gibt an,** dass der Dienst Fenster auf dem Desktop erstellen oder mit ihnen kommunizieren kann.

</dd> <dt>

*StartName* \[ In\]
</dt> <dd>

Kontoname, unter dem der Dienst ausgeführt wird. Je nach Diensttyp kann der Kontoname in Form von "DomainName \\ Username" (Domänenname Benutzername) angegeben werden. Der Dienstprozess wird mit einer dieser beiden Formen protokolliert, wenn er ausgeführt wird. Wenn das Konto zur integrierten Domäne gehört, ". \\ Benutzername" kann angegeben werden. Wenn **NULL** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Für Einen Kernel oder Treiber auf Systemebene enthält *StartName* den Namen des Treiberobjekts (d. h. FileSystem Rdr oder Driver Xns), den das Eingabe- und Ausgabesystem \\ \\ \\ (E/A) zum Laden des \\ Gerätetreibers verwendet. Wenn **NULL** angegeben wird, wird der Treiber mit einem Standardobjektnamen ausgeführt, der vom E/A-System basierend auf dem Dienstnamen erstellt wird. Beispiel: \\ DWDOM-Administrator.

</dd> <dt>

*StartPassword* \[ In\]
</dt> <dd>

Kennwort für den Kontonamen, der durch den *StartName-Parameter angegeben* wird. Geben **Sie NULL** an, wenn Sie das Kennwort nicht ändern. Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.

</dd> <dt>

*LoadOrderGroup* \[ In\]
</dt> <dd>

Gruppenname, der dem neuen Dienst zugeordnet ist. Ladereihenfolgegruppen sind in der Registrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden. Wenn der Zeiger NULL **ist** oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe. Abhängigkeiten zwischen Gruppen sollten im *LoadOrderGroupDependencies-Parameter aufgeführt* werden. Dienste in der Liste der Last reihenfolgengruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die nicht in der Liste der Last reihenfolgengruppen enthalten sind, gefolgt von Diensten, die nicht zu einer Gruppe gehören. Die Registrierung verfügt über eine Liste der Last reihenfolgengruppen unter:

**HKEY \_ LOCAL \_ MACHINE-System** \\  \\ **CurrentControlSet-Steuerelement** \\  \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ In\]
</dt> <dd>

Array von Last reihenfolgengruppen, die vor diesem Dienst gestartet werden müssen. Jedes Element im Array wird durch **NULL** getrennt, und die Liste wird durch zwei **NULL-Werte** beendet. In Visual Basic skript können Sie ein vbArray übergeben. Wenn der Zeiger NULL **ist** oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Gruppennamen muss das SC \_ GROUP IDENTIFIER-Zeichen (definiert in der Datei Winsvc.h) vorangestellt werden, um es von einem Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben \_ Namespace verwenden. Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

</dd> <dt>

*ServiceDependencies* \[ In\]
</dt> <dd>

Array, das Namen von Diensten enthält, die gestartet werden müssen, bevor dieser Dienst gestartet wird. Jedes Element im Array wird durch **NULL** getrennt, und die Liste wird durch zwei **NULL-Werte** beendet. In Visual Basic skript können Sie ein vbArray übergeben. Wenn der Zeiger NULL **ist** oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst ausgeführt wird, von dem er abhängig ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.

<dl> <dt>

**Erfolgreich**
</dt> <dd>

0

Die Anforderung wurde akzeptiert.

</dd> <dt>

**Nicht unterstützt**
</dt> <dd>

1

Die Anforderung wird nicht unterstützt.

</dd> <dt>

**Zugriff verweigert**
</dt> <dd>

2

Der Benutzer hatte nicht den erforderlichen Zugriff.

</dd> <dt>

**Ausgeführte abhängige Dienste**
</dt> <dd>

3

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**Ungültiges Dienststeuerelement**
</dt> <dd>

4

Der angeforderte Steuerungscode ist nicht gültig, oder es ist für den Dienst nicht akzeptabel.

</dd> <dt>

**Dienst kann Steuerelement nicht akzeptieren**
</dt> <dd>

5

Der angeforderte Steuerungscode kann nicht an den Dienst gesendet werden, da der Zustand des Diensts ([**Win32 \_ BaseService**](win32-baseservice.md)) ist.**State-Eigenschaft)** ist gleich 0, 1 oder 2.

</dd> <dt>

**Dienst nicht aktiv**
</dt> <dd>

6

Der Dienst wurde nicht gestartet.

</dd> <dt>

**Timeout für Dienstanforderungen**
</dt> <dd>

7

Der Dienst hat auf die Startanforderung nicht rechtzeitig reagiert.

</dd> <dt>

**Unbekannter Fehler**
</dt> <dd>

8

Interaktiver Prozess.

</dd> <dt>

**Pfad nicht gefunden**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Dienstdatei wurde nicht gefunden.

</dd> <dt>

**Dienst wird bereits ausgeführt**
</dt> <dd>

10

Der Dienst wird schon ausgeführt.

</dd> <dt>

**Dienstdatenbank gesperrt**
</dt> <dd>

11

Die Datenbank zum Hinzufügen eines neuen Diensts ist gesperrt.

</dd> <dt>

**Dienstabhängigkeit gelöscht**
</dt> <dd>

12

Eine Abhängigkeit, von der dieser Dienst abhängt, wurde aus dem System entfernt.

</dd> <dt>

**Dienstabhängigkeitsfehler**
</dt> <dd>

13

Der Dienst hat den Dienst nicht gefunden, der von einem abhängigen Dienst benötigt wird.

</dd> <dt>

**Dienst deaktiviert**
</dt> <dd>

14

Der Dienst wurde vom System deaktiviert.

</dd> <dt>

**Fehler bei der Dienstanmeldung**
</dt> <dd>

15

Der Dienst hat nicht die richtige Authentifizierung, um im System ausgeführt zu werden.

</dd> <dt>

**Dienst, der für den Löschvorgang markiert ist**
</dt> <dd>

16

Dieser Dienst wird aus dem System entfernt.

</dd> <dt>

**Dienst ohne Thread**
</dt> <dd>

17

Es gibt keinen Ausführungsthread für den Dienst.

</dd> <dt>

**Status Circular Dependency**
</dt> <dd>

18

Es gibt Ringabhängigkeiten beim Starten des Diensts.

</dd> <dt>

**Doppelter Statusname**
</dt> <dd>

19

Es wird ein Dienst unter dem gleichen Namen ausgeführt.

</dd> <dt>

**Ungültiger Statusname**
</dt> <dd>

20

Der Name des Diensts enthält ungültige Zeichen.

</dd> <dt>

**Ungültiger Parameter "Status"**
</dt> <dd>

21

Ungültige Parameter wurden an den Dienst übergeben.

</dd> <dt>

**Status Ungültiges Dienstkonto**
</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist entweder ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.

</dd> <dt>

**Statusdienst ist vorhanden**
</dt> <dd>

23

Der Dienst ist in der Datenbank der im System verfügbaren Dienste vorhanden.

</dd> <dt>

**Dienst wurde bereits angehalten**
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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> </dl>

 

