---
title: SystemRestore-Klasse
description: Bietet Methoden zum Deaktivieren und Aktivieren der Überwachung, zum Auflisten verfügbarer Wiederherstellungspunkte und zum Initiieren einer Wiederherstellung auf dem lokalen System.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- System Restore-Systemwiederherstellung
- System Restore Class System Restore, beschrieben
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
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040731"
---
# <a name="systemrestore-class"></a>SystemRestore-Klasse

Bietet Methoden zum Deaktivieren und Aktivieren der Überwachung, zum Auflisten verfügbarer Wiederherstellungspunkte und zum Initiieren einer Wiederherstellung auf dem lokalen System.

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

Die **SystemRestore** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **SystemRestore** -Klasse verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [**CreateRestorePoint**](createrestorepoint-systemrestore.md)     | Erstellt einen Wiederherstellungspunkt.<br/>                         |
| [**Deaktivieren**](disable-systemrestore.md)                           | Deaktiviert die Überwachung auf einem bestimmten Laufwerk.<br/>       |
| [**Aktivieren**](enable-systemrestore.md)                             | Aktiviert die Überwachung auf einem bestimmten Laufwerk.<br/>        |
| [**Getlastrestorestatus**](getlastrestorestatus-systemrestore.md) | Ruft den Status der letzten Systemwiederherstellung ab.<br/> |
| [**Restore**](restore-systemrestore.md)                           | Initiiert eine Systemwiederherstellung.<br/>                      |



 

### <a name="properties"></a>Eigenschaften

Die **SystemRestore** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**CreationTime**
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

Die Beschreibung, die angezeigt werden soll, damit der Benutzer problemlos einen Wiederherstellungspunkt identifizieren kann. Die maximale Länge einer ANSI-Zeichenfolge beträgt Max \_ . Die maximale Länge einer Unicode-Zeichenfolge ist Max \_ \_ . Weitere Informationen finden Sie unter [Wiederherstellungspunkt-Beschreibungs Text](restore-point-description-text.md).

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Art des Ereignisses. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                                           | Bedeutung                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <dt>**Anfang \_ \_System \_ Änderung**</dt> <dt>102</dt> </dl> | Eine Systemänderung wurde begonnen. Bei einem nachfolgenden, nicht aufzurufenden Befehl wird kein neuer Wiederherstellungspunkt erstellt. <br/> Für nachfolgende Aufrufe müssen die Systemänderung am Ende \_ \_ \_ und nicht das Ende der \_ Systemänderung verwendet werden \_ .<br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <dt>**Anfang \_ System \_ Änderung**</dt> <dt>100</dt> </dl>                       | Eine Systemänderung wurde begonnen.<br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <dt>**Ende \_ \_System \_ Änderung**</dt> <dt>103</dt> </dl>       | Eine Systemänderung wurde beendet.<br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <dt>**Ende \_ System \_ Änderung**</dt> <dt>101</dt> </dl>                             | Eine Systemänderung wurde beendet.<br/>                                                                                                                                                           |



 

</dd> <dt>

**Restorepointtype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Typ des Wiederherstellungs Punkts. Dieser Member kann einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                                                          | Bedeutung                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <dt>**Anwendung \_ Installieren**</dt> von <dt>0</dt> </dl>         | Eine Anwendung wurde installiert.<br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <dt>**Anwendung \_ Deinstallieren**</dt> <dt>1</dt> </dl>   | Eine Anwendung wurde deinstalliert.<br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <dt>**Abgebrochen \_ Vorgang**</dt> <dt>13</dt> </dl>        | Eine Anwendung muss den erstellten Wiederherstellungspunkt löschen. Beispielsweise verwendet eine Anwendung dieses Flag, wenn ein Benutzer eine Installation abbricht. <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <dt>**Gerät \_ Treiber \_ Installation**</dt> <dt>10</dt> </dl> | Ein Gerätetreiber wurde installiert.<br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <dt>**Ändern \_ Einstellungen**</dt> <dt>12</dt> </dl>                    | Eine Anwendung verfügt über Features, die hinzugefügt oder entfernt wurden.<br/>                                                                                                  |



 

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Die Sequenznummer des Wiederherstellungs Punkts.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können eine Liste von Wiederherstellungs Punkten abrufen, indem Sie die Methode " [**slibemservices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) " verwenden, um eine Sammlung von **SystemRestore** -Objekten abzurufen. Sie können die Klasseneigenschaften verwenden, um den Wiederherstellungspunkt zu identifizieren.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                         |
| Namespace<br/>                | \\Standardwert<br/>                                                          |
| MOF<br/>                      | <dl> <dt>SR. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Windows-Verwaltungsinstrumentation](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

