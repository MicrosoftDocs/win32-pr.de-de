---
description: Ändert einen Win32 \_ systemdriver-Dienst.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Change-Methode der Win32_SystemDriver-Klasse (mbnapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: da814c8321e35189594bc350bd1e278a219bac59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483563"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a>Change-Methode der Win32 \_ systemdriver-Klasse

Die **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode ändert einen [**Win32 \_ systemdriver**](win32-systemdriver.md) -Dienst. Der [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md) -Parameter stellt eine Gruppierung von System Diensten dar, die Ausführungs Abhängigkeiten definieren. Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.

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

Der Anzeigename des Diensts Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten. Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet.

Einschränkungen: akzeptiert denselben Wert wie der *Name* -Parameter.

Beispiel: "ATDISK"

</dd> <dt>

*Pfadname* \[ in\]
</dt> <dd>

Der voll qualifizierte Pfad zur ausführbaren Datei, die den Dienst implementiert.

Beispiel: *\\ systemroot \\ system32 \\ Drivers \\afd.sys*

</dd> <dt>

*ServiceType* \[ in\]
</dt> <dd>

Typ der Dienste, die für die Prozesse bereitgestellt werden, die Sie anrufen.

<dt>

1 (0x1)
</dt> <dd>

Kernel Treiber

</dd> <dt>

2 (0x2)
</dt> <dd>

Datei System Treiber

</dd> <dt>

4 (0x4)
</dt> <dd>

Adapter

</dd> <dt>

8 (0x8)
</dt> <dd>

Erkennungs Treiber

</dd> <dt>

16 (0x10)
</dt> <dd>

Eigener Prozess

</dd> <dt>

32 (0x20)
</dt> <dd>

Freigabeprozess

</dd> <dt>

256 (0x100)
</dt> <dd>

Interaktiver Prozess

</dd> </dl> </dd> <dt>

*ErrorControl* \[ in\]
</dt> <dd>

Der Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann. Der Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt. Alle Fehler werden vom System protokolliert.

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

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Start Start**


</dt> <dd>

Der Gerätetreiber wurde vom Betriebssystem Lader gestartet.

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Start Start**


</dt> <dd>

Gerätetreiber, der vom Betriebssystem Lader gestartet wird.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start**


</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Automatisch starten**


</dt> <dd>

Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Bedarfs Start**


</dt> <dd>

Dienst, der vom Dienststeuerungs-Manager gestartet wird, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-systemdriver.md) -Methode aufruft.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**


</dt> <dd>

Dienst, der nicht gestartet werden kann.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ in\]
</dt> <dd>

Ein-Wert, der, wenn der Wert **true** ist, den Windows-Dienst auf dem Desktop erstellen oder mit diesem kommunizieren kann.

</dd> <dt>

*StartName* \[ in\]
</dt> <dd>

Der Kontoname, unter dem der Dienst ausgeführt wird. Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name Benutzername" oder "" aufweisen \\ . \\ User. Bei der Ausführung wird der Dienst Prozess mit einer dieser beiden Formulare protokolliert. , Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden. Wenn eine leere Zeichenfolge angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Bei Kernel-oder System Treibern enthält *StartName* den Treiber Objektnamen, z \\ . b. Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden. Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, den das e/a-System basierend auf dem Dienstnamen erstellt, z. b. dwdom \\ Admin.

Sie können auch das UPN-Format (User Principal Name, Benutzer Prinzipal Name) verwenden, um den **StartName** anzugeben, z *Username@DomainName* . b..

</dd> <dt>

*Startpassword* \[ in\]
</dt> <dd>

Das Kennwort für den Kontonamen, der durch den *StartName* -Parameter angegeben wird. Geben Sie **null** an, wenn Sie das Kennwort nicht ändern. Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.

> [!Note]  
> Wenn ein Dienst von einem lokalen System in ein Netzwerk oder von einem Netzwerk auf ein lokales System geändert wird, muss *startpassword* eine leere Zeichenfolge ("") und nicht **null** sein.

 

</dd> <dt>

*LoadOrderGroup* \[ in\]
</dt> <dd>

Der Gruppenname, dem er zugeordnet ist. Lade Auftrags Gruppen sind in der Systemregistrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden. Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe. Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden. Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören. Die Systemregistrierung enthält eine Liste der Lade Auftrags Gruppen unter:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder**

</dd> <dt>

*Loadordergroupabhängigkeiten* \[ in\]
</dt> <dd>

Die Liste der Gruppen mit Lade Reihen, die vor dem Start dieses Dienstanbieter gestartet werden müssen. Das Array ist doppelt **null**-terminiert. Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten. Gruppennamen müssen dem **SC- \_ Gruppen \_ Bezeichner** (definiert in der Datei "winsvc. h") vorangestellt werden, um Sie von Dienstnamen zu unterscheiden, weil Dienste und Dienstgruppen denselben Namespace verwenden. Die Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

</dd> <dt>

*Service Abhängigkeiten* \[ in\]
</dt> <dd>

Die Liste, die die Namen der Dienste enthält, die vor dem Start dieses Diensts gestartet werden müssen. Das Array ist doppelt **null**-terminiert. Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten. Die Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich geändert wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und jede andere Zahl, die auf einen Fehler hinweist.

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Zugriff verweigert** (2)
</dt> <dt>

**Abhängige Dienste werden ausgeführt** (3)
</dt> <dt>

**Ungültige Dienst Kontrolle** (4).
</dt> <dt>

Der **Dienst kann die Steuerung nicht akzeptieren** (5).
</dt> <dt>

Der **Dienst ist nicht aktiv** (6).
</dt> <dt>

**Timeout für Dienst Anforderungen** (7)
</dt> <dt>

**Unbekannter Fehler** (8)
</dt> <dt>

Der **Pfad wurde nicht gefunden** (9).
</dt> <dt>

Der **Dienst wird bereits ausgeführt** (10).
</dt> <dt>

**Dienst Datenbank gesperrt** (11)
</dt> <dt>

**Dienst Abhängigkeit gelöscht** (12)
</dt> <dt>

**Dienst Abhängigkeitsfehler** (13)
</dt> <dt>

**Dienst deaktiviert** (14)
</dt> <dt>

Fehler bei der **Dienst Anmeldung** (15).
</dt> <dt>

Der **Dienst wurde zum Löschen markiert** (16).
</dt> <dt>

**Dienst ohne Thread** (17)
</dt> <dt>

**Status zirkuläre Abhängigkeit** (18)
</dt> <dt>

**Doppelter Name des Status** (19)
</dt> <dt>

**Ungültiger Name** (20).
</dt> <dt>

**Ungültiger Parameter** (21).
</dt> <dt>

**Ungültiges Dienst Konto** (22).
</dt> <dt>

**Status Dienst vorhanden** (23)
</dt> <dt>

Der **Dienst wurde bereits angeh** alten (24).
</dt> <dt>

**Sonstige** (25 4294967295)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Um einen Dienst von einem Netzwerkdienst in das lokale System zu ändern, verwenden Sie die folgenden Werte für die Parameter " *StartName* " und " *startpassword* ":


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Um einen Dienst von einem lokalen Systemdienst in einen Netzwerkdienst zu ändern, verwenden Sie die folgenden Werte für die Parameter " *StartName* " und " *startpassword* ":


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

[**Win32- \_ System Treiber**](win32-systemdriver.md)
</dt> </dl>

 

