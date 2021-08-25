---
title: Informationen zur Wiedergabelistensynchronisierung
description: Informationen zur Wiedergabelistensynchronisierung
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player, Wiedergabelistensynchronisierung
- Windows Media Player Objektmodell, Wiedergabelistensynchronisierung
- Objektmodell, Wiedergabelistensynchronisierung
- Windows Media Player ActiveX-Steuerelement, Wiedergabelistensynchronisierung
- ActiveX-Steuerelement, Wiedergabelistensynchronisierung
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelistensynchronisierung
- Windows Media Player Mobile Wiedergabelistensynchronisierung
- Synchronisieren von Geräten, Wiedergabelisten
- Gerätesynchronisierung, Wiedergabelisten
- Wiedergabelisten, Synchronisierung
- Windows Medienmetadatei-Wiedergabelisten, Synchronisierung
- Metafile-Wiedergabelisten, Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe54bef188fea2baee64da962dabf4eb8f700b72407772d591d73f52be2d4289
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956870"
---
# <a name="about-playlist-synchronization"></a>Informationen zur Wiedergabelistensynchronisierung

Windows Media Player 10 oder höher ist für die Synchronisierung digitaler Medieninhalte mit Geräten mithilfe eines Wiedergabelistensynchronisierungsmodells konzipiert. Dies bedeutet, dass Inhalte, die auf ein Gerät kopiert werden sollen, Teil einer Wiedergabeliste sein müssen. Wenn der Benutzer einzelne digitale Medieninhalte von seinem Computer auf ein Gerät übertragen möchte, fügt Windows Media Player den Inhalt einer Standardwiedergabeliste zum Kopieren hinzu.

Die Windows Media Player-Gerätesynchronisierungs-APIs sind so konzipiert, dass sie auch wie folgt funktionieren. Wie Windows Media Player kann Ihr Programm dem Benutzer eine Liste von Wiedergabelisten präsentieren, die er definiert hat. Anschließend können Sie dem Benutzer ermöglichen, auszuwählen, welche Wiedergabelisten mit einem bestimmten Gerät synchronisiert werden sollen, und die Prioritätsreihenfolge für den Synchronisierungsprozess festzulegen.

Da portable Geräte über eine begrenzte Speicherkapazität verfügen, kann der Benutzer mehr digitale Medieninhalte synchronisieren, als das Gerät speichern kann. Windows Media Player synchronisiert Inhalte in prioritätsgeordneter Reihenfolge. Der Benutzer kann die Prioritätsreihenfolge mithilfe eines Dialogfelds definieren, auf das über das **Feature Geräte** zugegriffen werden kann. Als Reaktion auf Benutzereingaben in Ihr Programm können Sie die Prioritätsreihenfolge programmgesteuert ändern, indem Sie die Werte bestimmter Wiedergabelistenattribute ändern. Zusammen werden diese Attribute als *Synchronisierungsattribute* bezeichnet.

Jede Wiedergabeliste in einer Bibliothek verfügt über 16 Synchronisierungsattribute: **Sync01** bis **Sync16.** Jedes Attribut stellt das Gerät dar, das über den entsprechenden Partnerschaftsindex verfügt. Der Wert jedes Attributs teilt Ihnen zwei Dinge mit:

-   Gibt an, ob die Wiedergabeliste mit dem Gerät synchronisiert werden soll.
-   Der Prioritätswert für die Wiedergabeliste.

Der Wert 0 gibt an, dass Windows Media Player nicht versuchen sollte, die Wiedergabeliste mit dem Gerät zu synchronisieren. Jeder andere Wert ist eine Prioritätsnummer. Niedrigere Werte erhalten zur Synchronisierungszeit eine höhere Priorität.

Wiedergabelisten verfügen auch über ein **SyncOnly-Attribut,** das angibt, ob die Wiedergabeliste nur für die Synchronisierung verfügbar ist.

Einzelne Elemente von Inhalten digitaler Medien enthalten auch Metadaten zur Synchronisierung. Wenn Sie ein **Media-Objekt** aus der Bibliothek abrufen, können Sie den Wert des **SyncState-Attributs** überprüfen. Dieses Attribut stellt erweiterte Informationen darüber bereit, ob der Inhalt erfolgreich auf das Gerät kopiert wurde oder ob beim Kopieren des Inhalts ein Fehler aufgetreten ist, da er nicht passt.

> [!Note]  
> Sie sollten die Bereitstellung von Benutzeroberflächenelementen vermeiden, die es dem Benutzer ermöglichen, Wiedergabelisten aus allen Bibliotheksinhalten für die Synchronisierung zu erstellen.

 

Um die Leistung zu optimieren, erzwingt Windows Media Player eine Reihe von Regeln zum Erstellen von Synchronisierungswiedergabelisten. Ihr Programm sollte nur Synchronisierungswiedergabelisten für von Ihnen bereitgestellte Inhalte erstellen. Erlauben Sie Windows Media Player, Synchronisierungswiedergabelisten für Inhalte zu erstellen, die der Benutzer der Bibliothek aus anderen Quellen hinzugefügt hat.

Als Alternative zum Erstellen einer eigenen Wiedergabelistenbenutzeroberfläche können Sie Benutzern ein Standarddialogfeld für die Auswahl von Wiedergabelisten und die Verwaltung der Partnerschaft für ein Gerät anzeigen. Rufen Sie hierzu [IWMPSyncDevice::showSettings auf.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings) Wenn Sie diese Methode aufrufen, zeigt Windows Media Player das entsprechende Synchronisierungseinstellungsdialogfeld an. Wenn der Benutzer das Dialogfeld schließt, kehrt Windows Media Player automatisch zum vorherigen Andockzustand zurück und übergibt die Steuerung an Das Remoteprogramm.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zur Gerätesynchronisierung**](about-device-synchronization.md)
</dt> <dt>

[**Verwalten von Synchronisierungswiedergabelisten**](managing-synchronization-playlists.md)
</dt> <dt>

[**Wiedergabelistenattribute**](playlist-attributes.md)
</dt> </dl>

 

 




