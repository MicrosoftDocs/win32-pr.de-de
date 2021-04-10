---
description: Ändert ein Dienst Objekt, das von Win32 \_ baseservice abgeleitet ist.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Change-Methode der Win32_BaseService-Klasse (mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a70ee83229a830e22fba4241a6c50eb8d971c5ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127228"
---
# <a name="change-method-of-the-win32_baseservice-class"></a>Change-Methode der Win32 \_ baseservice-Klasse

Die **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode ändert ein Dienst Objekt, das von [**Win32 \_ baseservice**](win32-baseservice.md)abgeleitet ist. Der [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md) -Parameter stellt eine Gruppe von System Diensten dar, die Ausführungs Abhängigkeiten definieren. Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern, dass Vorgänger Dienste ordnungsgemäß funktionieren.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Change(
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

*Display Name* \[ in\]
</dt> <dd>

Der Anzeige Name für einen Dienst. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager beibehalten. Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet

Einschränkungen: akzeptiert denselben Wert wie der *Name* -Parameter.

Beispiel: "ATDISK".

</dd> <dt>

*Pfadname* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad zur ausführbaren Datei, die einen Dienst implementiert.

Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys".

</dd> <dt>

*ServiceType* \[ in\]
</dt> <dd>

Typ der Dienste, die für Prozesse bereitgestellt werden, die Sie anrufen.

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**Kernel Treiber** (1)


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**Datei System Treiber** (2)


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**Adapter** (4)


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>**Erkennungs Treiber** (8)


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>**Eigener Prozess** (16)


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**Freigabeprozess** (32)


</dt> <dd></dd> <dt>



 (256)


</dt> <dd>

Interaktiver Prozess

</dd> </dl> </dd> <dt>

*ErrorControl* \[ in\]
</dt> <dd>

Schweregrad eines Fehlers, wenn dieser Dienst nicht während des Starts gestartet wird. Der Wert gibt die Aktion an, die das Start Programm durchführt, wenn ein Fehler auftritt. Das System protokolliert alle Fehler.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorieren** (0)


</dt> <dd>

Der Benutzer wird nicht benachrichtigt.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (1)


</dt> <dd>

Normal. Der Benutzer wird benachrichtigt.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Schwerwiegend** (2)


</dt> <dd>

Das System wird mit der letzten guten Konfiguration neu gestartet.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (3)


</dt> <dd>

Das System versucht, mit einer fehlerfreien Konfiguration zu neu starten.

</dd> </dl> </dd> <dt>

*StartMode* \[ in\]
</dt> <dd>

Der Start Modus des Windows-Basis Dienstanbieter.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Start Start** ("Start")


</dt> <dd>

Gerätetreiber, der vom Betriebssystem Lader gestartet wird.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")


</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>Automatischer **Start** ("automatisch")


</dt> <dd>

Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Bedarfs Start** ("manuell")


</dt> <dd>

Dienst, der vom Dienststeuerungs-Manager gestartet wird, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-baseservice.md) -Methode aufruft.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("deaktiviert")


</dt> <dd>

Dienst, der nicht gestartet werden kann.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ in\]
</dt> <dd>

**True** gibt an, dass der Dienst ein Fenster auf dem Desktop erstellen oder mit diesem kommunizieren kann.

</dd> <dt>

*StartName* \[ in\]
</dt> <dd>

Der Kontoname, unter dem der Dienst ausgeführt wird, der vom Diensttyp abhängig ist. Der Kontoname kann in der Form Domänen Name \\ Benutzername oder lauten \\ . User. Bei der Ausführung wird der Dienst Prozess mit einer der beiden vorherigen Formen protokolliert. , Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden. Wenn eine leere Zeichenfolge angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Für Treiber auf Kernel-oder Systemebene enthält *StartName* den Treiber Objektnamen, z \\ . b. Dateisystem- \\ rdr oder \\ Treiber- \\ xns, die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden. Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, den das e/a-System basierend auf dem Dienstnamen erstellt, z. b. dwdom \\ Admin.

Sie können auch das UPN-Format (User Principal Name, Benutzer Prinzipal Name) verwenden, um den **StartName** anzugeben, z *Username@DomainName* . b..

</dd> <dt>

*Startpassword* \[ in\]
</dt> <dd>

Kennwort für den Kontonamen, den der *StartName* -Parameter angibt. Geben Sie **null** an, wenn Sie das Kennwort nicht ändern. Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.

> [!Note]  
> Wenn Sie einen Dienst von einem lokalen System in ein Netzwerk oder von einem Netzwerk in ein lokales System ändern, muss *startpassword* eine leere Zeichenfolge ("") und nicht **null** sein.

 

</dd> <dt>

*LoadOrderGroup* \[ in\]
</dt> <dd>

Der Gruppenname, dem er zugeordnet ist. Lade Auftrags Gruppen sind in der Systemregistrierung enthalten und bestimmen die Reihenfolge, in der die Dienste in ein Betriebssystem geladen werden. Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe. Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden. Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören. Die Systemregistrierung enthält eine Liste der Lade Auftrags Gruppen, die sich unter **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder** befinden.

</dd> <dt>

*Loadordergroupabhängigkeiten* \[ in\]
</dt> <dd>

Liste der Lade Gruppen, die vor dem Start dieses Dienstanbieter gestartet werden müssen. Das Array ist doppelt **null**-terminiert. Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten. Gruppennamen müssen dem **SC- \_ Gruppen \_ Bezeichner** (definiert in der Datei "winsvc. h") vorangestellt werden, um Sie von Dienstnamen zu unterscheiden, weil Dienste und Dienstgruppen denselben Namespace verwenden. Die Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

</dd> <dt>

*Service Abhängigkeiten* \[ in\]
</dt> <dd>

Liste mit den Namen der Dienste, die vor dem Start dieses Diensts gestartet werden müssen. Das Array ist doppelt **null**-terminiert. Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten. Die Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.

</dd> </dl>

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

Der Benutzer verfügt nicht über die erforderlichen Zugriffsberechtigungen.

</dd> <dt>

**Abhängige Dienste werden ausgeführt**
</dt> <dd>

3

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**Ungültige Dienst Kontrolle.**
</dt> <dd>

4

Der angeforderte Steuerungs Code ist ungültig oder für den Dienst nicht zulässig.

</dd> <dt>

**Der Dienst kann keine Steuerung akzeptieren.**
</dt> <dd>

5

Der angeforderte Steuerungs Code kann nicht an den Dienst gesendet werden, da die [**State**](win32-baseservice.md) -Eigenschaft im [**Win32- \_ baseservice**](win32-baseservice.md) -Objekt gleich 0, 1 oder 2 ist.

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

Eine Abhängigkeit, von der dieser Dienst abhängig ist, wird aus dem System entfernt.

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

Dieser Dienst wird aus dem System entfernt.

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

An den Dienst wurden ungültige Parameter übermittelt.

</dd> <dt>

**Ungültiges Dienst Konto.**
</dt> <dd>

22

Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Dienstanbieter.

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

## <a name="remarks"></a>Bemerkungen

Um einen Dienst von einem Netzwerk auf ein lokales System zu ändern, verwenden Sie die folgenden Werte für die Parameter " *StartName* " und " *startpassword* ":


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Um einen Dienst von einem lokalen System in ein Netzwerk zu ändern, verwenden Sie die folgenden Werte für die Parameter " *StartName* " und " *startpassword* ":


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Mbnapi. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ baseservice**](win32-baseservice.md)
</dt> </dl>

 

