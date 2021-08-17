---
title: Einstellungen der Ordnerüberwachungsregistrierung
description: Einstellungen der Ordnerüberwachungsregistrierung
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Windows Media Player, Registrierungseinstellungen für die Ordnerüberwachung
- Windows Media Player, Registrierungseinstellungen für die Dateiordnerüberwachung
- Windows Media Player,Registrierung
- Registrierung, Ordnerüberwachungseinstellungen
- Registrierung, Überwachungseinstellungen für Dateiordner
- Registrierung, Einstellungen für Windows Media Player
- Registrierungseinstellungen für die Ordnerüberwachung
- Registrierungseinstellungen für die Dateiordnerüberwachung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3e5e99c633c58a68b3579c55d38e6ad5b2415d9faac8d6c3438251c5a83459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748441"
---
# <a name="folder-monitoring-registry-settings"></a>Einstellungen der Ordnerüberwachungsregistrierung

Windows Media Player Serie 9 oder höher können Dateiordner auf neue digitale Mediendateien überwachen. Wenn der Player eine neue Datei in einem überwachten Ordner erkennt, fügt er die Datei automatisch der Bibliothek hinzu. Für Windows Media Player 9 bis Windows Media Player 11 können Benutzer die Liste der überwachten Ordner ändern, indem sie im Dialogfeld **Optionen** auf der Registerkarte Bibliothek auf **Ordner überwachen** klicken. Für Windows Media Player 12 kann ein Benutzer die Liste der überwachten Ordner ändern, indem er die Anweisungen im Thema Hinzufügen von [Elementen zur Windows Media Player Bibliothek befolgt.](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library) Für Windows Media Player 9 bis Windows Media Player 11 können Sie programmgesteuert einen Zu überwachenden Ordner hinzufügen, indem Sie der Registrierung einen Wert hinzufügen. Für Windows Media Player 12 können Sie die Registrierung nicht verwenden, um zu überwachende Ordner programmgesteuert hinzuzufügen oder zu entfernen.

Für Windows Media Player 9 bis Windows Media Player 11 müssen Sie zum Hinzufügen eines Ordners für die Überwachung zunächst zwei Werte im folgenden Registrierungsschlüssel erstellen oder ändern:

**Einstellungen für \_ HKEY CURRENT \_ USER Software \\ Microsoft \\ \\ MediaPlayer \\\\**

Die neuen Werte müssen wie folgt benannt werden.



| Name                           | type           | Beschreibung                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TrackFoldersDirectories**    | **REG \_ DWORD** | Ein **DWORD-Wert,** der die Anzahl der zu überwachende Ordner darstellt. Dies muss mit der Anzahl der **TrackFoldersDirectories**_X-Werte_ übereinstimmen.                                                                                                                                         |
| **TrackFoldersDirectories**_X_ | **REG \_ SZ**    | Ein Zeichenfolgenwert, der den Pfad des zu überwachende Ordners darstellt. Jeder zu überwachende Ordner erfordert einen separaten Wert. Das Suffix *X* ist eine ganze Zahl, die immer bei 0 beginnen und dann um 1 erhöht werden soll. Windows Media Player überwacht auch Unterordner des angegebenen Ordners. |



 

Um beispielsweise den ersten zu überwachende Ordner hinzuzufügen, fügen Sie den folgenden Wert hinzu:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



Erstellen Sie dann den Count-Wert:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



Um einen zweiten zu überwachende Ordner hinzuzufügen, fügen Sie den folgenden Wert hinzu:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



Erhöhen Sie dann den Count-Wert:


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungseinstellungen**](registry-settings.md)
</dt> </dl>

 

 




