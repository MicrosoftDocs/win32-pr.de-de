---
description: Ändert einen \_ Win32-SystemDriver-Dienst.
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: Change-Methode der Win32_SystemDriver-Klasse (Mbnapi.h)
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
ms.openlocfilehash: 96ff327e84d3a5b6c66011506c162810f0fcc91d0cafe4053266aa8928f6e5a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925110"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a>Change-Methode der \_ Win32-SystemDriver-Klasse

Die **Change** [WMI-Klassenmethode](/windows/desktop/WmiSdk/retrieving-a-class) ändert einen [**Win32-SystemDriver-Dienst. \_**](win32-systemdriver.md) Der [**Win32 \_ LoadOrderGroup-Parameter**](win32-loadordergroup.md) stellt eine Gruppierung von Systemdiensten dar, die Ausführungsabhängigkeiten definieren. Die Dienste müssen in der von der Load Order Group angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern, dass die Vorgängerdienste vorhanden sind, damit sie ordnungsgemäß funktionieren.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

Der Anzeigename des Diensts Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager beibehalten. *Bei DisplayName-Vergleichen* wird die Groß-/Kleinschreibung immer nicht beachtet.

Einschränkungen: Akzeptiert den gleichen Wert wie der *Name-Parameter.*

Beispiel: "Atdisk"

</dd> <dt>

*PathName* \[ In\]
</dt> <dd>

Der vollqualifizierte Pfad zur ausführbaren Datei, die den Dienst implementiert.

Beispiel: *\\ SystemRoot \\ System32-Treiber \\ \\afd.sys*

</dd> <dt>

*ServiceType* \[ In\]
</dt> <dd>

Typ der Dienste, die für die Prozesse bereitgestellt werden, die sie aufrufen.

<dt>

1 (0x1)
</dt> <dd>

Kerneltreiber

</dd> <dt>

2 (0x2)
</dt> <dd>

Dateisystemtreiber

</dd> <dt>

4 (0x4)
</dt> <dd>

Adapter

</dd> <dt>

8 (0x8)
</dt> <dd>

Erkennungstreiber

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

*ErrorControl* \[ In\]
</dt> <dd>

Der Schweregrad des Fehlers, wenn dieser Dienst während des Starts nicht gestartet werden kann. Der Wert gibt die Aktion an, die vom Startprogramm ausgeführt wird, wenn ein Fehler auftritt. Alle Fehler werden vom System protokolliert.

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

*StartMode* \[ In\]
</dt> <dd>

Der Startmodus des Windows Basisdiensts.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Startstart**


</dt> <dd>

Vom Betriebssystemladeprogramm gestarteter Gerätetreiber.

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Startstart**


</dt> <dd>

Gerätetreiber, der vom Betriebssystemladeprogramm gestartet wird.

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Systemstart**


</dt> <dd>

Der Vom Initialisierungsprozess des Betriebssystems gestartete Gerätetreiber. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Automatischer Start**


</dt> <dd>

Dienst, der während des Systemstarts automatisch vom Dienststeuerungs-Manager gestartet werden soll.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Bedarfsstart**


</dt> <dd>

Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService-Methode**](startservice-method-in-class-win32-systemdriver.md) aufruft.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**


</dt> <dd>

Dienst, der nicht gestartet werden kann.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ In\]
</dt> <dd>

Ein -Wert, der bei **True** vom Dienst erstellt oder mit den Fenstern auf dem Desktop kommunizieren kann.

</dd> <dt>

*StartName* \[ In\]
</dt> <dd>

Der Kontoname, unter dem der Dienst ausgeführt wird. Je nach Diensttyp kann der Kontoname in form von DomainName \\ Username oder lauten. \\ Nutzername. Bei der Ausführung wird der Dienstprozess mit einer dieser beiden Formen protokolliert. Wenn das Konto zur integrierten Domäne gehört, . \\ Der Benutzername kann angegeben werden. Wenn eine leere Zeichenfolge angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Für Kernel- oder Treiber auf Systemebene enthält *StartName* den Namen des Treiberobjekts, z. \\ B. FileSystem \\ Rdr oder \\ Driver \\ Xns, den das E/A-System zum Laden des Gerätetreibers verwendet. Wenn **NULL** angegeben ist, wird der Treiber mit einem Standardobjektnamen ausgeführt, den das E/A-System basierend auf dem Dienstnamen erstellt, z. B. DWDOM \\ Admin.

