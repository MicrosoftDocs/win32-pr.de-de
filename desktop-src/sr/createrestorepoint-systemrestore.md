---
title: Methode "foraterestorepoint" der SystemRestore-Klasse
description: Erstellt einen Wiederherstellungspunkt.
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- Methode zum Wiederherstellen von "foraterestorepoint"
- Methode zum Wiederherstellen der Methode "foraterestorepoint", System Restore-Klasse
- System Restore-Klassen System Wiederherstellung, Methode ' Methode '
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477145"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a>Methode "foraterestorepoint" der SystemRestore-Klasse

Erstellt einen Wiederherstellungspunkt.

Diese Methode ist das Skript fähige Äquivalent der [**srsettrestorepoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) -Funktion.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Beschreibung* \[ in\]
</dt> <dd>

Die Beschreibung, die angezeigt werden soll, damit der Benutzer problemlos einen Wiederherstellungspunkt identifizieren kann. Die maximale Länge einer ANSI-Zeichenfolge beträgt Max \_ . Die maximale Länge einer Unicode-Zeichenfolge ist Max \_ \_ . Weitere Informationen finden Sie unter [Wiederherstellungspunkt-Beschreibungs Text](restore-point-description-text.md).

</dd> <dt>

*Restorepointtype* \[ in\]
</dt> <dd>

Der Typ des Wiederherstellungs Punkts. Dieser Member kann einen der folgenden Werte aufweisen.



| Typ des Wiederherstellungs Punkts                                                                                                                                                                                                                             | Bedeutung                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**Anwendung \_ Installieren**</dt> von <dt>0</dt> </dl>         | Eine Anwendung wurde installiert.<br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**Anwendung \_ Deinstallieren**</dt> <dt>1</dt> </dl>   | Eine Anwendung wurde deinstalliert.<br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**Gerät \_ Treiber \_ Installation**</dt> <dt>10</dt> </dl> | Ein Gerätetreiber wurde installiert.<br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**Ändern \_ Einstellungen**</dt> <dt>12</dt> </dl>                    | Eine Anwendung verfügt über Features, die hinzugefügt oder entfernt wurden.<br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <dt>**Abgebrochen \_ Vorgang**</dt> <dt>13</dt> </dl>        | Eine Anwendung muss den erstellten Wiederherstellungspunkt löschen. Beispielsweise verwendet eine Anwendung dieses Flag, wenn ein Benutzer eine Installation abbricht.<br/> |



 

</dd> <dt>

*EventType* \[ in\]
</dt> <dd>

Art des Ereignisses. Dieser Member kann einen der folgenden Werte aufweisen.



| Ereignistyp                                                                                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**Anfang \_ \_System \_ Änderung**</dt> <dt>102</dt> </dl> | Eine Systemänderung wurde begonnen. Bei einem nachfolgenden, nicht aufzurufenden Befehl wird kein neuer Wiederherstellungspunkt erstellt. <br/> Für nachfolgende Aufrufe müssen die Systemänderung am Ende \_ \_ \_ und nicht das Ende der \_ Systemänderung verwendet werden \_ .<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**Anfang \_ System \_ Änderung**</dt> <dt>100</dt> </dl>                       | Eine Systemänderung wurde begonnen. <br/> Bei einem nachfolgenden-Rückruf muss die Systemänderung am Ende des Systems \_ \_ nicht \_ \_ geändert werden \_ .<br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**Ende \_ \_System \_ Änderung**</dt> <dt>103</dt> </dl>       | Eine Systemänderung wurde beendet.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**Ende \_ System \_ Änderung**</dt> <dt>101</dt> </dl>                             | Eine Systemänderung wurde beendet.<br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Andernfalls gibt die Methode einen der com-Fehlercodes zurück, die in WinError. h definiert sind.

## <a name="remarks"></a>Bemerkungen

* * Windows 8: * *

Ein neuer Registrierungsschlüssel ermöglicht Anwendungsentwicklern das Ändern der Häufigkeit der Wiederherstellungspunkt Erstellung.

Anwendungen sollten diesen Schlüssel erstellen, um ihn zu verwenden, da er im System nicht bereits vorhanden ist. Wenn der Schlüssel nicht vorhanden ist, wird standardmäßig Folgendes angewendet: Wenn eine Anwendung die Methode "Methode zum Erstellen eines Wiederherstellungs Punkts" aufruft, überspringt **Windows das Erstellen** dieses neuen Wiederherstellungs Punkts, wenn in den letzten 24 Stunden Wiederherstellungspunkte erstellt wurden. Die Methode " **kreaterestorepoint** " gibt " **S \_ OK**" zurück.

Entwickler können Anwendungen schreiben, die den **DWORD** -Wert **systemrestorepointkreationfrequency** unter dem Registrierungsschlüssel **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore** erstellen. Mit dem Wert dieses Registrierungsschlüssels kann die Häufigkeit der Wiederherstellungspunkt Erstellung geändert werden. Mit dem Wert dieses Registrierungsschlüssels kann die Häufigkeit der Wiederherstellungspunkt Erstellung geändert werden.

Wenn die Anwendung "" zum Erstellen eines Wiederherstellungs Punkts "" mit dem Wert "" auf " **", und** der Wert des Registrierungsschlüssels "0" aufruft, wird die Erstellung des neuen Wiederherstellungs Punkts nicht überspringt.

Wenn die Anwendung "" zum Erstellen eines Wiederherstellungs Punkts mit "" "" "" "" "," "und der Registrierungsschlüssel Wert" N "ist, überspringt die Systemwiederherstellung die Erstellung eines neuen Wiederherstellungs **Punkts, wenn** in den letzten N Minuten Wiederherstellungspunkte erstellt wurden

## <a name="examples"></a>Beispiele


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                         |
| Namespace<br/>                | \\Standardwert<br/>                                                          |
| MOF<br/>                      | <dl> <dt>SR. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





