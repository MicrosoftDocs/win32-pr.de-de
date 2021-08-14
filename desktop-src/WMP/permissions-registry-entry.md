---
title: Registrierungseintrag "Berechtigungen"
description: Registrierungseintrag "Berechtigungen"
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player,Dateierweiterungen
- Windows Media Player,Berechtigungen
- Windows Media Player,Registrierung
- Registrierung, Dateinamenerweiterungen
- Registrierung,Berechtigungen
- registry,settings for Windows Media Player
- Registrierungseinstellungen der Dateinamenerweiterung
- Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5feaae3ebf55359f664e40df26b52912d727446ad715cd552d92cc1d090ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747737"
---
# <a name="permissions-registry-entry"></a>Registrierungseintrag "Berechtigungen"

Wenn Windows Media Player eine benutzerdefinierte Dateinamenerweiterung findet, sucht sie nach einem Registrierungsunterschlüssel, der der Erweiterung entspricht. Der Unterschlüssel wird unter [Dateinamenerweiterungsregistrierung Einstellungen.](file-name-extension-registry-settings.md) Einer der Registrierungseinträge, die unter dem Unterschlüssel der Erweiterung angezeigt werden können, ist der **Eintrag Berechtigungen.**

Der **Eintrag Berechtigungen** gibt die Aktionen an, Windows Media Player für Dateien mit der benutzerdefinierten Erweiterung ausführen dürfen. Der **Eintrag** Berechtigungen hat das folgende Formular.



| Name        | type           | Wert                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| Berechtigungen | **REG \_ DWORD** | Ein Satz von Flags, von denen jedes die Berechtigung für eine bestimmte Aktion erteilt. |



 

Der Wert des **Berechtigungseintrags** ist ein bitweises **OR** eines oder mehrere der folgenden Flags.



| Flag (Dezimalwert) | BESCHREIBUNG                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1                    | Berechtigung für die Wiedergabe. Dateien mit der registrierten Dateinamenerweiterung können abgespielt werden.                                                                                                                                                                                       |
| 2                    | Berechtigung zum Löschen von Ordnern. Dateien mit der registrierten Dateinamenerweiterung werden in die Wiedergabeliste aufgenommen, die erstellt wird, wenn der Benutzer einen Ordner mit den Dateien zieht und auf der Benutzeroberfläche des Players abstürzt.                                                      |
| 4                    | Berechtigung für Medien-CD. Dateien mit der registrierten Dateinamenerweiterung werden in die Wiedergabeliste aufgenommen, die erstellt wird, wenn eine CD mit den Dateien in das CD-ROM-Laufwerk eingefügt wird.                                                                                           |
| 8                    | Berechtigung für die Bibliothek. Dateien mit der registrierten Dateinamenerweiterung können der Bibliothek hinzugefügt werden. Erforderlich für Konvertierungs-Plug-Ins.                                                                                                                                    |
| 16                   | Berechtigung für HTML-Streaming. Dateien mit der registrierten Dateinamenerweiterung werden in den Internet Explorer zwischengespeichert, wenn sie von einem Webstream übermittelt werden.                                                                                                            |
| 128                  | Berechtigung für die Transcodierung. Dateien mit der registrierten Dateinamenerweiterung können unter bestimmten Bedingungen in Windows Medienformat transcodiert werden. Siehe [IWMPTranscodePolicy::allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode). Erfordert Windows Media Player 10 oder höher. |



 

Wenn der Benutzer versucht, eine Mediendatei mit einer benutzerdefinierten Dateierweiterung wieder zu verwenden, sucht Windows Media Player nach einem Registrierungsunterschlüssel, der der Erweiterung entspricht. Wenn keine Übereinstimmung gefunden wird, zeigt der Player dem Benutzer ein Warndialogfeld an, in dem der Benutzer aufgefordert wird, die Berechtigung zum Wieder geben der Datei zu erteilen. Wenn Sie digitale Mediendateien mit benutzerdefinierten Dateierweiterungen erstellen, können Sie verhindern, dass diese Warnung auf dem Computer des Benutzers angezeigt wird, indem Sie die Dateierweiterung registrieren und einen **Berechtigungseintrag** angeben.

Der **Berechtigungseintrag** (mit Ausnahme des Flagwerts 128) wird von Windows Media Player 9-Serie und höher unterstützt. Der Flagwert 128 wird von Windows Media Player 10 und höher unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Dateinamenerweiterungsregistrierungs-Einstellungen**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




