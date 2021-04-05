---
title: Struktur der Beispiel-Desktop Anwendung
description: Struktur der Beispiel-Desktop Anwendung
ms.assetid: e042470d-dc78-488c-bcad-2e8d34714d5d
keywords:
- Windows Media Device Manager, Beispiele
- Device Manager, Beispiele
- Desktop Anwendungen, Beispiele
- Windows Media Device Manager, Beispiel für eine Desktop Anwendung
- Beispiel für Device Manager Desktop Anwendung
- Beispiele, Desktop Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34fb377c1bb6ebf943721b55ec6175e65f70ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711118"
---
# <a name="structure-of-the-sample-desktop-application"></a>Struktur der Beispiel-Desktop Anwendung

Die Beispiel-Desktop Anwendung besteht aus zwei Hauptteilen:

-   Das wmdapp-Projekt enthält die meisten Klassen, die die Benutzeroberfläche anzeigen, Drag & amp; Drop verarbeiten und alle erforderlichen Funktionen des Programms ausführen.
-   Das proghelp-Projekt ist eine Hilfsanwendung, die nicht erforderliche Klassen zum Verarbeiten von Status Benachrichtigungen und manuellen Übertragungen von Dateien vom Desktop zur Anwendung enthält.

Die ausführbare Datei verwendet das Hilfsprojekt nur dann, wenn der Benutzer im Menü **Optionen die Option** **use Operation Interface** ausgewählt hat, um die manuelle Dateiübertragung an das Gerät zu verarbeiten und die Statusleiste im Formular zum Herunterladen des Fortschritts zu erhöhen. Der gesamte Rest der Anwendung wird im wmdapp-Projekt behandelt.



| Klasse                | Datei                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| —                    | wmdmapp. cpp             | Die Klasse, die das übergeordnete Fenster der Benutzeroberfläche behandelt. Der Code in dieser Datei verarbeitet auch einige Benutzereingaben, die nicht von cdevfiles behandelt werden, z. b. das Erstellen einer Wiedergabeliste oder eines Albums auf einem Gerät, das Löschen von Dateien und das Registrieren von Menü Optionen.                                                                                                                                                    |
| Cdevices             | Geräte. cpp             | Die Klasse, die den linken Bereich des Haupt Anwendungsfensters behandelt, in dem die verfügbaren Geräte aufgelistet sind. Diese Klasse verwaltet die Messaging Schleife, die Benutzereingaben behandelt, z. b. das Auswählen eines Geräts und das Benachrichtigen des cdevfiles-Bereichs, um die entsprechenden Dateien zu laden, wenn sich die Geräteauswahl geändert hat.                                                                              |
| Cdevfiles            | Devfiles. cpp            | Die Klasse, die den rechten Bereich des Haupt Anwendungsfensters behandelt, in dem die Dateien auf dem ausgewählten Gerät aufgeführt werden. Diese Klasse verwaltet die Messaging Schleife und verarbeitet Benutzereingaben, z. b. das Ziehen von Dateien auf das Gerät und das Löschen von Dateien auf dem Gerät.                                                                                                                          |
| Cstatus              | Status. cpp              | Die Klasse, die die untere Statusleiste im Hauptfenster behandelt, in der die Anzahl der Geräte und Dateien aufgeführt ist, sowie die Menge an freiem und verwendeter Arbeitsspeicher auf dem ausgewählten Gerät.                                                                                                                                                                                                         |
| Cwmdm                | Wmdevmgr. cpp            | Die Oberfläche der obersten Ebene für Windows Media Device Manager. Diese Klasse übernimmt die Authentifizierung, ruft die **iwmdevicemanager** -Schnittstelle der obersten Ebene ab und registriert sich mit der **iwmdmnotification** -Schnittstelle für Benachrichtigungen.                                                                                                                                                                  |
| Cprogress            | "Progress. cpp"            | Die-Klasse im Haupt Anwendungsprojekt, das das Dialogfeld erstellt und verwaltet, das den Fortschritt eines Ereignisses anzeigt.                                                                                                                                                                                                                                                                             |
| Citemdata            | ItemData. cpp            | Eine Wrapper Klasse, die einen Zeiger auf einen Speicher (bei Darstellung einer Datei oder eines Ordners auf dem Gerät) oder ein Gerät (bei Darstellung eines Geräts) enthält, sowie eine Vielzahl von Informationen über das Objekt, einschließlich Größe und Attributen.                                                                                                                                                                  |
| Cnotificationhandler | Notificationhandler. cpp | Behandelt Benachrichtigungen über das eintreffen und Entfernen von Geräten durch Warnung im Fenster "cdevices".                                                                                                                                                                                                                                                                                                               |
| Cprogresshelper      | Progresshelper. cpp      | Wird von cdevfiles in lokalen Funktionen erstellt, um Benachrichtigungen von Windows Media-Device Manager durch Implementieren von **iwmdmprogress** zu empfangen. Sie wird von der cprogress-Klasse verwendet, um die Anzahl der Balken in der Statusanzeige zu ermitteln, und, wenn eine Aktion abgeschlossen ist. Diese Klasse ist als COM-Objekt definiert, das die SDK-Schnittstelle **iwmdmprogress** und eine benutzerdefinierte Schnittstelle iwmdmprogresshelper verfügbar macht. |
| Coperationhelper     | Operationhelper. cpp     | Diese Klasse implementiert **iwmdmoperation** , um die manuelle Übertragung von Dateien zu verarbeiten. Es ist eine Multithread-Schnittstelle, die asynchron auftreten kann. es wird als COM-Objekt definiert, das eine benutzerdefinierte Schnittstelle (iwmdmoperationhelper) verfügbar macht, um die Klasse zu instanziieren und zu initialisieren. Diese Klasse wird nur verwendet, wenn der Benutzer im Menü **Optionen die Option** "Vorgangs Schnittstelle verwenden" auswählt.                            |



 

