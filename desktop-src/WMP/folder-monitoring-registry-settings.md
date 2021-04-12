---
title: Registrierungs Einstellungen für die Ordner Überwachung
description: Registrierungs Einstellungen für die Ordner Überwachung
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Windows Media Player, Registrierungs Einstellungen für die Ordner Überwachung
- Windows Media Player, Registrierungs Einstellungen für die Datei Ordner Überwachung
- Windows Media Player, Registrierung
- Registrierung, Ordner Überwachungs Einstellungen
- Registrierung, Einstellungen für die Überwachung von Datei Ordnern
- Registrierung, Einstellungen für Windows-Media Player
- Registrierungs Einstellungen für die Ordner Überwachung
- Registrierungs Einstellungen für die Datei Ordner Überwachung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233076d1fc807dd5cdd79e9b4985ef752fba0815
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391129"
---
# <a name="folder-monitoring-registry-settings"></a>Registrierungs Einstellungen für die Ordner Überwachung

Windows Media Player 9 oder höher kann Datei Ordner für neue digitale Mediendateien überwachen. Wenn der Spieler eine neue Datei in einem überwachten Ordner erkennt, wird die Datei automatisch der Bibliothek hinzugefügt. Für Windows Media Player 9 bis Windows Media Player 11 können Benutzer die Liste der überwachten Ordner ändern, indem Sie im Dialogfeld **Optionen** auf der Registerkarte Bibliothek auf **Ordner überwachen** klicken. Für Windows Media Player 12 kann ein Benutzer die Liste der überwachten Ordner anhand der Anweisungen im Thema [Hinzufügen von Elementen zur Windows Media Player-Bibliothek](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library)ändern. Für Windows Media Player 9 bis Windows Media Player 11 können Sie einen zu überwachenden Ordner Programm gesteuert hinzufügen, indem Sie der Registrierung einen Wert hinzufügen. Für Windows Media Player 12 können Sie die Registrierung nicht verwenden, um zu überwachende Ordner Programm gesteuert hinzuzufügen oder zu entfernen.

Wenn Sie für Windows Media Player 9 bis Windows Media Player 11 einen Ordner für die Überwachung hinzufügen möchten, müssen Sie zunächst zwei Werte im folgenden Registrierungsschlüssel erstellen oder ändern:

**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ Preferences\\**

Die neuen Werte müssen wie folgt benannt werden.



| Name                           | type           | BESCHREIBUNG                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Trackfoldersdirectories**    | **REG \_ DWORD** | Ein **DWORD** -Wert, der die Anzahl der zu überwachenden Ordner darstellt. Diese muss mit der Anzahl der **trackfoldersdirectories * * * X* -Werte identisch sein.                                                                                                                                         |
| **Trackfoldersdirectories * * * X* | **REG- \_ SZ**    | Ein Zeichen folgen Wert, der den Pfad des zu überwachenden Ordners darstellt. Für jeden zu überwachenden Ordner ist ein separater Wert erforderlich. Das Suffix *X* ist eine Ganzzahl, die immer bei 0 beginnen sollte und dann um 1 erhöht werden soll. Windows Media Player überwacht auch die Unterordner des angegebenen Ordners. |



 

Fügen Sie z. b. den folgenden Wert hinzu, um den ersten zu überwachenden Ordner hinzuzufügen:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



Erstellen Sie dann den Wert Anzahl:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



Um einen zweiten Ordner zur Überwachung hinzuzufügen, fügen Sie den folgenden Wert hinzu:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



Erhöhen Sie anschließend den Wert für die Anzahl:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungs Einstellungen**](registry-settings.md)
</dt> </dl>

 

 




