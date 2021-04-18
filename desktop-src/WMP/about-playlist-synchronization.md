---
title: Informationen zur Wiedergabeliste
description: Informationen zur Wiedergabeliste
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player, Wiedergabelisten Synchronisierung
- Windows Media Player-Objektmodell, Wiedergabelisten Synchronisierung
- Objektmodell, Wiedergabelisten Synchronisierung
- Windows Media Player ActiveX-Steuerelement, Wiedergabelisten Synchronisierung
- ActiveX-Steuerelement, Wiedergabeliste
- Windows Media Player Mobile ActiveX-Steuerelement, Wiedergabelisten Synchronisierung
- Windows Media Player Mobile, Wiedergabelisten Synchronisierung
- Synchronisieren von Geräten, Wiedergabelisten
- Geräte Synchronisierung, Wiedergabelisten
- Wiedergabelisten, Synchronisierung
- Windows Media Metadatei-Wiedergabelisten, Synchronisierung
- Metadatei-Wiedergabelisten, Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc019b31518fda1a49c8d3ae86f2d03c4ecefc8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314243"
---
# <a name="about-playlist-synchronization"></a>Informationen zur Wiedergabeliste

Windows Media Player 10 oder höher ist so konzipiert, dass digitale Medieninhalte mithilfe eines Wiedergabelisten-Synchronisierungs Modells mit Geräten synchronisiert werden. Dies bedeutet, dass Inhalte, die auf ein Gerät kopiert werden sollen, Teil einer Wiedergabeliste sein müssen. Wenn der Benutzer die Inhalte einzelner digitaler Medien von seinem Computer auf ein Gerät übertragen möchte, fügt Windows Media Player den Inhalt einer Standard Wiedergabeliste zum Kopieren hinzu.

Die APIs für die Synchronisierung von Windows Media Player-Geräten sind so konzipiert, dass Sie auch so funktionieren. Wie bei Windows Media Player kann das Programm dem Benutzer eine Liste der von ihm definierten Wiedergabelisten präsentieren. Anschließend können Sie es dem Benutzer ermöglichen, auszuwählen, welche Wiedergabelisten mit einem bestimmten Gerät synchronisiert werden sollen, und die Prioritäts Reihenfolge für den Synchronisierungs Prozess festzulegen.

Da tragbare Geräte über eine begrenzte Speicherkapazität verfügen, ist es möglich, dass der Benutzer mehr digitale Medieninhalte synchronisiert, als das Gerät speichern kann. Windows Media Player synchronisiert Inhalte in der Prioritäts Reihenfolge. Der Benutzer kann die Prioritäts Reihenfolge mithilfe eines Dialog Felds definieren, auf das über die **Geräte** Funktion zugegriffen werden kann. Als Reaktion auf Benutzereingaben für Ihr Programm können Sie die Prioritäts Reihenfolge Programm gesteuert ändern, indem Sie die Werte bestimmter Wiedergabelisten Attribute ändern. Gemeinsam werden diese Attribute als *Synchronisierungs* Attribute bezeichnet.

Jede Wiedergabeliste in einer Bibliothek hat 16 Synchronisierungs Attribute: **Sync01** bis **Sync16**. Jedes Attribut stellt das Gerät dar, das über den entsprechenden Partnerschafts Index verfügt. Der Wert jedes Attributs gibt Ihnen zwei Dinge:

-   Gibt an, ob die Wiedergabeliste mit dem Gerät synchronisiert werden soll.
-   Der Prioritätswert für die Wiedergabeliste.

Der Wert 0 (null) gibt an, dass Windows Media Player nicht versuchen soll, die Wiedergabeliste mit dem Gerät zu synchronisieren. Jeder andere Wert ist eine Prioritäts Nummer. Niedrigere Werte erhalten zum Zeitpunkt der Synchronisierung höhere Priorität.

Wiedergabelisten verfügen auch über ein **synkonstante** Attribut, das angibt, ob die Wiedergabeliste nur für die Synchronisierung verfügbar ist.

Einzelne Elemente digitaler Medieninhalte enthalten ebenfalls Metadaten über die Synchronisierung. Wenn Sie ein **Medien** Objekt aus der Bibliothek abrufen, können Sie den Wert des **SyncState** -Attributs überprüfen. Dieses Attribut enthält erweiterte Informationen darüber, ob der Inhalt erfolgreich auf das Gerät kopiert wurde oder ob beim Kopieren des Inhalts ein Fehler aufgetreten ist, weil er nicht geeignet wäre.

> [!Note]  
> Vermeiden Sie die Bereitstellung von Benutzeroberflächen Elementen, die es dem Benutzer ermöglichen, für die Synchronisierung Wiedergabelisten aus allen Bibliotheks Inhalten zu erstellen.

 

Um die Leistung zu optimieren, erzwingt Windows Media Player einen Satz von Regeln zum Erstellen von Synchronisierungs Wiedergabelisten. Ihr Programm sollte nur Synchronisierungs Wiedergabelisten für den von Ihnen bereitgestellten Inhalt erstellen. Erlauben Sie Windows Media Player, Synchronisierungs Wiedergabelisten für Inhalte zu erstellen, die der Bibliothek aus anderen Quellen hinzugefügt hat.

Als Alternative zum Erstellen einer eigenen Wiedergabeliste können Sie Benutzern ein Standard Dialogfeld für die Auswahl von Wiedergabelisten und die Verwaltung der Partnerschaft für ein Gerät präsentieren. Nennen Sie hierzu [iwmpsyncdevice:: showsettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings). Wenn Sie diese Methode aufrufen, zeigt Windows Media Player das Dialogfeld Synchronisierungs Einstellungen an. Wenn der Benutzer das Dialogfeld schließt, kehrt Windows Media Player automatisch in seinen vorherigen Andock Zustand zurück und übergibt die Steuerung zurück an das Remote Programm.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zur Geräte Synchronisierung**](about-device-synchronization.md)
</dt> <dt>

[**Synchronisierungs Wiedergabelisten**](managing-synchronization-playlists.md)
</dt> <dt>

[**Wiedergabelisten Attribute**](playlist-attributes.md)
</dt> </dl>

 

 




