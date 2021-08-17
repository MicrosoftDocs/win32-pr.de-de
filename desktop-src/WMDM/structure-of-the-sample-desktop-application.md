---
title: Struktur der Beispieldesktopanwendung
description: Struktur der Beispieldesktopanwendung
ms.assetid: e042470d-dc78-488c-bcad-2e8d34714d5d
keywords:
- Windows Medien Geräte-Manager,Beispiele
- Geräte-Manager,Beispiele
- Desktopanwendungen,Beispiele
- Windows Beispiel für Geräte-Manager,Desktopanwendung
- Geräte-Manager,Desktopanwendungsbeispiel
- Beispiele,Desktopanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dde8250a5efc8bc0f0b9582739bd8770d95ee586ea571a43bcbb9be69e8774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957160"
---
# <a name="structure-of-the-sample-desktop-application"></a>Struktur der Beispieldesktopanwendung

Die Beispieldesktopanwendung besteht aus zwei Hauptteilen:

-   Das wmdapp-Projekt enthält die meisten Klassen, die die Benutzeroberfläche anzeigen, ziehen und ablegen und alle erforderlichen Funktionen des Programms ausführen.
-   Das Proghelp-Projekt ist eine Hilfsanwendung, die nicht wichtige Klassen enthält, um Statusbenachrichtigungen und manuelle Dateiübertragungen vom Desktop an die Anwendung zu verarbeiten.

Die ausführbare Datei verwendet das Hilfsprojekt nur, wenn  der Benutzer im Menü Optionen die Option Operation **Interface** verwenden auswählt, um die manuelle Dateiübertragung an das Gerät zu verarbeiten und die Statusleiste im Downloadstatusformular zu erhöhen. Der Rest der Anwendung wird im wmdapp-Projekt verarbeitet.



| Klasse                | Datei                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| —                    | wmdmapp.cpp             | Die Klasse, die das übergeordnete Fenster der Benutzeroberfläche behandelt. Der Code in dieser Datei verarbeitet auch einige Benutzereingaben, die nicht von CDevFiles verarbeitet werden, z. B. das Erstellen einer Wiedergabeliste oder eines Albums auf einem Gerät, das Löschen von Dateien und das Registrieren von Menüoptionen.                                                                                                                                                    |
| CDevices             | Devices.cpp             | Die Klasse, die den linken Bereich des Hauptanwendungsfensters behandelt, in dem die verfügbaren Geräte aufgeführt sind. Diese Klasse verwaltet die Messagingschleife, die Benutzereingaben verarbeitet, z. B. das Auswählen eines Geräts und das Benachrichtigen des Bereichs CDevFiles, um die entsprechenden Dateien zu laden, wenn sich die Geräteauswahl geändert hat.                                                                              |
| CDevFiles            | Devfiles.cpp            | Die Klasse, die den rechten Bereich des Hauptanwendungsfensters behandelt, in dem die Dateien auf dem ausgewählten Gerät aufgelistet sind. Diese Klasse verwaltet die Messagingschleife und verarbeitet Benutzereingaben wie das Ziehen von Dateien auf das Gerät und das Löschen von Dateien vom Gerät.                                                                                                                          |
| CStatus              | Status.cpp              | Die Klasse, die die untere Statusleiste im Hauptfenster behandelt, in der die Anzahl der Geräte und Dateien aufgeführt ist, sowie die Menge an freiem und genutzten Arbeitsspeicher auf dem ausgewählten Gerät.                                                                                                                                                                                                         |
| CWMDM                | Wmdevmgr.cpp            | Die Schnittstelle der obersten Ebene für Windows Media Geräte-Manager. Diese Klasse verarbeitet die Authentifizierung, ruft die **IWMDeviceManager-Schnittstelle** der obersten Ebene ab und registriert sich für Benachrichtigungen mit **der IWMDMNotification-Schnittstelle.**                                                                                                                                                                  |
| CProgress            | Progress.cpp            | Die -Klasse im Hauptanwendungsprojekt, die das Dialogfeld erstellt und verwaltet, das den Fortschritt eines Ereignisses zeigt.                                                                                                                                                                                                                                                                             |
| CItemData            | ItemData.cpp            | Eine Wrapperklasse, die einen Zeiger auf einen Speicher (wenn sie eine Datei oder einen Ordner auf dem Gerät darstellt) oder ein Gerät (wenn es ein Gerät darstellt) sowie eine Vielzahl von Informationen über das Objekt enthält, einschließlich Größe und Attribute.                                                                                                                                                                  |
| CNotificationHandler | Notificationhandler.cpp | Verarbeitet Benachrichtigungen zum Ein- und Entfernen von Geräten durch Warnungen im Fenster "CGeräte".                                                                                                                                                                                                                                                                                                               |
| CProgressHelper      | ProgressHelper.cpp      | Erstellt von CDevFiles in lokalen Funktionen zum Empfangen von Benachrichtigungen von Windows Media Geräte-Manager durch Implementierung **von IWMDMProgress**. Sie wird von der CProgress-Klasse verwendet, um die Anzahl der Balken in der Statusleiste und den Abschluss einer Aktion zu bestimmen. Diese Klasse ist als COM-Objekt definiert, das die SDK-Schnittstelle **IWMDMProgress** und eine benutzerdefinierte Schnittstelle IWMDMProgressHelper verfügbar macht. |
| COperationHelper     | Operationhelper.cpp     | Diese Klasse implementiert **IWMDMOperation, um** die manuelle Übertragung von Dateien zu verarbeiten. Es ist multithreaded, um die asynchrone Ausführung zu ermöglichen, und ist als COM-Objekt definiert, das eine benutzerdefinierte Schnittstelle ( IWMDMOperationHelper) verfügbar macht, um die Klasse zu instanziieren und zu initialisieren. Diese Klasse wird nur verwendet, wenn der Benutzer im Menü Optionen die Option "Operation Interface **verwenden"** auswählt.                            |



 