In den folgenden Listen finden Sie die grundlegenden Schritte, die für verschiedene Benutzeraktionen ausgeführt werden:

**Beim Start**

Die folgenden Hauptschritte werden ausgeführt, wenn die Beispielanwendung gestartet wird.

1.  Die globale cwmdm-Variable wird instanziiert und authentifiziert und wird für den Empfang von Benachrichtigungen registriert.
2.  Globale cdevices werden instanziiert, und cdevices:: Create wird aufgerufen, um den Bereich Geräte zu erstellen und auszufüllen.
3.  Eine globale cdevfiles wird instanziiert, und cdevfiles:: Create wird aufgerufen, um den Bereich Dateien zu erstellen (dieser wird erst aufgefüllt, wenn der Benutzer ein Gerät auswählt).
4.  Ein globaler cstatus wird instanziiert, und cstatus:: Create wird aufgerufen, um die Statusleiste zu instanziieren.
5.  \_Onviewrefresh listet alle Geräte auf und initialisiert und fügt alle Geräte (citemdata) zu cdevices hinzu und aktualisiert die Statusleiste, um die Anzahl der Geräte anzuzeigen.
6.  Cdevices:: AddItem fügt das Element der TreeView-Ansicht, die die Geräte darstellt, mit einem Zeiger auf sich selbst als "tvitem. lParam" hinzu. Alle cdevice-Objekte (Geräte) und cdevfiles-Objekte (Datei) werden in diesem Mitglied des TreeView-Knotens im entsprechenden Fenster gespeichert.

**Beim Auswählen eines Geräts**

Die folgenden Hauptschritte werden ausgeführt, wenn der Benutzer im linken Bereich des Anwendungsfensters ein Gerät auswählt.

1.  Das Fenster "cdevices" fängt einen Klick ein und stellt eine WM- \_ DRM- \_ updatedevice-Nachricht an sich selbst.
2.  Cdevices empfängt eine eigene Nachricht und ruft updateselection auf, das dem globalen cdevfiles-Objekt mitteilt, alles zu löschen, alle Elemente der obersten Ebene im Gerät aufzulisten und cdevfiles:: AddItem aufzurufen, um die einzelnen Elemente dem Bereich Dateien hinzuzufügen.
3.  Zum Schluss ruft cdevices cdevfiles:: updatestatusbar auf, um die Statusleiste mit den richtigen Geräte-und Dateiinformationen zu aktualisieren.

**Beim Erstellen einer Wiedergabeliste**

Nachdem Sie auf "Wiedergabeliste erstellen" im Menü " **Container** " geklickt haben, ruft die Anwendung die lokale Funktion " \_ onupatewiedergabe" auf, die die folgenden Aktionen ausführt:

1.  Die Anzahl ausgewählter Elemente aus der globalen cdevfiles-Variablen erhalten.
2.  Ruft die lokale Funktion dlgnamewiedergabe auf, um ein Dialogfeld zu öffnen, in dem Sie einen Namen für die Wiedergabeliste abrufen können.
3.  Rufen Sie cprogress:: Create auf, um ein Dialogfeld zu erstellen, in dem der Fortschritt der Aktion angezeigt wird, und legen Sie Parameter für die cprogress-Klasse fest, z. b. Titel Text, Bereich, aktueller Wert usw.
4.  Durchlaufen Sie alle ausgewählten Elemente im Struktur Ansichts Objekt der cdevfiles, und fordern Sie das citemdata-Objekt an, das jeder ausgewählten Datei in der Strukturansicht zugeordnet ist. erhöhen Sie die Status Dialogleiste der einzelnen Dateien. Die Dateien werden einem Array von [**iwmdmstorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) -Schnittstellen hinzugefügt.
5.  Rufen Sie ein Handle für das aktuell ausgewählte Element ab, und Fragen Sie es nach einer [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) -Schnittstelle ab, die später zum Erstellen der neuen Wiedergabeliste auf dem Gerät verwendet wird.
6.  Fragen Sie das ausgewählte Objekt nach [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)ab, und rufen Sie [**CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject) auf, um eine neue [**iwmdmmetadata**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)-Schnittstelle zu erstellen.
7.  Fügen Sie den Code "WMDM \_ Formatcode \_ abstractaudiovideoplaylist" zur neuen **iwmdmmetadata** -Schnittstelle hinzu, und erstellen Sie eine Wiedergabeliste auf dem Gerät durch Aufrufen von [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)und übergeben Sie die Metadatenschnittstelle. Die-Methode ruft einen Zeiger auf den neuen **iwmdmstorage** auf dem Gerät ab.
8.  Füllen Sie die Wiedergabeliste aus, indem Sie den neuen Speicher für [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)Abfragen und [**IWMDMStorage4:: abtreferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences)aufrufen. übergeben Sie dabei das in Schritt 4 gesammelte Array von **iwmdmstorage** -Zeigern.
9.  Erstellen Sie abschließend ein neues citemdata-Objekt, das die neue Wiedergabeliste auf dem Gerät enthält, initialisieren Sie es mit dem neuen Speicher, und rufen Sie cdevfiles:: AddItem auf, um es dem Bereich "cdevfiles" hinzuzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispiel für eine Desktop Anwendung**](sample-desktop-application.md)
</dt> </dl>

 

 




