---
title: Verwalten von Dateien und Daten
description: Benutzer haben einfacheren Zugriff auf Dateien und Daten in Windows 7.
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9091a2d9bb2cf01d4f9b514c55e78f2f989f01d6d64a929608e14c32bfd395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086661"
---
# <a name="managing-files-and-data"></a>Verwalten von Dateien und Daten

Benutzer haben einfacheren Zugriff auf Dateien und Daten in Windows 7. Neue APIs machen Dateien und Ansichten informativer, sodass Anwendungen relevante und aussagekräftige Informationen an Windows Explorer übermitteln können. Darüber hinaus profitieren Anwendungen vom neuen Bibliotheksmodell, einem *nützlicheren,* abstrakteren Konzept des Benutzerspeicherplatzes als Ordner, und können auch an allgemeinen Bibliotheken ähnlicher Dateitypen teilnehmen, die von verschiedenen Anwendungen gemeinsam genutzt werden.

## <a name="libraries"></a>Bibliotheken

Windows 7 führt das Konzept von Bibliotheken als Ziele ein, bei denen Entwickler und Endbenutzer ihre Daten als Sammlungen von Elementen finden und organisieren können, die sich über mehrere *Speicherorte* auf dem lokalen Computer sowie auf Remotecomputern erstrecken können.

Die *Bibliotheks-APIs* bieten Entwicklern eine einfache Möglichkeit, Anwendungen zu erstellen, die *Bibliotheken* als erstklassige Elemente in Anwendungen erstellen, mit ihnen interagieren und diese unterstützen. *Bibliotheken* können auch über das Dialogfeld Ordnerauswahl ausgewählt werden. Anwendungen können relevante Bibliotheksbereiche aufzählen oder die Bibliothek direkt als Ordner verwenden. (Siehe [Windows Bibliotheken](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) und [Windows 7 Bibliotheken: Entwicklerressourcen](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).

![Windows 7-Bilderbibliothek](images/windows7-10.jpg)

*Bildbibliothek* zeigt Ihre Bilder an, unabhängig davon, wo sie gespeichert sind.

## <a name="file-formats-and-data-stores"></a>Dateiformate und Datenspeicher

In Windows 7 vereinfacht Windows Explorer die Dateiverwaltung und -bearbeitung für den Benutzer auf verschiedene Weise:

-   Die Vorschau für den Dateityp Ihrer Anwendung ist mit einer neuen Schaltfläche besser zugänglich, mit der Benutzer den Vorschaubereich anzeigen und ausblenden können.
-   Immersive Visuelle Stapel aggregieren Miniaturbilder für Dateitypen in einer Ansicht.
-   Windows Explorer-Ansichten zeigen nützliche Informationen basierend auf Eigenschaften an, die mit Ihrem Eigenschaftenhandler geschrieben wurden.
-   Dokumentausschnitte und Treffermarkierungen verwenden Ihre IFilter-Schnittstellenimplementierungen, um das Suchen und Suchen von Dateien zu vereinfachen. 
-   Kontextmenüverben und -befehle sind einfacher als je zuvor zu implementieren.

Durch die Implementierung aller geeigneten Formathandler für die elemente, die von Ihrem Protokollhandler zurückgegeben werden, können Suchergebnisse aus Ihrem benutzerdefinierten Datenspeicher so lang sein wie Suchergebnisse aus Dateien. *Bibliotheken* werden automatisch für Ihre Protokollhandler erstellt, sodass Benutzer ihre Suchvorgänge problemlos eingrenzen können. Und die Logik zum Erstellen von *Bibliotheken* kann problemlos über die Registrierung angepasst werden. (Weitere Informationen finden Sie unter [Developing Filters for Windows Search](../search/-search-3x-wds-extidx-filters.md).)

![Windows 7-Dokumentbibliothek](images/windows7-11.jpg)

In Windows 7 vereinfacht Windows Explorer die Verwaltung und Bearbeitung von Dateien.

 

 