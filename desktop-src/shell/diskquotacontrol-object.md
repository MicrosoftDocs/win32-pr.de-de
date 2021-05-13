---
description: Ermöglicht es einem Administrator, die Datenträgerkontingenteigenschaften eines Volumes zu verwalten.
title: DiskQuotaControl-Objekt
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
ms.openlocfilehash: 5f7b1d700c73df56ce7aaef39e162517629f96f6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841551"
---
# <a name="diskquotacontrol-object"></a>DiskQuotaControl-Objekt

Ermöglicht es einem Administrator, die Datenträgerkontingenteigenschaften eines Volumes zu verwalten. Mit dem NTFS-Dateisystem kann ein Administrator die Datenträgernutzung auf einem freigegebenen Volume verwalten, indem jedem Benutzer eine bestimmte Menge an Speicherplatz oder eine Kontingentgrenze zuteil wird. Mit diesem Objekt können Sie die Standardkontingentgrenze festlegen, die allen neuen Benutzern automatisch zugewiesen wird.

## <a name="members"></a>Member

Das **DiskQuotaControl-Objekt** verfügt über die folgenden Membertypen:

-   [Ereignisse](#events)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Das **DiskQuotaControl-Objekt** verfügt über diese Ereignisse.



| Ereignis                                                           | BESCHREIBUNG                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) | Tritt ein, wenn die Namensinformationen für ein [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) aufgelöst wurden.<br/> |



 

### <a name="methods"></a>Methoden

Das **DiskQuotaControl-Objekt** verfügt über diese Methoden.



| Methode                                                                                    | BESCHREIBUNG                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**AddUser**](diskquotacontrol-adduser.md)                                               | Weist einem neuen Benutzer ein nicht standardmäßiges Datenträgerkontingent zu.<br/>                                  |
| [**DeleteUser**](diskquotacontrol-deleteuser.md)                                         | Löscht einen Benutzer aus dem Volume.<br/>                                                 |
| [**FindUser**](diskquotacontrol-finduser.md)                                             | Sucht den Eintrag eines Benutzers nach Namen in der Kontingentdatei des Volumes.<br/>                      |
| [**GiveUserNameResolutionPriority**](diskquotacontrol-giveusernameresolutionpriority.md) | Platziert das angegebene Benutzerobjekt als Nächstes in der Zeile für die Namensauflösung.<br/>              |
| [**Initialisieren**](diskquotacontrol-initialize.md)                                         | Öffnet ein angegebenes Volume und initialisiert das Kontingentsteuerobjekt.<br/>              |
| [**InvalidateSidNameCache**](diskquotacontrol-invalidatesidnamecache.md)                 | Erklärt den Benutzernamencache der Sicherheits-ID für ungültig.<br/>                                    |
| [**ShutdownNameResolution**](diskquotacontrol-shutdownnameresolution.md)                 | Fährt den Thread für die Auflösung des Benutzernamens herunter.<br/>                                     |
| [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md)               | Übersetzt einen Anmeldenamen in die entsprechende Benutzersicherheits-ID im Zeichenfolgenformat.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **DiskQuotaControl-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                   | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)<br/>                 | Lesen/Schreiben<br/> | Legt das Standardkontingentlimit fest oder ruft es ab.<br/>                                                                                                              |
| [**DefaultQuotaLimitText**](diskquotacontrol-defaultquotalimittext.md)<br/>         | Schreibgeschützt<br/>  | Ruft die Standardkontingentgrenze als Textzeichenfolge ab.<br/>                                                                                                     |
| [**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)<br/>         | Lesen/Schreiben<br/> | Legt den Standardkontingentschwellenwert fest oder ruft sie ab.<br/>                                                                                                          |
| [**DefaultQuotaThresholdText**](diskquotacontrol-defaultquotathresholdtext.md)<br/> | Schreibgeschützt<br/>  | Ruft den Standardkontingentschwellenwert als Textzeichenfolge ab.<br/>                                                                                                 |
| [**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)<br/>                         | Lesen/Schreiben<br/> | Legt einen booleschen Wert fest oder ruft einen booleschen Wert ab, der angibt, ob ein Systemereignisprotokolleintrag erfolgt, wenn ein Benutzer sein zugewiesenes Kontingentlimit überschreitet.<br/>     |
| [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)<br/>                 | Lesen/Schreiben<br/> | Legt einen booleschen Wert fest oder ruft einen booleschen Wert ab, der angibt, ob ein Systemereignisprotokolleintrag erfolgt, wenn ein Benutzer seinen zugewiesenen Kontingentschwellenwert überschreitet.<br/> |
| [**QuotaFileIncomplete**](diskquotacontrol-quotafileincomplete.md)<br/>             | Schreibgeschützt<br/>  | Ruft einen booleschen Wert ab, der angibt, ob die Kontingentdatei für das Volume abgeschlossen ist.<br/>                                                             |
| [**QuotaFileRe building**](diskquotacontrol-quotafilerebuilding.md)<br/>             | Schreibgeschützt<br/>  | Ruft einen booleschen Wert ab, der angibt, ob die Kontingentdatei für das Volume gerade neu erstellt wird.<br/>                                              |
| [**QuotaState**](diskquotacontrol-quotastate.md)<br/>                               | Lesen/Schreiben<br/> | Legt den Status der Datenträgerkontingente des Volumes fest oder ruft sie ab.<br/>                                                                                                |
| [**UserNameResolution**](diskquotacontrol-usernameresolution.md)<br/>               | Lesen/Schreiben<br/> | Legt einen Wert fest, der steuert, wie die Benutzer-SID in Benutzernamen aufgelöst wird, oder ruft diesen ab.<br/>                                                                        |



 

