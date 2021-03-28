---
description: Ermöglicht es einem Administrator, die Datenträger Kontingent Eigenschaften eines Volumes zu verwalten.
title: Diskquotacontrol-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 843f33ee79e70309a47f170bb1935f94f45c8f2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994902"
---
# <a name="diskquotacontrol-object"></a>Diskquotacontrol-Objekt

Ermöglicht es einem Administrator, die Datenträger Kontingent Eigenschaften eines Volumes zu verwalten. Das NTFS-Dateisystem ermöglicht einem Administrator, die Datenträger Verwendung auf einem freigegebenen Volume zu verwalten, indem jedem Benutzer eine angegebene Menge an Speicherplatz oder *Kontingent Limit* zugewiesen wird. Mit diesem Objekt können Sie die Standard Kontingent Grenze festlegen, die automatisch allen neuen Benutzern zugewiesen wird.

## <a name="members"></a>Member

Das **diskquotacontrol** -Objekt verfügt über folgende Typen von Membern:

-   [Ereignisse](#events)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Das **diskquotacontrol** -Objekt enthält diese Ereignisse.



| Ereignis                                                           | BESCHREIBUNG                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**Onusernamechanged**](diskquotacontrol-onusernamechanged.md) | Tritt auf, wenn die Namensinformationen für ein [**didiskquotauser**](didiskquotauser-object.md) -Objekt aufgelöst wurden.<br/> |



 

### <a name="methods"></a>Methoden

Das **diskquotacontrol** -Objekt verfügt über diese Methoden.



| Methode                                                                                    | BESCHREIBUNG                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**AddUser**](diskquotacontrol-adduser.md)                                               | Weist einem neuen Benutzer ein nicht standardmäßiges Datenträger Kontingent zu.<br/>                                  |
| [**DeleteUser**](diskquotacontrol-deleteuser.md)                                         | Löscht einen Benutzer aus dem Volume.<br/>                                                 |
| [**FINDUSER**](diskquotacontrol-finduser.md)                                             | Sucht den Eintrag eines Benutzers anhand des Namens in der Kontingent Datei des Volumes.<br/>                      |
| [**Giveusernameresolutionpriority**](diskquotacontrol-giveusernameresolutionpriority.md) | Platziert das angegebene Benutzerobjekt für die Namensauflösung in der nächsten Zeile.<br/>              |
| [**Initialisieren**](diskquotacontrol-initialize.md)                                         | Öffnet ein angegebenes Volume und initialisiert dessen Kontingent Steuerungsobjekt.<br/>              |
| [**Invalidatesidnamecache**](diskquotacontrol-invalidatesidnamecache.md)                 | Macht den Benutzernamen Cache für die Sicherheits-ID ungültig.<br/>                                    |
| [**Shutdownnameresolution**](diskquotacontrol-shutdownnameresolution.md)                 | Fährt den Thread für die Auflösung von Benutzernamen herunter.<br/>                                     |
| [**Translatelogonnametosid**](diskquotacontrol-translatelogonnametosid.md)               | Übersetzt einen Anmelde Namen in die entsprechende Benutzersicherheits-ID im Zeichen folgen Format.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **diskquotacontrol** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Defaultquotalimit**](diskquotacontrol-defaultquotalimit.md)<br/>                 | Lesen/Schreiben<br/> | Legt die Standard Kontingent Grenze fest oder ruft Sie ab.<br/>                                                                                                              |
| [**Defaultquotalimittext**](diskquotacontrol-defaultquotalimittext.md)<br/>         | Schreibgeschützt<br/>  | Ruft die Standard Kontingent Grenze als Text Zeichenfolge ab.<br/>                                                                                                     |
| [**Defaultquotathreshold**](diskquotacontrol-defaultquotathreshold.md)<br/>         | Lesen/Schreiben<br/> | Legt den Standard Kontingent Schwellenwert fest oder ruft ihn ab.<br/>                                                                                                          |
| [**Defaultquotader OLDTEXT**](diskquotacontrol-defaultquotathresholdtext.md)<br/> | Schreibgeschützt<br/>  | Ruft den Standard Kontingent Schwellenwert als Text Zeichenfolge ab.<br/>                                                                                                 |
| [**Logquotalimit**](diskquotacontrol-logquotalimit.md)<br/>                         | Lesen/Schreiben<br/> | Legt einen booleschen Wert fest, der angibt, ob ein Eintrag des System Ereignis Protokolls durchgeführt wird, wenn ein Benutzer sein zugewiesenes Kontingent Limit überschreitet, oder ruft ihn ab.<br/>     |
| [**Logquotathreshold**](diskquotacontrol-logquotathreshold.md)<br/>                 | Lesen/Schreiben<br/> | Legt einen booleschen Wert fest, der angibt, ob ein System Ereignisprotokoll-Eintrag erfolgt, wenn ein Benutzer seinen zugewiesenen Kontingent Schwellenwert überschreitet, oder ruft diesen booleschen Wert ab.<br/> |
| [**Quotafilinput Complete**](diskquotacontrol-quotafileincomplete.md)<br/>             | Schreibgeschützt<br/>  | Ruft einen booleschen Wert ab, der angibt, ob die Kontingent Datei für das Volume fertig ist.<br/>                                                             |
| [**Quotafilerebuilding**](diskquotacontrol-quotafilerebuilding.md)<br/>             | Schreibgeschützt<br/>  | Ruft einen booleschen Wert ab, der angibt, ob die Kontingent Datei für das Volume gerade neu erstellt wird.<br/>                                              |
| [**Quotastate**](diskquotacontrol-quotastate.md)<br/>                               | Lesen/Schreiben<br/> | Legt den Status der Datenträger Kontingente des Volumes fest oder ruft ihn ab.<br/>                                                                                                |
| [**Usernameresolution**](diskquotacontrol-usernameresolution.md)<br/>               | Lesen/Schreiben<br/> | Legt einen Wert fest, der steuert, wie Benutzer-SID in Benutzernamen aufgelöst wird, oder ruft diesen ab.<br/>                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Ein Administrator kann das **diskquotacontrol** -Objekt verwenden, um eine Reihe von Aufgaben auszuführen, einschließlich der folgenden:

