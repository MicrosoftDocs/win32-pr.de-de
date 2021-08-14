---
title: Registrierungseinträge für die Bibliothekklassifizierung
description: Registrierungseinträge für die Bibliothekklassifizierung
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Windows Media Player,Bibliothek
- Windows Media Player,Klassifizierungsregistrierungseinträge
- Windows Media Player,Dateierweiterungen
- Windows Media Player,Registrierung
- Registrierung, Dateinamenerweiterungen
- Registrierung, Bibliotheksklassifizierungseinträge
- registry,settings for Windows Media Player
- Registrierungseinstellungen der Dateinamenerweiterung
- Library,Klassifizierungsregistrierungseinträge
- Bibliothek, Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cb263732dc8071d603c5acd62db25fc8ee887c35b28d109d961a63aba80d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575130"
---
# <a name="library-classification-registry-entries"></a>Registrierungseinträge für die Bibliothekklassifizierung

Wenn Windows Media Player eine Mediendatei mit einer benutzerdefinierten Dateierweiterung findet, weiß sie nicht, ob die Datei als Audio, Video oder einen anderen Typ klassifiziert werden soll. Standardmäßig werden Windows Media Player Dateien im Abschnitt Andere Medien der Bibliothek platziert.

Wenn Ihre digitalen Mediendateien ein benutzerdefiniertes Format haben, können Sie Windows Media Player Informationen dazu bereitstellen, wo Ihre Dateien in der Bibliothek des Players angezeigt werden sollen, indem Sie zwei Einträge in der Registrierung auf dem Computer des Benutzers platzieren.

Ein Eintrag wird im folgenden Unterschlüssel verwendet.

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**

Der Registrierungseintrag hat das folgende Format.



| Name                                                  | Datentyp   | Wert                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| Die Dateierweiterung ohne Punkttrennzeichen (.) | **REG \_ SZ** | Eine Zeichenfolge, die einen Bibliotheksspeicherort angibt. |



 

Der andere Registrierungseintrag wird im folgenden Unterschlüssel gespeichert, den Sie erstellen.

**HKEY \_ CLASSES \_ \\ ROOT** *customExtension*

dabei *ist customExtension* die Dateierweiterung, einschließlich des Punkttrennzeichens (.).

Der Registrierungseintrag hat das folgende Format.



| Name          | Datentyp   | Wert                                      |
|---------------|-------------|--------------------------------------------|
| PerceivedType | **REG \_ SZ** | Eine Zeichenfolge, die einen Bibliotheksspeicherort angibt. |



 

Beide Registrierungseinträge müssen denselben Wert haben. Mögliche Werte sind in der folgenden Tabelle angegeben.



| Wert | Beschreibung                                                                      |
|-------|----------------------------------------------------------------------------------|
| Audio | Dateien mit der benutzerdefinierten Erweiterung werden im Musikteil der Bibliothek angezeigt. |
| video | Dateien mit der benutzerdefinierten Erweiterung werden im Videoteil der Bibliothek angezeigt. |



 

Die folgenden Registrierungseinträge geben beispielsweise an, dass Dateien mit der Dateinamenerweiterung .xyz im Musikteil der Bibliothek angezeigt werden:


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



Beachten Sie, dass jeder Code, der versucht, in die Registrierung auf dem Computer des Benutzers zu schreiben, nur dann in die HKEY LOCAL MACHINE-Unterstruktur schreiben kann, wenn der aktuelle Benutzer über \_ \_ Administratorrechte verfügt.

Registrierungseinträge für die Bibliothekklassifizierung werden von den folgenden Versionen von Windows Media Player.

-   Windows Media Player 9-Serie mit Hotfix 823275
-   Windows Media Player 10 und höher

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierung der Dateinamenerweiterung Einstellungen**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




