---
title: SystemRestore-Klasse
description: Stellt Methoden zum Deaktivieren und Aktivieren der Überwachung, zum Auflisten verfügbarer Wiederherstellungspunkte und zum Initiieren einer Wiederherstellung auf dem lokalen System bereit.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- SystemRestore-Klasse System Restore
- SystemRestore-Klasse Systemwiederherstellung , beschrieben
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca781f960f51c8f7804d56f3b2f5531517c3f16505f40dd48d442857fa58bf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967989"
---
# <a name="systemrestore-class"></a>SystemRestore-Klasse

Stellt Methoden zum Deaktivieren und Aktivieren der Überwachung, zum Auflisten verfügbarer Wiederherstellungspunkte und zum Initiieren einer Wiederherstellung auf dem lokalen System bereit.

## <a name="syntax"></a>Syntax

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a>Member

Die **SystemRestore-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **SystemRestore-Klasse** verfügt über diese Methoden.



| Methode                                                             | Beschreibung                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [**CreateRestorePoint**](createrestorepoint-systemrestore.md)     | Erstellt einen Wiederherstellungspunkt.<br/>                         |
| [**Deaktivieren**](disable-systemrestore.md)                           | Deaktiviert die Überwachung auf einem bestimmten Laufwerk.<br/>       |
| [**Aktivieren**](enable-systemrestore.md)                             | Ermöglicht die Überwachung auf einem bestimmten Laufwerk.<br/>        |
| [**GetLastRestoreStatus**](getlastrestorestatus-systemrestore.md) | Ruft den Status der letzten Systemwiederherstellung ab.<br/> |
| [**Restore**](restore-systemrestore.md)                           | Initiiert eine Systemwiederherstellung.<br/>                      |



 

### <a name="properties"></a>Eigenschaften

Die **SystemRestore-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Creationtime**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Zeitpunkt, zu dem die Zustandsänderung aufgetreten ist.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Beschreibung, die angezeigt werden soll, damit der Benutzer einen Wiederherstellungspunkt leicht identifizieren kann. Die maximale Länge einer ANSI-Zeichenfolge ist MAX \_ DESC. Die maximale Länge einer Unicode-Zeichenfolge ist MAX \_ DESC \_ W. Weitere Informationen finden Sie unter [Wiederherstellungspunktbeschreibungstext.](restore-point-description-text.md)

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Art des Ereignisses. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**BEGIN \_ GESCHACHTELTE \_ \_ SYSTEMÄNDERUNG**</dt> <dt>102</dt> </dl> | Eine Systemänderung wurde gestartet. Ein nachfolgender geschachtelter Aufruf erstellt keinen neuen Wiederherstellungspunkt. <br/> Nachfolgende Aufrufe müssen END \_ NESTED \_ SYSTEM CHANGE und nicht END SYSTEM CHANGE \_ \_ \_ verwenden.<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**BEGIN \_ SYSTEM \_ CHANGE**</dt> <dt>100</dt> </dl>                       | Eine Systemänderung wurde gestartet.<br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**END \_ NESTED \_ SYSTEM \_ CHANGE**</dt> <dt>103</dt> </dl>       | Eine Systemänderung wurde beendet.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**END \_ SYSTEM \_ CHANGE**</dt> <dt>101</dt> </dl>                             | Eine Systemänderung wurde beendet.<br/>                                                                                                                                                           |



 

</dd> <dt>

**RestorePointType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Typ des Wiederherstellungspunkts. Dieser Member kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**ANWENDUNG \_ INSTALL**</dt> <dt>0</dt> </dl>         | Eine Anwendung wurde installiert.<br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**ANWENDUNG \_ DEINSTALLIEREN 1**</dt> <dt></dt> </dl>   | Eine Anwendung wurde deinstalliert.<br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <dt>**CANCELLED \_ VORGANG**</dt> <dt>13</dt> </dl>        | Eine Anwendung muss den erstellten Wiederherstellungspunkt löschen. Beispielsweise würde eine Anwendung dieses Flag verwenden, wenn ein Benutzer eine Installation abbricht. <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**GERÄT \_ \_TREIBERINSTALLATION**</dt> <dt>10</dt> </dl> | Ein Gerätetreiber wurde installiert.<br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**MODIFY \_ EINSTELLUNGEN**</dt> <dt>12</dt> </dl>                    | Einer Anwendung wurden Features hinzugefügt oder entfernt.<br/>                                                                                                  |



 

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Die Sequenznummer des Wiederherstellungspunkts.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können eine Liste der Wiederherstellungspunkte abrufen, indem Sie die [**SWbemServices.InstancesOf-Methode**](/windows/desktop/WmiSdk/swbemservices-instancesof) verwenden, um eine Sammlung von **SystemRestore-Objekten** abzurufen. Sie können die Klasseneigenschaften verwenden, um den Wiederherstellungspunkt zu identifizieren.

## <a name="examples"></a>Beispiele

Das folgende Beispielskript listet die aktuellen Wiederherstellungspunkte auf.


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                         |
| Namespace<br/>                | \\Stammstandard<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Windows-Verwaltungsinstrumentation](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