-   Aktivieren und Deaktivieren des Datenträger Kontingent Systems für das Volume.
-   Abrufen des Status des Kontingent Systems auf dem Volume.
-   Verweigern von Speicherplatz für Benutzer, die ihre Kontingent Grenze überschreiten.
-   Angeben der Standardwerte für Warnungs Schwellenwert und Kontingent Grenze, die neuen Benutzern zugewiesen werden.
-   Hinzufügen und Entfernen von Benutzern.

Das **diskquotacontrol** -Objekt ermöglicht es Ihnen, globale Standardwerte für das Volume für Eigenschaften wie Kontingent Limits festzulegen. Jeder Benutzer wird jedoch durch ein [**didiskquotauser**](didiskquotauser-object.md) -Objekt dargestellt, das zum angeben einzelner Kontingent Einstellungen verwendet werden kann.

Es gibt mehrere Möglichkeiten, das [**didiskquotauser**](didiskquotauser-object.md) -Objekt eines Benutzers zu erhalten:

-   Die [**didiskquotauser**](didiskquotauser-object.md) -Objekte für alle Benutzer mit Kontingenten auf dem Volume werden als Sammlung verfügbar gemacht und können aufgezählt werden. Eine Erläuterung zum Auflisten von " **didiskquotauser** "-Objekten finden Sie unter Auflisten von Datenträger **Kontingenten für Benutzer** im Abschnitt "Hinweise" von " **didiskquotauser**".
-   Wenn Sie einen neuen Benutzer hinzufügen, gibt die [**adduser**](diskquotacontrol-adduser.md) -Methode das [**didiskquotauser**](didiskquotauser-object.md) -Objekt des Benutzers zurück.
-   Wenn Sie den Namen des Benutzers haben, gibt die [**FINDUSER**](diskquotacontrol-finduser.md) -Methode das [**didiskquotauser**](didiskquotauser-object.md) -Objekt des Benutzers zurück.

Dieses Objekt stellt die grundlegenden Funktionen der idiskquotacontrol-Schnittstelle für Skripterstellung und Microsoft Visual Basic basierten Anwendungen zur Verfügung.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Shellobjekt**](shell.md)
</dt> </dl>

 

 




