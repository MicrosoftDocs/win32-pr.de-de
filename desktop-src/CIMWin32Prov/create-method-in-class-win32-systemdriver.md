---
description: Erstellt einen neuen Dienst, der vom System Treiber verwaltet wird.
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
ms.openlocfilehash: a4ae14243582ea1239e8cc68c1e1d5464339a45b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127764"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a>Create-Methode der Win32 \_ systemdriver-Klasse

Die **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode erstellt einen neuen Dienst, der vom System Treiber verwaltet wird. Der *Win32 \_ LoadOrderGroup* -Parameter stellt eine Gruppierung von System Diensten dar, die Ausführungs Abhängigkeiten definieren. Die Dienste müssen in der von der Gruppe "Lade Reihenfolge" angegebenen Reihenfolge initiiert werden, da die Dienste voneinander abhängig sind. Diese abhängigen Dienste erfordern, dass die Vorgänger Dienste ordnungsgemäß funktionieren.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

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

*Name* \[ in\]
</dt> <dd>

Name des Dienstanbieter, der in der **Create** -Methode installiert werden soll. Die maximale Zeichen folgen Länge beträgt 256 Zeichen. Die Dienst Steuerungs Verwaltung behält die Groß-/Kleinschreibung der Zeichen bei. bei Dienstnamen vergleichen wird jedoch immer die Groß-/Kleinschreibung beachtet. Vorwärts Schrägstriche (/) und doppelte umgekehrte Schrägstriche ( \\ ) sind ungültige Dienstnamen Zeichen.

</dd> <dt>

*Display Name* \[ in\]
</dt> <dd>

Der Anzeige Name des Dienstanbieter. Die maximale Länge der Zeichenfolge beträgt 256 Zeichen. Der Name wird im Dienststeuerungs-Manager nach Groß-/Kleinschreibung beibehalten. Bei *Display Name* -vergleichen wird immer die Groß-/Kleinschreibung beachtet.

Einschränkungen: akzeptiert denselben Wert wie der *Name* -Parameter.

Beispiel: "ATDISK".

</dd> <dt>

*Pfadname* \[ in\]
</dt> <dd>

Voll qualifizierter Pfad zur ausführbaren Datei, die den Dienst implementiert.

Beispiel: " \\ systemroot \\ system32 \\ Drivers \\afd.sys".

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

Der Schweregrad des Fehlers, wenn die **Create** -Methode nicht gestartet werden kann. Dieser Wert gibt die vom Start Programm ausgeführte Aktion an, wenn ein Fehler auftritt. Alle Fehler werden vom System protokolliert.

<dt>

0
</dt> <dd>

Lassen

Der Benutzer wird nicht benachrichtigt.

</dd> <dt>

1
</dt> <dd>

"Normal"

Der Benutzer wird benachrichtigt.

</dd> <dt>

2
</dt> <dd>

Starkem

Das System wird mit der letzten bekannten, fehlerfreien Konfiguration neu gestartet.

</dd> <dt>

3
</dt> <dd>

Kritisch

Das System versucht, mit einer guten Konfiguration zu beginnen.

</dd> </dl> </dd> <dt>

*StartMode* \[ in\]
</dt> <dd>

Der Start Modus des Windows-Basis Dienstanbieter.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Starten**


</dt> <dd>

Der Gerätetreiber wurde vom Betriebssystem Lader gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Anlage**


</dt> <dd>

Der Gerätetreiber wurde durch den Initialisierungs Prozess des Betriebssystems gestartet. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatisch**


</dt> <dd>

Der Dienst, der vom Dienststeuerungs-Manager beim Systemstart automatisch gestartet wird.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuell**


</dt> <dd>

Der Dienst, der vom Dienststeuerungs-Manager gestartet werden soll, wenn ein Prozess die [**StartService**](startservice-method-in-class-win32-systemdriver.md) -Methode aufruft.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert**


</dt> <dd>

Dienst, der nicht mehr gestartet werden kann.

</dd> </dl> </dd> <dt>

*DesktopInteract* \[ in\]
</dt> <dd>

**True** gibt an, dass der Dienst die Fenster auf dem Desktop erstellen oder mit Ihnen kommunizieren kann.

</dd> <dt>

*StartName* \[ in\]
</dt> <dd>

