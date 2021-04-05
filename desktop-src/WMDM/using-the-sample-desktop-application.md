---
title: Verwenden der Beispiel-Desktop Anwendung
description: Verwenden der Beispiel-Desktop Anwendung
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Windows Media Device Manager, Beispiele
- Device Manager, Beispiele
- Desktop Anwendungen, Beispiele
- Windows Media Device Manager, Beispiel für eine Desktop Anwendung
- Beispiel für Device Manager Desktop Anwendung
- Beispiele, Desktop Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd511ea5241f458d2cd926dc8fb2f3681757ff8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708747"
---
# <a name="using-the-sample-desktop-application"></a>Verwenden der Beispiel-Desktop Anwendung

Bei der Beispiel-Desktop Anwendung handelt es sich um ein grundlegendes Fenster mit zwei Fenstern, das einem Windows-Explorer ähnelt Es ermöglicht Ihnen das Durchsuchen des Inhalts eines Geräts, das Verwenden einer Strukturansicht der Ordner im linken Bereich und von Dateien im rechten Bereich. Das Stammverzeichnis jeder Ordnerstruktur wird logisch als anderes Gerät betrachtet, obwohl einige Geräte sich selbst als mehrere Objekte (eines für jeden Stamm Speicher) darstellen könnten. Um die grundlegenden Eigenschaften eines Ordners oder einer Datei zu lesen, klicken Sie mit der rechten Maustaste auf das Objekt, und wählen Sie **Eigenschaften** aus.

Sie können Dateien auf dem Gerät löschen, indem Sie im rechten Bereich eine Datei auswählen und im Menü **Datei** die Option **Löschen** auswählen. Zum Hinzufügen von Mediendateien zum Gerät können Sie Dateien vom Desktop auf den rechten Bereich des Programms ziehen. Beachten Sie, dass Dateien ein vom Gerät unterstütztes Medienformat aufweisen müssen. Dateien mit unzulässigen Formaten (nicht-Mediendateien, z. b. txt-Dateien oder Medienformate, die nicht vom Gerät unterstützt werden) werden nicht an das Gerät gesendet. (Beachten Sie, dass es sich bei dieser Einschränkung um das Programm handelt. Mithilfe von Windows Media Device Manager können Sie jede beliebige Datei an ein Gerät senden, wenn Sie vom Gerät akzeptiert wird.)

Wenn Sie Rückruf Ereignisse erfassen möchten, die an die [**iwmdmoperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) -Schnittstelle gesendet werden, müssen Sie die Option "Use Operation Interface" im Menü **Optionen** aktivieren.

Mit dem Menü **Optionen** können Sie auch auswählen, ob Sie mehrere erweiterte Schnittstellen mit Funktionen verwenden möchten, die von erweiterten Geräten unterstützt werden.

Das Menü **Container** enthält Optionen, mit denen Sie eine Wiedergabeliste oder ein Album erstellen können. Um eine Wiedergabeliste zu erstellen, wählen Sie mindestens ein Titel auf dem Gerät aus, und klicken Sie im Menü **Container** auf **Wiedergabeliste erstellen** . Diese Funktion funktioniert nur auf MTP-Geräten, da der Code nur die Erstellung einer "virtuellen" Wiedergabelisten Datei unterstützt. (Eine virtuelle Wiedergabeliste ist eine Wiedergabeliste, die nur durch Metadatenwerte angegeben wird, und nicht durch eine physische Datei (z. b. eine WPL-Datei). Das Gerät muss leere Wiedergabelisten unterstützen, um dieses Feature verwenden zu können.

Wenn Sie ein Album (eine Wiedergabeliste mit zugeordneter Grafik) erstellen möchten, wählen Sie ein oder mehrere Titel auf dem Gerät aus, und klicken Sie im Menü **Container** auf **Album erstellen** . Mit einem Dialogfeld können Sie eine Bilddatei auf Ihrem Computer suchen, die dem Album zugeordnet werden soll. Ähnlich wie bei der Erstellung von Wiedergabelisten erstellt die Anwendung eine "leere" Album Datei. Wenn das Gerät keine leeren Alben unterstützt, funktioniert diese Funktion nicht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiel für eine Desktop Anwendung**](sample-desktop-application.md)
</dt> </dl>

 

 




