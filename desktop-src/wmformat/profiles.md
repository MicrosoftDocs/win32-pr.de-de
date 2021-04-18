---
title: Profiles
description: Profiles
ms.assetid: 6e70393f-3dab-4036-8d34-a672ef1795c6
keywords:
- Windows Media-Format-SDK, profile
- Advanced Systems Format (ASF), profile
- ASF (Advanced Systems Format), profile
- Windows Media-Format-SDK, PRX-Dateien
- Advanced Systems Format (ASF), PRX-Dateien
- ASF (Advanced Systems Format), PRX-Dateien
- Windows Media-Format-SDK, Profil-Editor
- Advanced Systems Format (ASF), Profil-Editor
- ASF (Advanced Systems Format), Profil-Editor
- PRX-Dateien
- PRX "-Dateien
- Profil-Editor
- Windows Media Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de244445a7c1301c7a14ef273b81ac9fd9cbfb62
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338244"
---
# <a name="profiles"></a>Profiles

Bei einem Profil handelt es sich um eine Sammlung von Daten, die die Konfiguration einer ASF-Datei beschreibt. Ein Profil muss mindestens Konfigurationseinstellungen für einen einzelnen Stream enthalten.

Die Datenstrom Informationen in einem Profil enthalten die Bitrate, das Puffer Fenster und die Medien Eigenschaften für den Datenstrom. Die streaminformationen für Audiodaten und Videos beschreiben genau, wie die Medien in der Datei konfiguriert werden, einschließlich des Codecs, der zum Komprimieren der Daten verwendet wird.

Ein Profil enthält außerdem Informationen zu den verschiedenen Funktionen der ASF-Datei, die in Dateien verwendet werden, die mit diesem erstellt werden. Dazu zählen [gegenseitiger Ausschluss](mutual-exclusion.md), [streampriorisierung](stream-prioritization.md), [Bandbreiten Freigabe](bandwidth-sharing.md)und [Dateneinheiten Erweiterungen](data-unit-extensions.md).

In früheren Versionen des SDK für den Windows Media-Format wurden vorkonfigurierte Systemprofile bereitgestellt, die verwendet werden können, um gängige Dateitypen zu erstellen oder leicht entsprechend den Anforderungen Ihrer Anwendung geändert zu werden. System Profile werden für die Codecs der Windows Media 9-Serie nicht unterstützt. Dies liegt daran, dass die Anzahl der "gängigen" Dateitypen mit dem Hinzufügen neuer Features exponentiell vergrößert wurde. Es wird erwartet, dass praktisch jeder Inhaltsersteller über die einfachen Lösungen hinausgeht, die von Systemprofilen bereitgestellt werden. Sie können weiterhin die alten Systemprofile als Ausgangspunkt verwenden. Weitere Informationen finden Sie unter [Verwenden von System Profilen](using-system-profiles.md).

Sie müssen dem Writer ein Profil für jede Datei bereitstellen, die Sie schreiben. Sie können ein Profil angeben, das mit dem Writer verwendet werden soll, indem Sie [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile)aufrufen.

Profildaten sind in verschiedenen Formularen vorhanden, die vom SDK für den Windows Media-Format verwendet werden können. Auf Profilinformationen kann auch auf verschiedene Weise zugegriffen werden. Dies kann zu Verwirrung in Bezug auf das Profil und seine Verwendung führen.

Das folgende Diagramm zeigt, wie Profildaten im SDK verwendet werden.

![Diagramm, das den Fluss der Profilinformationen anzeigt.](images/formatsdk01.png)

Profildaten nehmen drei verschiedene Formen auf: Daten, die in einem Profil Objekt in einer Anwendung enthalten sind, eine XML-Datei auf einem Datenträger und Daten im Header einer ASF-Datei. Jede dieser Daten Formen wird als schattiertes Rechteck im Diagramm angezeigt.

## <a name="data-in-a-profile-object"></a>Daten in einem Profil Objekt

Wenn Sie ein Profil bearbeiten, verwenden Sie ein Profil Objekt, das alle Profildaten kapselt. Sie können ein leeres Profil Objekt erstellen, indem Sie das Profil-Manager-Objekt verwenden. Sie können auch das Profil-Manager-Objekt verwenden, um vorhandene Profildaten in ein Profil Objekt zu laden.

Die meisten Profildaten müssen durch die Verwendung von-Objekten, die einzelne Teile des Profils darstellen, hinzugefügt und manipuliert werden. Hierzu gehören Datenstrom-Konfigurationsobjekte, gegenseitige Ausschluss Objekte, freigegebene Bandbreiten Objekte und ein streampriorisierungsobjekt. Jeder dieser Objekttypen kann mithilfe von Methoden im Profil Objekt erstellt werden. Änderungen an diesen Objekten wirken sich erst auf das Profil Objekt aus, wenn Sie eine Methode im Profil Objekt verwenden, um die aktualisierten Daten aus dem anderen Objekt einzuschließen.