Der Kontoname, unter dem der Dienst ausgeführt wird. Abhängig vom Diensttyp kann der Kontoname die Form "Domänen Name \\ Benutzername" oder "Benutzer Prinzipal Name (UPN) Format ()" aufweisen Username@DomainName . Der Dienst Prozess wird mit einer dieser beiden Formulare protokolliert, wenn er ausgeführt wird. , Wenn das Konto zur integrierten Domäne gehört. \\ Der Benutzername kann angegeben werden. Wenn **null** angegeben wird, wird der Dienst als LocalSystem-Konto angemeldet. Bei Kernel-oder System Treibern enthält *StartName* den Treiber Objektnamen ( \\ Dateisystem- \\ rdr oder \\ Treiber- \\ XNS), die vom Eingabe-und Ausgabesystem zum Laden des Gerätetreibers verwendet werden. Wenn **null** angegeben wird, wird der Treiber mit einem Standard Objektnamen ausgeführt, der vom e/a-System basierend auf dem Dienstnamen erstellt wurde.

Beispiel: dwdom- \\ Administrator

</dd> <dt>

*Startpassword* \[ in\]
</dt> <dd>

Das Kennwort für den Kontonamen, der durch den *StartName* -Parameter angegeben wird. Geben Sie **null** an, wenn Sie das Kennwort nicht ändern. Geben Sie eine leere Zeichenfolge an, wenn der Dienst kein Kennwort besitzt.

</dd> <dt>

*LoadOrderGroup* \[ in\]
</dt> <dd>

Der dem neuen Dienst zugeordnete Gruppenname. Lade Reihen folgen Gruppen sind in der Registrierung enthalten und bestimmen die Reihenfolge, in der Dienste in das Betriebssystem geladen werden. Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge verweist, gehört der Dienst nicht zu einer Gruppe. Abhängigkeiten zwischen Gruppen sollten im *loadordergroupdependen-* Parameter aufgeführt werden. Dienste in der Liste der Auslastungs Reihen folgen Gruppen werden zuerst gestartet, gefolgt von Diensten in Gruppen, die sich nicht in der Liste der Auslastungs Reihen folgen Gruppen befinden, gefolgt von Diensten, die nicht zu einer Gruppe gehören. Die Registrierung enthält eine Liste der Lade Auftrags Gruppen unter:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **servicegrouporder**

</dd> <dt>

*Loadordergroupabhängigkeiten* \[ in\]
</dt> <dd>

Array von Gruppen für die Auslastungs Anordnung, die vor diesem Dienst gestartet werden müssen. Jedes Element im Array wird durch **null** getrennt, und die Liste wird durch zwei **null** -Werte beendet. In Visual Basic oder Skript können Sie ein VBArray übergeben. Wenn der Zeiger **null** ist oder auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten. Gruppennamen muss der **SC- \_ Gruppen \_ Bezeichner** (definiert in der Datei "winsvc. h") vorangestellt werden, um ihn von einem Dienstnamen zu unterscheiden, da Dienste und Dienstgruppen denselben Namespace verwenden. Die Abhängigkeit von einer Gruppe bedeutet, dass dieser Dienst ausgeführt werden kann, wenn mindestens ein Mitglied der Gruppe ausgeführt wird, nachdem versucht wurde, alle Mitglieder der Gruppe zu starten.

</dd> <dt>

*Service Abhängigkeiten* \[ in\]
</dt> <dd>

Ein Array, das die Namen von Diensten enthält, die vor dem Start dieses Diensts gestartet werden müssen. Jedes Element im Array wird durch **null** getrennt, und die Liste wird durch zwei **null** -Werte beendet. In Visual Basic oder Skript können Sie ein VBArray übergeben. Wenn der Zeiger **null** ist, oder wenn er auf eine leere Zeichenfolge zeigt, hat der Dienst keine Abhängigkeiten. Die Abhängigkeit von einem Dienst bedeutet, dass dieser Dienst nur ausgeführt werden kann, wenn der Dienst, von dem er abhängt, ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn der Dienst erfolgreich erstellt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und eine andere Zahl, die auf einen Fehler hinweist.

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

[**Win32- \_ System Treiber**](win32-systemdriver.md)
</dt> </dl>

 

