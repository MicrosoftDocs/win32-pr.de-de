---
title: Anpassen der Project
description: Anpassen der Project
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player,Anpassen von Beispielprojekten
- Onlineshops,Anpassen von Beispielprojekten
- 'Typ 2: Onlineshops,Anpassen von Beispielprojekten'
- Windows Media Player,Beispielprojekte
- Onlineshops,Beispielprojekte
- 'Typ 2: Onlineshops,Beispielprojekte'
- Anpassen von Beispielprojekten
- Beispiele,Geben Sie 2 Onlineshops ein.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdb57327904d81ac85114af0df9037d6c2c054938f16048f6ca72e711063cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902080"
---
# <a name="customizing-the-sample-project"></a>Anpassen der Project

Wenn Sie einen eigenen Onlineshop erstellen, sollten Sie die Implementierungen der folgenden Methoden in der Datei YourProject.cpp ändern:

-   **CYourProject::allowPlay**. Verwenden Sie diese Funktion, um Ihre Geschäftsregeln zum Wiedergeben geschützter Inhalte anzuwenden.
-   **CYourProject::allow CDProject**. Verwenden Sie diese Funktion, um Ihre Geschäftsregeln anzuwenden, damit Benutzer geschützte Inhalte auf eine CD kopieren können.
-   **CYourProject::allowPDATransfer**. Verwenden Sie diese Funktion, um Ihre Geschäftsregeln anzuwenden, damit Benutzer geschützte Inhalte auf ein portables Gerät übertragen können.
-   **CYourProject::startBackgroundProcessing**. Verwenden Sie diese Funktion, um alle Hintergrundverarbeitungsaufgaben zu initiieren, die Sie benötigen. Sie können dies z. B. als Gelegenheit verwenden, um nach abgelaufenen Lizenzen zu überprüfen.
-   **CYourProject::d eviceAvailable**. Verwenden Sie diese Funktion, um alle Aufgaben im Zusammenhang mit einem verbundenen Gerät zu initiieren.
-   **CYourProject::p repareForSync**. Verwenden Sie diese Funktion, um die erforderlichen Aufgaben direkt vor dem Synchronisieren digitaler Medien mit dem Gerät auszuführen.
-   **CYourProject::serviceEvent**. Verwenden Sie diese Funktion, um Aufgaben zu starten und zu beenden, die Sie ausführen möchten, wenn Ihr Onlineshop aktiv ist.
-   **CYourProject::stopBackgroundProcessing**. Verwenden Sie diese Funktion, um alle Hintergrundverarbeitungsaufgaben zu beenden, die Sie gestartet Windows Media Player **CYourProject::startBackgroundProcessing aufgerufen haben.**

## <a name="working-with-media-and-playlist-objects"></a>Arbeiten mit Medien- und Wiedergabelistenobjekten

Die **allowPlay-Methode** stellt einen Zeiger auf die **IWMPMedia-Schnittstelle** als Parameter bereit. Diese Schnittstelle ist die Windows Media Player Schnittstelle, die Medienobjekte darstellt. Durch Aufrufen der Methoden auf dieser Schnittstelle können Sie mit den Attributen und Eigenschaften eines einzelnen Medienelements arbeiten.

Die **Methoden allowCDPlay** und **allowPDATransfer** stellen einen Zeiger auf die **IWMPPlaylist-Schnittstelle** als Parameter bereit. Diese Schnittstelle ist die Windows Media Player Schnittstelle, die Wiedergabelistenobjekte darstellt. Durch Aufrufen der Methoden auf dieser Schnittstelle können Sie mit den Attributen und Eigenschaften einer Wiedergabeliste arbeiten, einer Wiedergabeliste Elemente hinzufügen oder Elemente aus einer Wiedergabeliste entfernen.

Informationen zum programmgesteuerten Entfernen eines Elements aus einer Wiedergabeliste finden Sie in der Implementierung von **CAllowBaseDialog <T> ::OnRemoveMediaFromPlaylist**. Weitere Informationen zum Arbeiten mit Medien- und Wiedergabelistenobjekten finden Sie unter [Player Object Model for Scripting Languages](player-object-model-for-scripting-languages.md).

## <a name="code-that-can-be-removed"></a>Code, der entfernt werden kann

Wahrscheinlich möchten Sie den Code entfernen, der Dialogfelder öffnet, da es unwahrscheinlich ist, dass Sie möchten, dass Benutzer entscheiden, welche Medienelemente abgespielt oder kopiert werden können. Entfernen Sie aus YourProject.h den folgenden Code:

-   Die Deklaration von **CAllowBaseDialog**.
-   Die Deklaration von **CAllowDialogDialog**.
-   Die Deklaration von **CAllowTransferDialog**.

Entfernen Sie aus YourProject.cpp den folgenden Code:

-   Die Implementierung von **CAllowBaseDialog <T> ::OnInitDialog**.
-   Die Implementierung von **CAllowBaseDialog <T> ::OnRemoveMediaFromPlaylist**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen des Plug-Ins für eine Online-Store**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