## <a name="data-in-an-xml-file"></a>Daten in einer XML-Datei

Profildaten werden auf dem Datenträger in Form einer XML-Datei mit der Dateinamenerweiterung ". PRX" gespeichert. Im Windows Media SDK enthalten ist eine Sammlung von Profilen namens Systemprofilen, die die gängigsten Typen von ASF-Dateien abdecken. System Profile werden in einer Datei mit dem Namen WMSysPr9. PRX gespeichert. (Beachten Sie, dass diese Datei keine Systemprofile für Windows Media 9-Reihen enthält, da das Konzept der Systemprofile nicht mehr verwendet wird.) Wenn Sie Ihre eigenen benutzerdefinierten Profile speichern, müssen Sie Sie in ihren eigenen Dateien speichern.

Sie können das Profil-Manager-Objekt verwenden, um die Daten aus einem Profil Objekt in eine Zeichenfolge von XML-Text zu speichern. Sie können dann beliebige Datei-e/a-Funktionen verwenden, um die Zeichenfolge in einer Datei auf dem Datenträger zu speichern.

## <a name="data-in-the-header-of-an-asf-file"></a>Daten im Header einer ASF-Datei

Der Writer nimmt die Informationen aus dem Profil und verwendet ihn zum Erstellen der Streams, die in den Daten Abschnitt der ASF-Datei gelangen. Der Großteil der Profildaten wird im Header Abschnitt der Datei gespeichert, wenn eine Datei geschrieben wird. Bei der Wiedergabe kann das Reader-Objekt (oder das synchrone Reader-Objekt) auf die Informationen im Header der Datei zugreifen. In diesem Fall erstellt das Lese Objekt ein Profil Objekt und füllt es mit den Daten aus dem Header auf.

Wenn Sie mithilfe des Readers (oder synchronen Readers) auf die Profildaten zugreifen, können Sie die Profilinformationen ändern, aber es gibt keine Möglichkeit, diese Änderungen auf die Datei im Reader anzuwenden. Sie können die Profilinformationen aus einer Datei in einem Reader auf ein Profil in einem Writer anwenden, um eine neue Datei zu erstellen, die die gleichen Einstellungen wie die Datei im Reader hat. In diesem Fall werden alle Änderungen, die Sie an den Profilinformationen vornehmen, bevor Sie das Profil im Writer festlegen, in den vom Writer registrierten Profilinformationen berücksichtigt.

## <a name="using-profile-editor"></a>Verwenden des Profil-Editors

Anstatt Profile mithilfe des Windows Media SDK zu erstellen, können Sie den Profil-Editor verwenden, ein Dienstprogramm, das in Windows Media Encoder enthalten ist. Verwenden Sie in der Codierungs Anwendung die **iwmprofilemanager:: loadprofilebydata** -Methode, um das gespeicherte Profil zu laden. In einigen Szenarien, z. b. Wenn Sie eine begrenzte Anzahl von Profilen verwenden, die nie dynamisch geändert werden, ist es möglicherweise bequemer, den Profil-Editor zum Erstellen ihrer Profile zu verwenden.

Wenn Sie jedoch den Profil-Editor verwenden, empfiehlt es sich, die Einstellung "Videogröße: identisch mit Videoeingabe" nicht zu verwenden. Wenn dieses Kontrollkästchen aktiviert ist, erstellt der Profil-Editor ein Profil, bei dem die Videoausgabe Höhe und-Breite auf 0 (null) festgelegt ist. Wenn in Windows Media Encoder diese Profile gefunden werden, werden die korrekten Werte so festgelegt, dass Sie mit der Videoeingabe identisch sind. Der Writer im Windows Media-Format SDK führt dies jedoch nicht automatisch aus. Daher müssen Sie sicherstellen, dass die Video Frame Größe von der Anwendung festgelegt wird, wenn das Profil keine hat.

**Hinweis** Einige Datenstrom-Konfigurationselemente werden nicht im Profil gespeichert. Die Daten im Profil beschreiben das Format der fertigen ASF-Datei. Eingabemedien Eigenschaften und andere Konfigurationsdaten, die vom Writer-Objekt zum Konfigurieren der Codecs verwendet werden, werden nicht im Profil gespeichert. Dies schließt alle Eigenschaften ein, die mithilfe der [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) -Methode festgelegt wurden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Bandbreiten Freigabe Objekt**](bandwidth-sharing-object.md)
</dt> <dt>

[**Konzepte**](concepts.md)
</dt> <dt>

[**Iwmprofile-Schnittstelle**](iwmprofile.md)
</dt> <dt>

[**Iwmprofilemanager-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Gegenseitiges Ausschluss Objekt**](mutual-exclusion-object.md)
</dt> <dt>

[**Profil-Manager-Objekt**](profile-manager-object.md)
</dt> <dt>

[**Stream-Konfigurationsobjekt**](stream-configuration-object.md)
</dt> <dt>

[**Streampriorisierungsobjekt**](stream-prioritization-object.md)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 