In den folgenden Listen werden die grundlegenden Schritte beschrieben, die für verschiedene Benutzeraktionen durchgeführt werden:

**Beim Start**

Die folgenden Hauptschritte erfolgen, wenn die Beispielanwendung gestartet wird.

1.  Die globale CWMDM-Variable wird instanziiert und authentifiziert und registriert sich für den Empfang von Benachrichtigungen.
2.  Eine globale CDevices-Instanz wird instanziiert, und CDevices::Create wird aufgerufen, um den Gerätebereich zu erstellen und zu füllen.
3.  Eine globale CDevFiles-Instanz wird instanziiert, und CDevFiles::Create wird aufgerufen, um den Dateibereich zu erstellen (der erst aufgefüllt wird, wenn der Benutzer ein Gerät auswählt).
4.  Ein globaler CStatus wird instanziiert, und CStatus::Create wird aufgerufen, um die Statusleiste zu instanziieren.
5.  \_OnViewRefresh durchlistet alle Geräte und initialisiert und fügt CDevices alle Geräte (CItemData) hinzu und aktualisiert die Statusleiste, um die Anzahl der Geräte anzuzeigen.
6.  CDevices::AddItem fügt das Element der Strukturansicht hinzu, die die Geräte darstellt, mit einem Zeiger auf sich selbst als TVITEM.lparam. Alle CDevice-Objekte (Geräte) und CDevFiles-Objekte (Datei) werden in diesem Member des Treeview-Knotens im entsprechenden Fenster gespeichert.

**Beim Auswählen eines Geräts**

Die folgenden Hauptschritte erfolgen, wenn der Benutzer im linken Bereich des Anwendungsfensters ein Gerät auswählt.

1.  Das CDevices-Fenster fängt einen Klick ab und veröffentlicht eine WM \_ DRM \_ UPDATEDEVICE-Meldung an sich selbst.
2.  CDevices empfängt eine eigene Nachricht und ruft UpdateSelection auf. Dies weist das globale CDevFiles-Objekt an, alles zu löschen, alle Elemente der obersten Ebene auf dem Gerät aufzählen und CDevFiles::AddItem aufrufen, um diese elemente dem Dateibereich hinzuzufügen.
3.  Schließlich ruft CDevices CDevFiles::UpdateStatusBar auf, um die Statusleiste mit den richtigen Geräte- und Dateiinformationen zu aktualisieren.

**Beim Erstellen einer Wiedergabeliste**

Nach dem Klicken auf "Wiedergabeliste erstellen" im Menü **Container** ruft die Anwendung die lokale \_ Funktion OnCreatePlaylist auf, die die folgenden Aktionen ausführt:

1.  Sie können die Anzahl der ausgewählten Elemente aus der globalen CDevFiles-Variablen erhalten.
2.  Rufen Sie die lokale Funktion DlgNamePlaylist auf, um ein Dialogfeld zum Erhalten eines Namens für die Wiedergabeliste zu öffnen.
3.  Rufen Sie CProgress::Create auf, um ein Dialogfeld zu erstellen, in dem der Fortschritt der Aktion angezeigt wird, und legen Sie Parameter für die CProgress-Klasse fest, z. B. Titeltext, Bereich, aktueller Wert und so weiter.
4.  Schleife durch alle ausgewählten Elemente im CDevFiles-Strukturansichtsobjekt, und fordern Sie das CItemData-Objekt an, das jeder ausgewählten Datei in der Strukturansicht zugeordnet ist, und erhöhen Sie die Statusdialogleiste mit jeder Datei. Die Dateien werden einem Array von [**IWMDMStorage-Schnittstellen**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) hinzugefügt.
5.  Erhalten Sie ein Handle für das aktuell ausgewählte Element, und fragen Sie es nach einer [**IWMDMStorageControl3-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) ab, die später zum Erstellen der neuen Wiedergabeliste auf dem Gerät verwendet wird.
6.  Fragen Sie das ausgewählte Objekt [**für IWMDMStorage3 ab,**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3)und rufen Sie [**CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject) auf, um eine neue [**IWMDMMetaData-Schnittstelle zu**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata)erstellen.
7.  Fügen Sie den Formatcode WMDM FORMATCODE ABSTRACTAUDIOVIDEOPLAYLIST der neuen IWMDMMetadata-Schnittstelle hinzu, und erstellen Sie eine Wiedergabeliste auf dem Gerät, indem Sie \_ \_ [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)  aufrufen und die Metadatenschnittstelle übergeben. Die -Methode ruft einen Zeiger auf das neue **IWMDMStorage auf** dem Gerät ab.
8.  Füllen Sie die Wiedergabeliste aus, indem Sie den neuen Speicher für [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4)abfragen und [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences)aufrufen und das Array der **IWMDMStorage-Zeiger** übergeben, die in Schritt 4 gesammelt wurden.
9.  Erstellen Sie abschließend ein neues CItemData-Objekt, um die neue Wiedergabeliste auf dem Gerät zu speichern, initialisieren Sie sie mit dem neuen Speicher, und rufen Sie CDevFiles::AddItem auf, um sie dem Bereich CDevFiles hinzuzufügen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beispieldesktopanwendung**](sample-desktop-application.md)
</dt> </dl>

 

 




