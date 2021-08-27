---
description: Ändert ein von Win32 BaseService abgeleitetes \_ Dienstobjekt.
ms.assetid: d5f4f472-e7d9-4664-9430-9c77034a5978
ms.tgt_platform: multiple
title: Change-Methode der Win32_BaseService -Klasse (Mbnapi.h)
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
ms.openlocfilehash: 306f771df0e44cb11ec61631b2d6b51f11ccefac9a719776d3a483d5cc861133
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085830"
---
# <a name="change-method-of-the-win32_baseservice-class"></a>Change-Methode der Win32 \_ BaseService-Klasse

Die **Change** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) ändert ein von [**Win32 BaseService abgeleitetes \_ Dienstobjekt.**](win32-baseservice.md) Der [**Win32 \_ LoadOrderGroup-Parameter**](win32-loadordergroup.md) stellt eine Gruppe von Systemdiensten dar, die Ausführungsabhängigkeiten definieren. Die Dienste müssen in der von der Load Order Group angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern voraussente Dienste, um ordnungsgemäß zu funktionieren.

In diesem Thema wird Managed Object Format (MOF)-Syntax verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

*DisplayName* \[ In\]
</dt> <dd>

Der Anzeigename für einen Dienst. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager beibehalten. *Bei DisplayName-Vergleichen* wird die Groß-/Kleinschreibung immer nicht beachtet.

Einschränkungen: Akzeptiert den gleichen Wert wie der *Name-Parameter.*

Beispiel: "Atdisk".

</dd> <dt>

*PathName* \[ In\]
</dt> <dd>

Der vollqualifizierte Pfad zur ausführbaren Datei, die einen Dienst implementiert.

Beispiel: \\ "SystemRoot \\ \\ System32-Treiber \\afd.sys".

</dd> <dt>

*ServiceType* \[ In\]
</dt> <dd>

Typ der Dienste, die für Prozesse bereitgestellt werden, die sie aufrufen.

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



 (256)


</dt> <dd>

Interaktiver Prozess

</dd> </dl> </dd> <dt>

*ErrorControl* \[ In\]
</dt> <dd>

Schweregrad eines Fehlers, wenn dieser Dienst während des Starts nicht gestartet wird. Der Wert gibt die Aktion an, die das Startprogramm bei einem Fehler vorgibt. Das System protokolliert alle Fehler.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** (0)


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

*StartMode* \[ In\]
</dt> <dd>

Startmodus des Windows Basisdiensts.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Startstart** ("Start")


</dt> <dd>

Gerätetreiber, der vom Betriebssystemlader gestartet wird.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Systemstart** ("System")


</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungsprozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Automatischer Start** ("Automatisch")


</dt> <dd>

Der Dienst wird automatisch vom Dienststeuerungs-Manager während des Systemstarts gestartet.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manuell")


</dt> <dd>

Dienst, der vom Dienststeuerungs-Manager gestartet wird, wenn ein Prozess die [**StartService-Methode**](startservice-method-in-class-win32-baseservice.md) aufruft.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** ("Deaktiviert")


</dt> <dd>

Dienst, der nicht gestartet werden kann.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ In\]
</dt> <dd>

True **gibt an,** dass der Dienst ein Fenster auf dem Desktop erstellen oder mit diesem kommunizieren kann.

</dd> <dt>

*StartName* \[ In\]
</dt> <dd>

Kontoname, unter dem der Dienst ausgeführt wird, abhängig vom Diensttyp. Der Kontoname kann in Form von DomainName \\ Username oder sein. \\ Nutzername. Wenn er ausgeführt wird, wird der Dienstprozess mithilfe eines der beiden vorherigen Formulare protokolliert. Wenn das Konto zur integrierten Domäne gehört, . \\ Der Benutzername kann angegeben werden. Wenn eine leere Zeichenfolge angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Für Treiber auf Kernel- oder Systemebene enthält *StartName* den Namen des Treiberobjekts, z. B. FileSystem Rdr oder Driver Xns, das vom Eingabe- und Ausgabesystem \\ \\ \\ (E/A) zum Laden des Gerätetreibers verwendet \\ wird. Wenn **NULL** angegeben ist, wird der Treiber mit einem Standardobjektnamen ausgeführt, den das E/A-System basierend auf dem Dienstnamen erstellt, z. B. DWDOM \\ Admin.

Sie können auch das UPN-Format (User Principal Name) verwenden, um **den StartName** anzugeben, z. *Username@DomainName* B. .

</dd> <dt>

