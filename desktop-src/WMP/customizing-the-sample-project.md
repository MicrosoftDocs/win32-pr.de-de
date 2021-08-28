---
title: Anpassen der Beispiel-Project
description: Anpassen der Beispiel-Project
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player Onlineshops, Anpassen von Beispielprojekten
- Onlineshops, Anpassen von Beispielprojekten
- Geben Sie 2 Onlineshops ein, und passen Sie Beispielprojekte an.
- Windows Media Player Onlineshops, Beispielprojekte
- Onlineshops, Beispielprojekte
- Geben Sie 2 Onlineshops ein, Beispielprojekte.
- Anpassen von Beispielprojekten
- Beispiele, Geben Sie 2 Onlineshops ein.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e83d6384529ea9b67c5132ec9cc1846da5e438
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881808"
---
# <a name="customizing-the-sample-project"></a>Anpassen der Beispiel-Project

Wenn Sie einen eigenen Onlineshop erstellen, sollten Sie die Implementierungen der folgenden Methoden in der Datei YourProject.cpp ändern:

-   **CYourProject::allowPlay**. Verwenden Sie diese Funktion, um Ihre Geschäftsregeln anzuwenden, um die Wiedergabe geschützter Inhalte zuzulassen.
-   **CYourProject::allow CDProject**. Verwenden Sie diese Funktion, um Ihre Geschäftsregeln anzuwenden, damit Benutzer geschützte Inhalte auf eine CD kopieren können.
-   **CYourProject::allowPDATransfer**. Verwenden Sie diese Funktion, um Ihre Geschäftsregeln anzuwenden, damit Benutzer geschützte Inhalte auf ein portables Gerät übertragen können.
-   **CYourProject::startBackgroundProcessing**. Verwenden Sie diese Funktion, um alle erforderlichen Hintergrundverarbeitungsaufgaben zu initiieren. Sie können dies beispielsweise verwenden, um nach abgelaufenen Lizenzen zu suchen.
-   **CYourProject::d eviceAvailable**. Verwenden Sie diese Funktion, um alle Aufgaben im Zusammenhang mit einem verbundenen Gerät zu initiieren.
-   **CYourProject::p repareForSync**. Verwenden Sie diese Funktion, um die erforderlichen Aufgaben direkt vor der Synchronisierung digitaler Medien mit dem Gerät auszuführen.
-   **CYourProject::serviceEvent**. Verwenden Sie diese Funktion, um Aufgaben zu starten und zu beenden, die Sie ausführen möchten, wenn Ihr Onlineshop aktiv ist.
-   **CYourProject::stopBackgroundProcessing**. Verwenden Sie diese Funktion, um alle Hintergrundverarbeitungsaufgaben zu beenden, die Sie beim Windows Media Player **CYourProject::startBackgroundProcessing** gestartet haben.

## <a name="working-with-media-and-playlist-objects"></a>Arbeiten mit Medien- und Wiedergabelistenobjekten

Die **allowPlay-Methode** stellt einen Zeiger auf die **IWMPMedia-Schnittstelle** als Parameter bereit. Diese Schnittstelle ist die Windows Media Player Schnittstelle, die Medienobjekte darstellt. Indem Sie die Methoden auf dieser Schnittstelle aufrufen, können Sie mit den Attributen und Eigenschaften eines einzelnen Medienelements arbeiten.

Die **Methoden allowCDDda** und **allowPDATransfer** stellen einen Zeiger auf die **IWMPPlaylist-Schnittstelle** als Parameter bereit. Diese Schnittstelle ist die Windows Media Player Schnittstelle, die Wiedergabelistenobjekte darstellt. Indem Sie die Methoden auf dieser Schnittstelle aufrufen, können Sie mit den Attributen und Eigenschaften einer Wiedergabeliste arbeiten, einer Wiedergabeliste Elemente hinzufügen oder Elemente aus einer Wiedergabeliste entfernen.

Informationen zum programmgesteuerten Entfernen eines Elements aus einer Wiedergabeliste finden Sie in der Implementierung von **CAllowBaseDialog &lt; T &gt; ::OnRemoveMediaFromPlaylist.** Weitere Informationen zum Arbeiten mit Medien- und Wiedergabelistenobjekten finden Sie unter [Player-Objektmodell für Skriptsprachen.](player-object-model-for-scripting-languages.md)

## <a name="code-that-can-be-removed"></a>Code, der entfernt werden kann

Sie möchten wahrscheinlich den Code entfernen, der Dialogfelder öffnet, da es unwahrscheinlich ist, dass Benutzer entscheiden, welche Medienelemente wiedergegeben oder kopiert werden können. Entfernen Sie aus YourProject.h den folgenden Code:

-   Die Deklaration von **CAllowBaseDialog**.
-   Die Deklaration von **CAllowDialogDialog.**
-   Die Deklaration von **CAllowTransferDialog**.

Entfernen Sie aus YourProject.cpp den folgenden Code:

-   Die Implementierung von **CAllowBaseDialog &lt; T &gt; ::OnInitDialog**.
-   Die Implementierung von **CAllowBaseDialog &lt; T &gt; ::OnRemoveMediaFromPlaylist**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen des Plug-Ins für einen Typ 2 Online Store**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