Sie können auch das UPN-Format (User Principal Name) verwenden, um den **StartName** anzugeben, z. *Username@DomainName* B. .

</dd> <dt>

*StartPassword* \[ In\]
</dt> <dd>

Das Kennwort für den Kontonamen, der durch den *StartName-Parameter* angegeben wird. Geben Sie **NULL** an, wenn Sie das Kennwort nicht ändern. Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.

> [!Note]  
> Beim Ändern eines Diensts von einem lokalen System in ein Netzwerk oder von einem Netzwerk in ein lokales System muss *StartPassword* eine leere Zeichenfolge ("") und nicht **NULL** sein.

 

</dd> <dt>

*LoadOrderGroup* \[ In\]
</dt> <dd>

Der Gruppenname, dem er zugeordnet ist. Ladereihenfolgengruppen sind in der Systemregistrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden. Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe. Abhängigkeiten zwischen Gruppen sollten im *LoadOrderGroupDependencies-Parameter* aufgeführt werden. Dienste in der Liste der Ladereihenfolgegruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die nicht in der Liste der Lastenreihenfolgegruppen enthalten sind, gefolgt von Diensten, die keiner Gruppe angehören. Die Systemregistrierung verfügt über eine Liste der Lastreihenfolgegruppen unter:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ In\]
</dt> <dd>

Die Liste der Lastreihenfolgegruppen, die gestartet werden müssen, bevor dieser Dienst gestartet wird. Das Array ist doppelt **NULL**-terminiert. Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Gruppennamen muss das **Zeichen SC GROUP \_ \_ IDENTIFIER** (definiert in der WinSvc.h-Datei) vorangestellt sein, um sie von Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden. Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

</dd> <dt>

*ServiceDependencies* \[ In\]
</dt> <dd>

Die Liste, die die Namen der Dienste enthält, die gestartet werden müssen, bevor dieser Dienst gestartet wird. Das Array ist doppelt **NULL**-terminiert. Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich geändert wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und eine beliebige andere Zahl, um einen Fehler anzugeben.

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Zugriff verweigert** (2)
</dt> <dt>

**Abhängige Dienste, die ausgeführt werden** (3)
</dt> <dt>

**Ungültige Dienststeuerung** (4)
</dt> <dt>

**Dienst kann Steuerung nicht akzeptieren** (5)
</dt> <dt>

**Dienst nicht aktiv** (6)
</dt> <dt>

**Service Request Timeout** (7)
</dt> <dt>

**Unbekannter Fehler** (8)
</dt> <dt>

**Pfad nicht gefunden** (9)
</dt> <dt>

**Dienst wird bereits ausgeführt** (10)
</dt> <dt>

**Dienstdatenbank gesperrt** (11)
</dt> <dt>

**Dienstabhängigkeit gelöscht** (12)
</dt> <dt>

**Dienstabhängigkeitsfehler** (13)
</dt> <dt>

**Dienst deaktiviert** (14)
</dt> <dt>

**Fehler bei der Dienstanmeldung** (15)
</dt> <dt>

**Dienst zum Löschen markiert** (16)
</dt> <dt>

**Dienst ohne Thread** (17)
</dt> <dt>

**Statuszirkuläre Abhängigkeit** (18)
</dt> <dt>

**Doppelter Statusname** (19)
</dt> <dt>

**Ungültiger Statusname** (20)
</dt> <dt>

**Ungültiger Statusparameter** (21)
</dt> <dt>

**Status Ungültiges Dienstkonto** (22)
</dt> <dt>

**Statusdienst ist vorhanden** (23)
</dt> <dt>

**Dienst wurde bereits angehalten** (24)
</dt> <dt>

**Sonstige** (25 4294967295)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Um einen Dienst von einem Netzwerkdienst in das lokale System zu ändern, verwenden Sie die folgenden Werte für die Parameter *StartName* und *StartPassword:*


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



Um einen Dienst von einem lokalen Systemdienst in einen Netzwerkdienst zu ändern, verwenden Sie die folgenden Werte für die Parameter *StartName* und *StartPassword:*


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

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

