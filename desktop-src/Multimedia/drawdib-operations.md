---
title: Drawdib-Vorgänge
description: Drawdib-Vorgänge
ms.assetid: 785ad42e-0c77-44a4-b4ef-be2a0ee2b563
keywords:
- Drawdib, Info
- Drawdib, zugreifen auf
- Drawdib, öffnen
- Drawdib, Vorgänge
- Drawdib, Gerätekontext (DC)
- DC (Gerätekontext)
- Drawdibopen-Funktion
- Drawdibclose-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc366287cdf481d70ef03aa82df5ea248673280b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471749"
---
# <a name="drawdib-operations"></a>Drawdib-Vorgänge

Mithilfe der [**drawdibopen**](/windows/desktop/api/Vfw/nf-vfw-drawdibopen) -Funktion können Sie auf die gesamte Gruppe von drawdib-Funktionen zugreifen. Diese Funktion lädt die dll (Dynamic-Link Library), ordnet Speicherressourcen zu, erstellt einen drawdib-Gerätekontext (DC) und verwaltet einen Verweis Zähler für die Anzahl der DCS, die initialisiert werden. **Drawdibopen** gibt auch ein Handle des neuen DC zurück, den Sie mit den anderen drawdib-Funktionen verwenden.

Sie können einen drawdib-DC freigeben, wenn Sie die Verwendung mithilfe der [**drawdibclose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose) -Funktion abgeschlossen haben. **Drawdibclose** Dekremente auch den Verweis Zähler der Anwendungen, die auf die dll zugreifen. Der **aufzurufende drawdibclose** -Befehl sollte die letzte drawdib-Funktion in der Anwendung sein.

Beliebig viele drawdib-DCS können erstellt werden. Sie können mehrere drawdib DCS verwenden, um mehrere Bitmaps gleichzeitig zu zeichnen. Sie können auch mehrere drawdib DCS mit eindeutigen Merkmalen erstellen, sodass Ihre Anwendung den DC mit den geeignetsten Einstellungen auswählen und dann verwenden kann. Beispielsweise können Sie zwei drawdib-DCS in einer Anwendung erstellen: eine, die ein Bild bei der normalen Auflösung anzeigt, und die andere, die einen vergrößerten Teil des Bilds anzeigt.

Um effizient auszuführen, benötigen drawdib-Funktionen Informationen zum Anzeige Adapter und dessen Treiber. Das Anzeige Profil wird durch Ausführen einer Reihe von Tests auf dem Anzeige Adapter abgerufen, wenn der Zugriff auf die dll, die die drawdib-Funktionen enthält, erstmalig erfolgt. Die drawdib-Funktionen verwenden diese Informationen für alle Anwendungen. Sie können diese Tests bei Bedarf mit der [**drawdibprofiledisplay**](/windows/desktop/api/Vfw/nf-vfw-drawdibprofiledisplay) -Funktion wiederholen.

> [!Note]  
> Das Abrufen und Speichern des Anzeige Profils ist in der Regel ein einmalige vorkommen. Wenn die Profilinformationen jedoch gelöscht werden oder ein anderer Anzeigetreiber im System installiert ist, führt drawdib die Tests erneut aus.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über die drawdib-Funktionen](about-the-drawdib-functions.md)
</dt> </dl>

 

 




