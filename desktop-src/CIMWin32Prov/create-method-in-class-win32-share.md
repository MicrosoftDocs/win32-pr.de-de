---
description: Initiiert die Freigabe für eine Server Ressource.
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Create-Methode der Win32_Share-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7a74838d9f6c532d3433240a5b8a70846b63776
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958623"
---
# <a name="create-method-of-the-win32_share-class"></a>Create-Methode der Win32- \_ Freigabe Klasse

Die Methode **Create**   [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) initiiert die Freigabe für eine Server Ressource.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfad* \[ in\]
</dt> <dd>

Lokaler Pfad der Windows-Freigabe.

Beispiel: "C: \\ Program Files".

</dd> <dt>

*Name* \[ in\]
</dt> <dd>

Übergibt den Alias an einen Pfad, der auf einem Computersystem, auf dem Windows ausgeführt wird, als Freigabe eingerichtet ist.

Beispiel: "Public".

</dd> <dt>

*Typ* \[ in\]
</dt> <dd>

Übergibt den Typ der freigegebenen Ressource. Zu den Typen zählen Laufwerke, Druck Warteschlangen, prozessübergreifende Kommunikation (prozessübergreifende Communications, IPC) und allgemeine Geräte. Kann einen der folgenden Werte aufweisen.

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Laufwerk (0** )


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**Druck Warteschlange** (1)


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**Gerät** (2)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3)


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**Laufwerks Administrator** (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Administrator der Druck Warteschlange** (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Geräte Administrator** (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**IPC admin** (2147483651)


</dt> <dd></dd> </dl> </dd> <dt>

*MaximumAllowed* \[ in, optional\]
</dt> <dd>

Limit für die maximale Anzahl von Benutzern, die gleichzeitig diese Ressource verwenden dürfen.

Beispiel: 10. Dieser Parameter ist optional.

</dd> <dt>

*Beschreibung* \[ in, optional\]
</dt> <dd>

Optionaler Kommentar zum Beschreiben der freigegebenen Ressource. Dieser Parameter ist optional.

</dd> <dt>

*Kennwort* \[ in, optional\]
</dt> <dd>

Kennwort (bei Ausführung des Servers mit Sicherheit auf Freigabe Ebene) für die freigegebene Ressource. Wenn der Server mit Sicherheit auf Benutzerebene ausgeführt wird, wird dieser Parameter ignoriert. Dieser Parameter ist optional.

</dd> <dt>

*Zugriff* \[ in, optional\]
</dt> <dd>

Sicherheits Beschreibung für Berechtigungen auf Benutzerebene. Eine Sicherheits Beschreibung enthält Informationen über die Berechtigungen, den Besitzer und die Zugriffs Funktionen der Ressource. Wenn dieser Parameter nicht angegeben wird oder den Wert **null** aufweist, verfügt jeder über Lesezugriff auf die Freigabe. Weitere Informationen finden Sie unter [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der in der folgenden Liste aufgeführten Werte oder einen anderen Wert zurück, um einen Fehler anzugeben. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Zugriff verweigert** (2)
</dt> <dt>

**Unbekannter Fehler** (8)
</dt> <dt>

**Ungültiger Name** (9)
</dt> <dt>

**Ungültige Ebene** (10)
</dt> <dt>

**Ungültiger Parameter** (21)
</dt> <dt>

**Doppelte Freigabe** (22)
</dt> <dt>

**Umgeleiteter Pfad** (23)
</dt> <dt>

**Unbekanntes Gerät oder Verzeichnis** (24)
</dt> <dt>

Der **Netzwerkname wurde nicht gefunden** (25).
</dt> <dt>

**Sonstige** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

**Create** ist eine statische Methode.

Nur Mitglieder der lokalen Gruppe "Administratoren" oder "Konto-Operatoren" oder die Gruppenmitgliedschaften "Kommunikation", "Drucken" oder "Server Operator" können " **Create**" Der Druck Operator kann nur Drucker Warteschlangen hinzufügen. Der Kommunikations Operator kann nur Kommunikationsgeräte Warteschlangen hinzufügen.

## <a name="examples"></a>Beispiele

Das PowerShell-Beispiel [exportieren und Importieren von Fileshares](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) exportiert und importiert Dateifreigaben und legt Freigabe Berechtigungen fest. Entsprechend erstellt das Beispiel [Create a share und Set-Berechtigungen](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) auch eine neue Freigabe und legt die Freigabe Berechtigungen fest.

Mit dem folgenden PowerShell-Code wird eine Freigabe erstellt.


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



Im vorherigen Codebeispiel wird Folgendes zurückgegeben:

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

Im folgenden C- \# Codebeispiel wird beschrieben, wie die Create-Methode aufgerufen wird.


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
```



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

[**Win32- \_ Freigabe**](win32-share.md)
</dt> </dl>

 

