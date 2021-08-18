---
description: Erstellt einen neuen Dienst, der vom Systemtreiber verwaltet wird.
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Create-Methode der Win32_SystemDriver-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a85b18a04672f63c4f1fd8fe4fa386ffb4e3094e817b53a20af9887a84748a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080154"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a>Create-Methode der \_ Win32-SystemDriver-Klasse

Die [Methode WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) **erstellen** erstellt einen neuen Dienst, der vom Systemtreiber verwaltet wird. Der *Win32 \_ LoadOrderGroup-Parameter* stellt eine Gruppierung von Systemdiensten dar, die Ausführungsabhängigkeiten definieren. Die Dienste müssen in der von der Load Order Group angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern, dass die Vorgängerdienste vorhanden sind, damit sie ordnungsgemäß funktionieren.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zur Verwendung dieser Methode finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

Name des Diensts, der in der **Create-Methode** installiert werden soll. Die maximale Zeichenfolgenlänge beträgt 256 Zeichen. Die Service Control Manager-Datenbank behält die Groß-/Kleinschreibung der Zeichen bei, bei Dienstnamenvergleichen wird jedoch immer die Groß-/Kleinschreibung beachtet. Schrägstriche (/) und doppelte umgekehrte Schrägstriche \\ () sind ungültige Dienstnamenzeichen.

</dd> <dt>

*DisplayName* \[ In\]
</dt> <dd>

Anzeigename des Diensts. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager beibehalten. *Bei DisplayName-Vergleichen* wird die Groß-/Kleinschreibung immer nicht beachtet.

Einschränkungen: Akzeptiert den gleichen Wert wie der *Name-Parameter.*

Beispiel: "Atdisk".

</dd> <dt>

*PathName* \[ In\]
</dt> <dd>

Vollqualifizierte Pfad zur ausführbaren Datei, die den Dienst implementiert.

Beispiel: \\ "SystemRoot \\ \\ System32-Treiber \\afd.sys".

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

Schweregrad des Fehlers, wenn die **Create-Methode** nicht gestartet werden kann. Dieser Wert gibt die Aktion an, die vom Startprogramm ausgeführt wird, wenn ein Fehler auftritt. Alle Fehler werden vom System protokolliert.

<dt>

0
</dt> <dd>

"Ignorieren"

Der Benutzer wird nicht benachrichtigt.

</dd> <dt>

1
</dt> <dd>

"Normal"

Der Benutzer wird benachrichtigt.

</dd> <dt>

2
</dt> <dd>

"Schwerwiegend"

Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.

</dd> <dt>

3
</dt> <dd>

"Kritisch"

Das System versucht, mit einer guten Konfiguration zu beginnen.

</dd> </dl> </dd> <dt>

*StartMode* \[ In\]
</dt> <dd>

Startmodus des Windows Basisdiensts.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Booten**


</dt> <dd>

Vom Betriebssystemladeprogramm gestarteter Gerätetreiber. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**


</dt> <dd>

Der Vom Initialisierungsprozess des Betriebssystems gestartete Gerätetreiber. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch**


</dt> <dd>

Der Dienst wird während des Systemstarts automatisch vom Dienststeuerungs-Manager gestartet.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell**


</dt> <dd>

Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService-Methode**](startservice-method-in-class-win32-systemdriver.md) aufruft.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**


</dt> <dd>

Dienst, der nicht mehr gestartet werden kann.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ In\]
</dt> <dd>

True gibt an, dass der Dienst die Fenster auf dem Desktop erstellen oder mit ihnen kommunizieren kann.

</dd> <dt>

*StartName* \[ In\]
</dt> <dd>

Kontoname, unter dem der Dienst ausgeführt wird. Je nach Diensttyp kann der Kontoname im Format DomainName \\ Username oder User Principal Name (UPN) () Username@DomainName vorliegen. Der Dienstprozess wird bei der Ausführung mit einer dieser beiden Formen protokolliert. Wenn das Konto zur integrierten Domäne gehört, . \\ Der Benutzername kann angegeben werden. Wenn **NULL** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Für Treiber auf Kernel- oder Systemebene enthält *StartName* den Namen des Treiberobjekts (d.h. \\ FileSystem \\ Rdr oder \\ Driver \\ Xns), den das E/A-System zum Laden des Gerätetreibers verwendet. Wenn **NULL** angegeben ist, wird der Treiber mit einem Standardobjektnamen ausgeführt, der vom E/A-System basierend auf dem Dienstnamen erstellt wurde.

Beispiel: DWDOM \\ Admin

</dd> <dt>

*StartPassword* \[ In\]
</dt> <dd>

Kennwort für den vom *StartName-Parameter* angegebenen Kontonamen. Geben Sie **NULL** an, wenn Sie das Kennwort nicht ändern. Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.

</dd> <dt>

*LoadOrderGroup* \[ In\]
</dt> <dd>

Gruppenname, der dem neuen Dienst zugeordnet ist. Ladereihenfolgengruppen sind in der Registrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden. Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, gehört der Dienst nicht zu einer Gruppe. Abhängigkeiten zwischen Gruppen sollten im *LoadOrderGroupDependencies-Parameter* aufgeführt werden. Dienste in der Liste der Ladereihenfolgegruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die nicht in der Liste der Lastenreihenfolgegruppen enthalten sind, gefolgt von Diensten, die keiner Gruppe angehören. Die Registrierung verfügt über eine Liste der Ladereihenfolgegruppen unter:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[ In\]
</dt> <dd>

Array von Lastreihenfolgegruppen, die vor diesem Dienst gestartet werden müssen. Jedes Element im Array wird durch **NULL** getrennt, und die Liste wird durch zwei **NULL-Werte** beendet. In Visual Basic oder Skript können Sie ein vbArray übergeben. Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Gruppennamen muss das **Zeichen SC GROUP \_ \_ IDENTIFIER** (definiert in der Datei Winsvc.h) vorangestellt sein, um sie von einem Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden. Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

</dd> <dt>

*ServiceDependencies* \[ In\]
</dt> <dd>

Ein Array, das die Namen der Dienste enthält, die gestartet werden müssen, bevor dieser Dienst gestartet wird. Jedes Element im Array wird durch **NULL** getrennt, und die Liste wird durch zwei **NULL-Werte** beendet. In Visual Basic oder Skript können Sie ein vbArray übergeben. Wenn der Zeiger **NULL** ist oder auf eine leere Zeichenfolge zeigt, weist der Dienst keine Abhängigkeiten auf. Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich erstellt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und eine beliebige andere Zahl, um einen Fehler anzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