*StartPassword* \[ In\]
</dt> <dd>

Kennwort für den Kontonamen, den *der StartName-Parameter* angibt. Geben **Sie NULL** an, wenn Sie das Kennwort nicht ändern. Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort hat.

> [!Note]  
> Wenn Sie einen Dienst vom lokalen System zum Netzwerk oder vom Netzwerk zum lokalen System ändern, muss *StartPassword* eine leere Zeichenfolge ("") und nicht **NULL sein.**

 

</dd> <dt>

*LoadOrderGroup* \[ In\]
</dt> <dd>

Gruppenname, dem er zugeordnet ist. Ladereihenfolgegruppen sind in der Systemregistrierung enthalten und bestimmen die Reihenfolge, in der Dienste in ein Betriebssystem geladen werden. Wenn der Zeiger NULL **ist** oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe. Abhängigkeiten zwischen Gruppen sollten im *LoadOrderGroupDependencies-Parameter aufgeführt* werden. Dienste in der Liste der Last reihenfolgengruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die nicht in der Liste der Last reihenfolgengruppen enthalten sind, gefolgt von Diensten, die nicht zu einer Gruppe gehören. Die Systemregistrierung verfügt über eine Liste von Lade reihenfolgengruppen unter **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.

</dd> <dt>

*LoadOrderGroupDependencies* \[ In\]
</dt> <dd>

Liste der Last reihenfolgengruppen, die gestartet werden müssen, bevor dieser Dienst gestartet wird. Das Array ist doppelt NULL-terminiert. Wenn der Zeiger NULL **ist** oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Gruppennamen muss das SC **\_ GROUP \_ IDENTIFIER-Zeichen** (definiert in der Datei Winsvc.h) vorangestellt werden, um sie von Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden. Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

</dd> <dt>

*ServiceDependencies* \[ In\]
</dt> <dd>

Liste, die die Namen der Dienste enthält, die gestartet werden müssen, bevor dieser Dienst gestartet wird. Das Array ist doppelt NULL-terminiert. Wenn der Zeiger NULL **ist** oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst ausgeführt wird, von dem er abhängig ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben.

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

**Ausgeführte abhängige Dienste**
</dt> <dd>

3

Der Dienst kann nicht beendet werden, da andere ausgeführte Dienste davon abhängig sind.

</dd> <dt>

**Ungültiges Dienststeuerelement**
</dt> <dd>

4

Der angeforderte Steuerungscode ist ungültig oder für den Dienst nicht akzeptabel.

</dd> <dt>

**Dienst kann Steuerelement nicht akzeptieren**
</dt> <dd>

5

Der angeforderte Steuerelementcode kann nicht an den Dienst gesendet werden, da die [**State-Eigenschaft**](win32-baseservice.md) im [**Win32 \_ BaseService-Objekt**](win32-baseservice.md) gleich 0, 1 oder 2 ist.

</dd> <dt>

**Dienst nicht aktiv**
</dt> <dd>

6

Der Dienst wurde nicht gestartet.

</dd> <dt>

**Timeout für Dienstanforderungen**
</dt> <dd>

7

Der Dienst reagiert nicht schnell auf die Startanforderung.

</dd> <dt>

**Unbekannter Fehler**
</dt> <dd>

8

Interaktiver Prozess.

</dd> <dt>

**Pfad nicht gefunden**
</dt> <dd>

9

Der Verzeichnispfad zur ausführbaren Datei des Diensts wurde nicht gefunden.

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

Eine Abhängigkeit, auf die dieser Dienst angewiesen ist, wird aus dem System entfernt.

</dd> <dt>

**Dienstabhängigkeitsfehler**
</dt> <dd>

13

Der Dienst findet den Dienst, der von einem abhängigen Dienst benötigt wird, nicht.

</dd> <dt>

**Dienst deaktiviert**
</dt> <dd>

14

Der Dienst ist vom System deaktiviert.

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

Das Konto, unter dem dieser Dienst ausgeführt werden soll, ist ungültig oder verfügt nicht über die Berechtigungen zum Ausführen des Diensts.

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

## <a name="remarks"></a>Hinweise

Um einen Dienst von einem Netzwerk in ein lokales System zu ändern, verwenden Sie die folgenden Werte für die Parameter *StartName* und *StartPassword:*


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Um einen Dienst von einem lokalen System in ein Netzwerk zu ändern, verwenden Sie die folgenden Werte für die Parameter *StartName* und *StartPassword:*


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Mbnapi.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> </dl>

 

