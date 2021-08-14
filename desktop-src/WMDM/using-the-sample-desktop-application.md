---
title: Verwenden der Beispieldesktopanwendung
description: Verwenden der Beispieldesktopanwendung
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Windows Media Geräte-Manager, Beispiele
- Geräte-Manager, Beispiele
- Desktopanwendungen, Beispiele
- Windows Beispiel für Medien-Geräte-Manager,Desktopanwendung
- beispiel für Geräte-Manager,Desktopanwendung
- Beispiele,Desktopanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b418458c9e6091b3e2002a30afb95abb77919d062667a9667a3aac9d4dad6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584166"
---
# <a name="using-the-sample-desktop-application"></a>Verwenden der Beispieldesktopanwendung

Die Beispieldesktopanwendung ist ein einfaches Fenster mit zwei Schwenken, das Windows Explorer ähnelt. Sie können den Inhalt eines Geräts durchsuchen, indem Sie eine Strukturansicht mit Ordnern im linken Bereich und Dateien im rechten Bereich anzeigen. Der Stamm jeder Ordnerstruktur wird logisch als ein anderes Gerät betrachtet, obwohl sich einige Geräte als mehrere Objekte darstellen können (eines für jeden Stammspeicher). Um die grundlegenden Eigenschaften eines Ordners oder einer Datei zu lesen, klicken Sie mit der rechten Maustaste auf das Objekt, und wählen Sie **Eigenschaften** aus.

Sie können Dateien auf dem Gerät löschen, indem Sie im rechten Bereich eine Datei und im Menü **Datei** die Option **Löschen** auswählen. Um dem Gerät Mediendateien hinzuzufügen, können Sie Dateien vom Desktop in den rechten Bereich des Programms ziehen. Beachten Sie, dass Dateien ein medienformat aufweisen müssen, das vom Gerät unterstützt wird. Dateien in unzulässigen Formaten (Nicht-Mediendateien wie .txt Dateien oder Medienformate, die vom Gerät nicht unterstützt werden) werden nicht an das Gerät gesendet. (Beachten Sie, dass diese Einschränkung die des Programms ist. Windows Mit media Geräte-Manager können Sie beliebige Dateien an ein Gerät senden, wenn das Gerät sie akzeptiert.)

Um Rückrufereignisse zu erfassen, die an die [**IWMDMOperation-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) gesendet werden, müssen Sie die Option "Operation Interface verwenden" im Menü **Optionen** aktivieren.

Im Menü **Optionen** können Sie auch auswählen, ob Sie mehrere erweiterte Schnittstellen mit Features verwenden möchten, die von erweiterten Geräten unterstützt werden.

Das Menü **Container** verfügt über Optionen, mit denen Sie eine Wiedergabeliste oder ein Album erstellen können. Wählen Sie zum Erstellen einer Wiedergabeliste mindestens einen Song auf dem Gerät aus, und klicken Sie im Menü **Container** auf **Wiedergabeliste erstellen.** Dieses Feature funktioniert nur auf MTP-Geräten, da der Code nur die Erstellung einer "virtuellen" Wiedergabelistendatei unterstützt. (Eine virtuelle Wiedergabeliste ist eine Wiedergabeliste, die nur durch Metadatenwerte und nicht durch eine physische Datei angegeben wird, z.B. eine WPL-Datei.) Das Gerät muss leere Wiedergabelisten unterstützen, um dieses Feature verwenden zu können.

Um ein Album (eine Wiedergabeliste mit einem zugeordneten Bild) zu erstellen, wählen Sie mindestens einen Song auf dem Gerät aus, und klicken Sie im Menü **Container** auf **Album erstellen.** Mit einem Dialogfeld können Sie zu einer Bilddatei auf Ihrem Computer navigieren, die dem Album zugeordnet werden soll. Ähnlich wie bei der Erstellung von Wiedergabelisten erstellt die Anwendung eine "leere" Albumdatei. Wenn das Gerät leere Alben nicht unterstützt, funktioniert dieses Feature nicht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispieldesktopanwendung**](sample-desktop-application.md)
</dt> </dl>

 

 




