---
title: Verwalten von Dateien und Daten
description: Benutzer haben in Windows 7 einen einfacheren Zugriff auf Dateien und Daten.
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5617d7746746186933bce022aa2202175fb994e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948895"
---
# <a name="managing-files-and-data"></a>Verwalten von Dateien und Daten

Benutzer haben in Windows 7 einen einfacheren Zugriff auf Dateien und Daten. Neue APIs machen Dateien und Ansichten informativer, sodass Anwendungen relevante und besondere Informationen an Windows Explorer übermitteln können. Darüber hinaus profitieren Anwendungen vom neuen *Bibliotheks* Modell, einem nützlichen, stärker abstrakten Konzept des Benutzer Speicherplatzes als Ordnern und können auch an gemeinsamen Bibliotheken ähnlicher Dateitypen teilnehmen, die von verschiedenen Anwendungen gemeinsam genutzt werden.

## <a name="libraries"></a>Bibliotheken

Mit Windows 7 wird das Konzept der *Bibliotheken* als Ziele eingeführt, bei denen Entwickler und Endbenutzer Ihre Daten als Sammlungen von Elementen suchen und organisieren können, die mehrere Standorte auf dem lokalen Computer und auf Remote Computern umfassen können.

Die *Bibliotheks*-APIs bieten Entwicklern eine einfache Möglichkeit, Anwendungen zu erstellen, die *Bibliotheken* als erstklassige Elemente innerhalb von Anwendungen erstellen, mit ihnen interagieren und diese unterstützen. *Bibliotheken* können auch über das Dialogfeld Ordner Auswahl ausgewählt werden. Anwendungen können relevante Bibliotheks Bereiche auflisten, oder Sie können die Bibliothek direkt als Ordner verwenden. (Weitere Informationen finden Sie unter [Windows-Bibliotheken](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) und [Windows 7-Bibliotheken: Entwickler Ressourcen](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).

![Windows 7-Bildbibliothek](images/windows7-10.jpg)

*Bilderbibliothek* zeigt Ihre Bilder an, unabhängig davon, wo Sie gespeichert sind.

## <a name="file-formats-and-data-stores"></a>Dateiformate und Datenspeicher

In Windows 7 erleichtert Windows Explorer das Verwalten und manipulieren von Dateien für den Benutzer auf verschiedene Weise:

-   Die Vorschau für den Dateityp Ihrer Anwendung ist mit einer neuen Schaltfläche, über die Benutzer den Vorschaufenster anzeigen und ausblenden können, besser zugänglich.
-   Immersive visuelle Stapel aggregieren Miniaturbilder für Dateitypen in einer Ansicht.
-   Windows Explorer-Ansichten zeigen nützliche Informationen auf der Grundlage von Eigenschaften an, die mit Ihrem Eigenschaften Handler geschrieben wurden.
-   Dokument Ausschnitte und Treffer Hervorhebung verwenden Sie die Implementierung der **IFilter** -Schnittstelle, um das Suchen und suchen von Dateien zu vereinfachen.
-   Kontextmenü Verben und Befehle sind einfacher als je zuvor zu implementieren.

Durch Implementieren aller entsprechenden Format Handler für die Elemente, die von Ihrem Protokollhandler zurückgegeben werden, können Suchergebnisse aus dem benutzerdefinierten Datenspeicher so umfangreich sein wie Suchergebnisse aus Dateien. *Bibliotheken* werden automatisch für Ihre Protokollhandler erstellt, damit Benutzer Ihre Suchvorgänge problemlos festlegen können. Und die Logik zum Erstellen von *Bibliotheken* kann problemlos über die Registrierung angepasst werden. (Siehe [entwickeln von Filtern für die Windows-Suche](../search/-search-3x-wds-extidx-filters.md).)

![Windows 7-Dokumentbibliothek](images/windows7-11.jpg)

In Windows 7 erleichtert Windows Explorer die Dateiverwaltung und-Bearbeitung.

 

 