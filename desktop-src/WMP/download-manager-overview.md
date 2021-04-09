---
title: 'Download-Manager: Übersicht'
description: 'Download-Manager: Übersicht'
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Windows Media Player Online Stores, Download-Manager
- Online Stores, Download-Manager
- Typ 2 Online Stores, Download-Manager
- Windows Media Player Online Stores, Echt Zeit Downloads
- Online Stores, Echt Zeit Downloads
- Typ 2 Online Stores, Echt Zeit Download
- Windows Media Player Online Stores, herunterladen im Hintergrund
- Online Stores, herunterladen im Hintergrund
- Typ 2 Online Stores, herunterladen im Hintergrund
- Windows Media Player, Download-Manager
- Windows Media Player Download-Manager
- Download-Manager
- Herunterladen in Echtzeit
- Herunterladen im Hintergrund
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037507"
---
# <a name="download-manager-overview"></a>Download-Manager: Übersicht

Microsoft Windows Media Player bietet Aufgabenbereiche im Online Store, die ein gehostetes Browserfenster enthalten. Über die Online Stores können Benutzer über das Internet mit Webseiten im Online Store interagieren.

Der Windows Media Player Download-Manager stellt ein Objektmodell bereit, das Sie verwenden können, um die Aufgaben für das Herunterladen von Inhalten auf dem Computer des Benutzers von Microsoft Internetinformationsdienste (IIS) mithilfe von Hypertext Transfer Protocol (http) zu verarbeiten. Mit dem Download-Manager können Sie folgende Aktionen ausführen:

-   Gleichzeitiges Verwalten mehrerer Downloads als Sammlung
-   Geben Sie eine URL für eine Datei an, und starten Sie Sie mit http.
-   Fragen Sie den Download Status und den Fortschritt ab.
-   Anhalten, fortsetzen oder Abbrechen eines Downloads.
-   Geben Sie an, ob ein Download im Hintergrund oder in Echtzeit stattfinden soll. (Das Herunterladen im Hintergrund ist nur unter dem Betriebssystem Microsoft Windows XP verfügbar.) Weitere Informationen finden Sie unter [Informationen zu Hintergrund und Echt Zeit Downloads](#about-background-and-real-time-downloading).
-   Geben Sie an, wie Inhalt in der Bibliothek angezeigt wird. [Informationen zur Bibliotheks Integration](#about-library-integration)finden Sie unter.

Der Download-Manager ist die Lösung für das Herunterladen von Inhalten aus Skriptcode in gehosteten Webseiten. Zum Herunterladen von Inhalten mithilfe von C++-Code verwenden Sie Windows XP Background Intelligent Transfer Service (Bits). Weitere Informationen finden Sie unter [Bits](bits.md).

## <a name="about-background-and-real-time-downloading"></a>Informationen zu Hintergrund-und Echt Zeit Downloads

Der Download-Manager bietet zwei Arten von Downloads: Hintergrund und Echt Zeit. Welchen Typ Sie verwenden, ist Ihnen überlassen, und es ist möglich, dem Benutzer auch das Auswählen des Download Typs zu ermöglichen. Wenn Sie dem Benutzer die Auswahl des Download Typs gestatten, sollten Sie die Unterschiede zwischen den beiden verfügbaren Typen erläutern.

Der Echt Zeit Download erfolgt gleichzeitig. Wenn der Benutzer einen Datei Download startet, wird die gesamte Datei in einem einzigen kontinuierlichen Stream auf den Computer des Benutzers übertragen. Der Benutzer kann den Download nicht anhalten oder anderweitig unterbrechen. Wenn der Benutzer Windows Media Player schließen möchte, bevor der Download abgeschlossen ist, verliert er alle unvollständigen Dateien und muss Sie von Anfang an herunterladen, um den Inhalt zu erhalten.

Der Hauptvorteil von Echt Zeit Downloads besteht darin, dass der Benutzer den Inhalt schneller als das Herunterladen im Hintergrund abrufen kann. Das Herunterladen in Echtzeit ist für Benutzer von Windows XP verfügbar, aber es ist die einzige Art von Download, die unter Versionen des Windows-Betriebssystems vor Windows XP verfügbar ist.

Das Herunterladen im Hintergrund erfolgt schrittweise. Wenn der Benutzer einen Download im Hintergrund startet, werden Teile der Datei auf den Computer des Benutzers übertragen, wenn die Prozessorzeit verfügbar ist. Es ist möglich, einen Hintergrund Download anzuhalten und fortzusetzen. Wenn sich der Benutzer für das Schließen von Windows-Media Player entscheidet, bevor das Herunterladen des Hintergrunds abgeschlossen ist, wird die Bedingung aller unvollständigen Dateien gespeichert, und der Download kann im Hintergrund fortgesetzt werden, auch nachdem der Computer neu gestartet wurde.

Das Herunterladen im Hintergrund kann länger dauern als das Herunterladen in Echtzeit, da der Downloadvorgang nur erfolgt, wenn der Prozessor keine anderen Tasks ausführt.

Das Herunterladen im Hintergrund ist nur bei Verwendung von Windows XP verfügbar.

## <a name="about-library-integration"></a>Informationen zur Bibliotheks Integration

Windows Media Player kann Online Store-Inhalte in der Bibliothek automatisch organisieren. Um dies zu ermöglichen, müssen Sie für jede digitale Mediendatei einen Wert für das Attribut " **WM/contentdistributor** " angeben. Wenn der Bibliothek eine digitale Mediendatei hinzugefügt wird, die automatisch bei Verwendung des Download-Managers erfolgt, wird die Datei automatisch im Knoten **erworbene Musik** oder **erworbene Videos** aufgeführt. Wenn der Wert für **WM/contentdistributor** beispielsweise "Proseware" lautet und die digitale Mediendatei Musik enthält, wird der Inhalt in der Bibliothek am folgenden Speicherort angezeigt:

Alle Musik/erworbenen Musik/Proseware

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Download-Manager**](download-manager.md)
</dt> <dt>

[**Download Collection. startDownload**](downloadcollection-startdownload.md)
</dt> </dl>

 

 




