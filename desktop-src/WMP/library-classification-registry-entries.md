---
title: Registrierungseinträge für die Bibliotheks Klassifizierung
description: Registrierungseinträge für die Bibliotheks Klassifizierung
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Windows-Media Player, Bibliothek
- Windows Media Player, Klassifizierungs Registrierungseinträge
- Windows Media Player, Dateinamen Erweiterungen
- Windows Media Player, Registrierung
- Registrierung, Dateinamen Erweiterungen
- Registrierung, Bibliotheks Klassifizierungs Einträge
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Dateinamenerweiterung
- Bibliothek, Klassifizierungs Registrierungseinträge
- Bibliothek, Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342070"
---
# <a name="library-classification-registry-entries"></a>Registrierungseinträge für die Bibliotheks Klassifizierung

Wenn Windows Media Player auf eine Mediendatei mit einer benutzerdefinierten Dateierweiterung stößt, ist nicht bekannt, ob die Datei als Audiodatei, Video oder ein anderer Typ klassifiziert werden soll. Standardmäßig platziert Windows Media Player diese Dateien in den anderen Medienbereich der Bibliothek.

Wenn Ihre digitalen Mediendateien ein benutzerdefiniertes Format aufweisen, können Sie Windows Media Player Informationen darüber bereitstellen, wo Ihre Dateien in der Bibliothek des Players angezeigt werden sollen, indem Sie zwei Einträge in der Registrierung auf dem Computer des Benutzers platzieren.

Ein Eintrag wird in den folgenden Unterschlüssel geleitet.

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Media Player \\ MLS \\ Extensions**

Der Registrierungs Eintrag weist das folgende Format auf.



| Name                                                  | Datentyp   | Wert                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| Die Dateinamenerweiterung ohne das Punkt Trennzeichen (.) | **REG- \_ SZ** | Eine Zeichenfolge, die einen Bibliotheks Speicherort angibt. |



 

Der andere Registrierungs Eintrag ist der folgende Unterschlüssel, den Sie erstellen.

**HKEY \_ Klassen Stamm-CustomExtension \_ \\** 

Dabei ist *CustomExtension* die Dateinamenerweiterung, einschließlich des Punkt Trennzeichens (.).

Der Registrierungs Eintrag weist das folgende Format auf.



| Name          | Datentyp   | Wert                                      |
|---------------|-------------|--------------------------------------------|
| Wahrnehmungstyp | **REG- \_ SZ** | Eine Zeichenfolge, die einen Bibliotheks Speicherort angibt. |



 

Beide Registrierungseinträge müssen denselben Wert aufweisen. Mögliche Werte sind in der folgenden Tabelle angegeben.



| Wert | BESCHREIBUNG                                                                      |
|-------|----------------------------------------------------------------------------------|
| Audio | Dateien, die über die benutzerdefinierte Erweiterung verfügen, werden im Musik Teil der Bibliothek angezeigt. |
| video | Dateien, die über die benutzerdefinierte Erweiterung verfügen, werden im Video Teil der Bibliothek angezeigt. |



 

Die folgenden Registrierungseinträge geben z. b. an, dass Dateien mit der Dateinamenerweiterung ". xyz" im Musik Teil der Bibliothek angezeigt werden:


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



Beachten Sie, dass jeder Code, der versucht, in die Registrierung auf dem Computer des Benutzers zu schreiben, in die HKEY-Unterstruktur des lokalen Computers schreiben kann, \_ \_ Wenn der aktuelle Benutzer über Administratorrechte verfügt.

Registrierungseinträge für die Bibliotheks Klassifizierung werden von den folgenden Versionen von Windows Media Player unterstützt.

-   Windows Media Player 9-Serie mit Hotfix 823275
-   Windows Media Player 10 und höher

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungs Einstellungen für die Dateinamenerweiterung**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