## <a name="remarks"></a>Hinweise

Ein Administrator kann das **DiskQuotaControl-Objekt** verwenden, um eine Reihe von Aufgaben auszuführen, einschließlich der folgenden:

-   Aktivieren und Deaktivieren des Datenträgerkontingentsystems des Volumes.
-   Abrufen des Status des Kontingentsystems auf dem Volume.
-   Verweigern von Speicherplatz für Benutzer, die ihre Kontingentgrenze überschreiten.
-   Angeben der Standardwerte für Warnungsschwellenwert und Kontingentgrenzwert, die neuen Benutzern zugewiesen werden.
-   Hinzufügen und Entfernen von Benutzern.

Mit **dem DiskQuotaControl-Objekt** können Sie globale Standardwerte für das Volume für Eigenschaften wie Kontingentgrenzen festlegen. Jeder Benutzer wird jedoch durch ein [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) dargestellt, das zum Angeben einzelner Kontingenteinstellungen verwendet werden kann.

Es gibt mehrere Möglichkeiten, das [**DIDiskQuotaUser-Objekt**](didiskquotauser-object.md) eines Benutzers zu erhalten:

-   Die [**DIDiskQuotaUser-Objekte**](didiskquotauser-object.md) für alle Benutzer mit Kontingenten auf dem Volume werden als Sammlung verfügbar gemacht und können aufzählt werden. Eine Erläuterung zum Aufzählen von **DIDiskQuotaUser-Objekten** finden Sie unter **Aufzählen** von Datenträgerkontingentbenutzern im Abschnitt "Hinweise" von **DIDiskQuotaUser**.
-   Wenn Sie einen neuen Benutzer hinzufügen, gibt die [**AddUser-Methode**](diskquotacontrol-adduser.md) das [**DIDiskQuotaUser-Objekt des Benutzers**](didiskquotauser-object.md) zurück.
-   Wenn Sie über den Namen des Benutzers verfügen, gibt die [**FindUser-Methode**](diskquotacontrol-finduser.md) das [**DIDiskQuotaUser-Objekt des Benutzers**](didiskquotauser-object.md) zurück.

Dieses Objekt macht die grundlegenden Funktionen der IDiskQuotaControl-Schnittstelle für Skripts und Microsoft Visual Basic-basierten Anwendungen verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Shell-Objekt**](shell.md)
</dt> </dl>

 

 




