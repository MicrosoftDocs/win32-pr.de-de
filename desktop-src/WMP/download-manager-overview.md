---
title: Übersicht über den Download-Manager
description: Übersicht über den Download-Manager
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Windows Media Player,Download-Manager
- Onlineshops,Download-Manager
- Typ 2 Onlineshops,Download-Manager
- Windows Media Player online stores,real-time downloading
- Onlineshops,Echtzeitdownloads
- Typ 2 Onlineshops,Echtzeitdownload
- Windows Media Player online stores,background downloading
- Onlineshops,Hintergrunddownloads
- Typ 2 Onlineshops,Hintergrunddownloads
- Windows Media Player,Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Echtzeitdownload
- Hintergrunddownloads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790466db4c09f7c2310729bd6f866bc5066348641a73756eb9199aa685a7fafe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997080"
---
# <a name="download-manager-overview"></a>Übersicht über den Download-Manager

Microsoft Windows Media Player stellt Aufgabenbereiche für Onlineshops mit einem gehosteten Browserfenster zur Verfügung. Über die Onlineshops können Benutzer über das Internet mit Webseiten des Onlineshops interagieren.

Der Windows Media Player-Download-Manager stellt ein Objektmodell bereit, mit dem Sie die Aufgaben verarbeiten können, die mit dem Herunterladen von Inhalten von Microsoft-Internetinformationsdienste (IIS) auf den Computer des Benutzers mithilfe von Hypertext Transfer Protocol (HTTP) verbunden sind. Mit dem Download-Manager können Sie:

-   Verwalten Sie mehrere Downloads gleichzeitig als Sammlung.
-   Geben Sie eine URL für eine Datei an, und starten Sie den Download über HTTP.
-   Fragen Sie den Downloadstatus und den Fortschritt ab.
-   Anhalten, Fortsetzen oder Abbrechen eines Downloads.
-   Geben Sie an, ob ein Download im Hintergrund oder in Echtzeit erfolgt. (Hintergrunddownloads sind nur unter dem Microsoft Windows XP-Betriebssystem verfügbar.) Weitere [Informationen finden Sie unter Informationen zum Herunterladen von im Hintergrund und in Echtzeit.](#about-background-and-real-time-downloading)
-   Geben Sie an, wie Inhalte in der Bibliothek angezeigt werden. Weitere Informationen [finden Sie unter Informationen zur Bibliotheksintegration.](#about-library-integration)

Der Download-Manager ist die Lösung zum Herunterladen von Inhalten aus Skriptcode auf gehosteten Webseiten. Verwenden Sie zum Herunterladen von Inhalten mit C++-Code Windows XP Background Intelligent Transfer Service (BITS). Weitere Informationen finden Sie unter [BITS](bits.md).

## <a name="about-background-and-real-time-downloading"></a>Informationen zu Hintergrund- und Echtzeitdownloads

Der Download-Manager bietet zwei Arten von Downloads: Hintergrund und Echtzeit. Der typ, den Sie verwenden, liegt bei Ihnen, und es ist möglich, dem Benutzer zu erlauben, auch den Downloadtyp auszuwählen. Wenn Sie dem Benutzer erlauben möchten, den Downloadtyp auszuwählen, müssen Sie die Unterschiede zwischen den beiden verfügbaren Typen erläutern.

Das Herunterladen in Echtzeit erfolgt auf einmal. Wenn der Benutzer einen Dateidownload startet, wird die gesamte Datei in einem einzelnen fortlaufenden Stream auf den Computer des Benutzers übertragen. Der Benutzer kann den Download nicht anhalten oder anderweitig unterbrechen. Wenn der Benutzer entscheidet, Windows Media Player, bevor der Download abgeschlossen ist, verliert er alle unvollständigen Dateien und muss sie von Anfang an herunterladen, um den Inhalt zu erhalten.

Der Hauptvorteil des Echtzeitdownloads ist, dass der Benutzer den Inhalt schneller als das Herunterladen im Hintergrund erhalten kann. Echtzeitdownloads sind für Benutzer von Windows XP verfügbar, aber es ist der einzige Downloadtyp, der in Versionen des Windows-Betriebssystems vor Windows XP verfügbar ist.

Das Herunterladen im Hintergrund erfolgt nach und nach. Wenn der Benutzer einen Hintergrunddownload startet, werden Teile der Datei auf den Computer des Benutzers übertragen, wenn Prozessorzeit verfügbar ist. Es ist möglich, einen Hintergrunddownload anzuhalten und wieder aufzunehmen. Wenn der Benutzer Windows Media Player schließt, bevor der Hintergrunddownload abgeschlossen ist, wird die Bedingung unvollständiger Dateien gespeichert, und der Download kann auch nach einem Neustart des Computers im Hintergrund fortgesetzt werden.

Das Herunterladen im Hintergrund kann länger dauern als das Herunterladen in Echtzeit, da der Downloadvorgang nur erfolgt, wenn der Prozessor keine anderen Aufgaben ausgeführt.

Hintergrunddownloads sind nur verfügbar, wenn Sie Windows XP verwenden.

## <a name="about-library-integration"></a>Informationen zur Bibliotheksintegration

Windows Media Player können Inhalte des Onlineshops in der Bibliothek automatisch organisieren. Um dies zu aktivieren, müssen Sie für jede digitale Mediendatei einen Wert für das **WM/ContentDistributor-Attribut** angeben. Wenn der Bibliothek eine digitale Mediendatei hinzugefügt wird, die bei Verwendung des Download-Managers automatisch erfolgt, wird die Datei automatisch im Knoten Erworbene Musik oder Erworbene **Videos** aufgeführt.  Wenn der Wert für **WM/ContentDistributor** beispielsweise "Proseware" ist und die digitale Mediendatei Musik enthält, wird der Inhalt in der Bibliothek an folgendem Speicherort angezeigt:

Alle Musik/erworbene Musik/Proseware

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Download-Manager**](download-manager.md)
</dt> <dt>

[**DownloadCollection.startDownload**](downloadcollection-startdownload.md)
</dt> </dl>

 

 




