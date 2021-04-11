---
title: Anpassen des Beispielprojekts
description: Anpassen des Beispielprojekts
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player Online Stores, Anpassen von Beispielprojekten
- Online Stores, Anpassen von Beispielprojekten
- Geben Sie 2 Online Stores ein, und passen Sie Beispiel Projekte an.
- Windows Media Player Online Stores, Beispiel Projekte
- Online Stores, Beispiel Projekte
- Typ 2 Online Stores, Beispiel Projekte
- Anpassen von Beispielprojekten
- Beispiele, Typ 2 Online Stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeec3ebcb74304cd5181783e9c457d6a149b0cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948003"
---
# <a name="customizing-the-sample-project"></a>Anpassen des Beispielprojekts

Beim Erstellen eines eigenen Online Stores möchten Sie die Implementierungen der folgenden Methoden in der Datei "yourproject. cpp" ändern:

-   **Cyourproject:: allowplay**. Verwenden Sie diese Funktion, um Ihre Geschäftsregeln anzuwenden, um die Wiedergabe geschützter Inhalte zuzulassen.
-   **Cyourproject:: lässt cdburn** zu. Verwenden Sie diese Funktion, um Ihre Geschäftsregeln anzuwenden, damit Benutzer geschützte Inhalte auf eine CD kopieren können.
-   **Cyourproject:: allowpdatransfer**. Verwenden Sie diese Funktion, um Ihre Geschäftsregeln anzuwenden, damit Benutzer geschützte Inhalte auf ein tragbares Gerät übertragen können.
-   **Cyourproject:: startbackgroundprocessing**. Verwenden Sie diese Funktion, um alle erforderlichen Hintergrund Verarbeitungsaufgaben zu initiieren. Beispielsweise können Sie dies als Gelegenheit zum Überprüfen auf abgelaufene Lizenzen verwenden.
-   **Cyourproject::d** entfernen. Verwenden Sie diese Funktion, um alle Aufgaben im Zusammenhang mit einem verbundenen Gerät zu initiieren.
-   **Cyourproject::p Analyse forsync**. Verwenden Sie diese Funktion, um erforderliche Aufgaben auszuführen, bevor Sie digitale Medien mit dem Gerät synchronisieren.
-   **Cyourproject:: Service Event**. Verwenden Sie diese Funktion, um Aufgaben zu starten und zu beenden, die Sie ausführen möchten, wenn Ihr Online Store aktiv ist.
-   **Cyourproject:: stopbackgroundprocessing**. Verwenden Sie diese Funktion, um alle Hintergrund Verarbeitungsaufgaben zu beenden, die Sie gestartet haben, als Windows Media Player den Namen **cyourproject:: startbackgroundprocessing** hat.

## <a name="working-with-media-and-playlist-objects"></a>Arbeiten mit Medien-und Wiedergabelisten Objekten

Die **allowplay** -Methode stellt einen Zeiger auf die **iwmpmedia** -Schnittstelle als Parameter bereit. Diese Schnittstelle ist die Windows Media Player-Schnittstelle, die Medienobjekte darstellt. Indem Sie die-Methoden für diese Schnittstelle aufrufen, können Sie mit den Attributen und Eigenschaften eines einzelnen Medien Elements arbeiten.

Die Methoden **allowcdburn** und **allowpdatransfer** stellen einen Zeiger auf die **iwmpwiedergabe** -Schnittstelle als Parameter bereit. Diese Schnittstelle ist die Windows Media Player-Schnittstelle, die Wiedergabelisten Objekte darstellt. Indem Sie die-Methoden für diese Schnittstelle aufrufen, können Sie mit den Attributen und Eigenschaften einer Wiedergabeliste arbeiten, Elemente zu einer Wiedergabeliste hinzufügen oder Elemente aus einer Wiedergabeliste entfernen.

Informationen zum programmgesteuerten Entfernen eines Elements aus einer Wiedergabeliste finden Sie in der Implementierung von **callowbasedialog <T> :: onremovemediafromplaylist**. Weitere Informationen zum Arbeiten mit Medien-und Wiedergabelisten Objekten finden Sie unter [Player Object Model for Scripting Languages](player-object-model-for-scripting-languages.md).

## <a name="code-that-can-be-removed"></a>Code, der entfernt werden kann

Wahrscheinlich möchten Sie den Code entfernen, der die Dialogfelder öffnet, da es unwahrscheinlich ist, dass Benutzer entscheiden, welche Medienelemente wiedergegeben oder kopiert werden können. Entfernen Sie den folgenden Code aus yourproject. h:

-   Die Deklaration von **callowbasedialog**.
-   Die Deklaration von **callowburndialog**.
-   Die Deklaration von **callowtransferdialog**.

Entfernen Sie aus yourproject. cpp den folgenden Code:

-   Die Implementierung von **callowbasedialog <T> :: OnInitDialog**.
-   Die Implementierung von **callowbasedialog <T> :: onremovemediafromwiedergabe Liste**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Entwickeln des Plug-Ins für einen Typ 2-Online Store**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




