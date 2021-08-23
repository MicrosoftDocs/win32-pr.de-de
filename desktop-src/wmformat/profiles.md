---
title: Profiles
description: Profiles
ms.assetid: 6e70393f-3dab-4036-8d34-a672ef1795c6
keywords:
- Windows Medienformat-SDK, Profile
- Advanced Systems Format (ASF),profiles
- ASF (Advanced Systems Format), Profiles
- Windows Medienformat-SDK,PRX-Dateien
- ASF-Dateien (Advanced Systems Format), PRX-Dateien
- ASF (Advanced Systems Format), PRX-Dateien
- Windows Medienformat-SDK, Profil-Editor
- Advanced Systems Format (ASF), Profil-Editor
- ASF (Advanced Systems Format), Profil-Editor
- PRX-Dateien
- PRX-Dateien
- Profil-Editor
- Windows Media Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a89c06f031c9cf8214888efb35f2986135f88207fc94a631e1e111c94ce16d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707414"
---
# <a name="profiles"></a>Profiles

Ein Profil ist eine Sammlung von Daten, die die Konfiguration einer ASF-Datei beschreibt. Ein Profil muss mindestens Konfigurationseinstellungen für einen einzelnen Stream enthalten.

Die Streaminformationen in einem Profil enthalten die Bitrate, das Pufferfenster und die Medieneigenschaften für den Stream. Die Streaminformationen für Audio und Video beschreiben genau, wie die Medien in der Datei konfiguriert werden, einschließlich des Codecs (falls möglich), der zum Komprimieren der Daten verwendet wird.

Ein Profil enthält auch Informationen zu den verschiedenen ASF-Dateifeatures, die in mit ihm erstellten Dateien verwendet werden. Dazu gehören [gegenseitiger Ausschluss,](mutual-exclusion.md) [Streampriorisierung,](stream-prioritization.md) [Bandbreitenfreigabe](bandwidth-sharing.md)und [Dateneinheitserweiterungen.](data-unit-extensions.md)

Frühere Versionen des Windows Media Format SDK stellten vorkonfigurierte Systemprofile bereit, die zum Erstellen gängiger Dateitypen verwendet oder geringfügig an die Anforderungen Ihrer Anwendung angepasst werden konnten. Systemprofile werden für die Codecs der Windows Media 9-Serie nicht unterstützt. Dies liegt daran, dass die Anzahl der "gängigen" Dateitypen mit dem Zusatz neuer Features exponentiell gestiegen ist. Es wird erwartet, dass praktisch jeder Inhaltsersteller Anforderungen hat, die über die einfachen Lösungen hinausgehen, die von Systemprofilen bereitgestellt werden. Sie können weiterhin die alten Systemprofile als Ausgangspunkt verwenden. Weitere Informationen finden Sie unter [Verwenden von Systemprofilen.](using-system-profiles.md)

Sie müssen dem Writer für jede Datei, die Sie schreiben, ein Profil geben. Sie können ein Profil angeben, das mit dem Writer verwendet werden soll, indem [**Sie IWMWriter::SetProfile aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile)

Profildaten sind in verschiedenen Formen vorhanden, die vom Windows Media Format SDK verwendet werden können. Auf Profilinformationen kann auch auf verschiedene Weise zugegriffen werden. Dies kann zu Verwirrung darüber führen, was ein Profil ist und wie es verwendet wird.

Das folgende Diagramm zeigt, wie Profildaten im SDK verwendet werden.

![Diagramm, das den Fluss der Profilinformationen zeigt.](images/formatsdk01.png)

Profildaten haben drei verschiedene Formen: Daten, die in einem Profilobjekt in einer Anwendung enthalten sind, eine XML-Datei auf dem Datenträger und Daten im Header einer ASF-Datei. Jede dieser Datenformen wird im Diagramm als schattiertes Rechteck angezeigt.

## <a name="data-in-a-profile-object"></a>Daten in einem Profilobjekt

Wenn Sie ein Profil bearbeiten, verwenden Sie ein Profilobjekt, das alle Profildaten kapselt. Sie können ein leeres Profilobjekt erstellen, indem Sie das Profil-Manager-Objekt verwenden. Sie können auch das Profil-Manager-Objekt verwenden, um vorhandene Profildaten in ein Profilobjekt zu laden.

Die meisten Profildaten müssen mithilfe von -Objekten hinzugefügt und bearbeitet werden, die einzelne Teile des Profils darstellen. Dazu gehören Streamkonfigurationsobjekte, Objekte für gegenseitigen Ausschluss, Objekte zur Bandbreitenfreigabe und ein Streampriorisierungsobjekt. Jeder dieser Objekttypen kann mithilfe von Methoden im Profilobjekt erstellt werden. Das Vornehmen von Änderungen an diesen Objekten wirkt sich erst dann auf das Profilobjekt aus, wenn Sie eine Methode im Profilobjekt verwenden, um die aktualisierten Daten aus dem anderen Objekt ein include.

## <a name="data-in-an-xml-file"></a>Daten in einer XML-Datei

Profildaten werden auf dem Datenträger in Form einer XML-Datei mit der Dateierweiterung PRX gespeichert. Im Lieferumfang des Windows Media Format SDK ist eine Sammlung von Profilen enthalten, die als Systemprofile bezeichnet werden und die gängigsten Typen von ASF-Dateien abdecken. Systemprofile werden in einer Datei namens WMSysPr9.prx gespeichert. (Beachten Sie, dass diese Datei tatsächlich keine Systemprofile für Windows Media 9-Serie enthält, da das Konzept der Systemprofile nicht mehr verwendet wird.) Wenn Sie Ihre eigenen benutzerdefinierten Profile speichern, müssen Sie sie in Ihren eigenen Dateien speichern.

Sie können das Profil-Manager-Objekt verwenden, um die Daten aus einem Profilobjekt in einer Zeichenfolge mit XML-Text zu speichern. Sie können dann die datei-E/A-Funktionen verwenden, die Sie verwenden möchten, um die Zeichenfolge in einer Datei auf dem Datenträger zu speichern.

## <a name="data-in-the-header-of-an-asf-file"></a>Daten im Header einer ASF-Datei

Der Writer verwendet die Informationen aus dem Profil, um die Datenströme zu erstellen, die in den Datenabschnitt der ASF-Datei wechseln. Der Großteil der Profildaten wird beim Schreiben einer Datei im Headerabschnitt der Datei gespeichert. Bei der Wiedergabe kann das Readerobjekt (oder das synchrone Readerobjekt) auf die Informationen im Header der Datei zugreifen. In diesem Fall erstellt das Leseobjekt ein Profilobjekt und füllt es mit den Daten aus dem Header auf.

Wenn Sie mithilfe des Readers (oder synchronen Readers) auf die Profildaten zugreifen, können Sie Änderungen an den Profilinformationen vornehmen, aber es gibt keine Möglichkeit, diese Änderungen auf die Datei im Reader anzuwenden. Sie können die Profilinformationen aus einer Datei in einem Reader auf ein Profil in einem Writer anwenden, um eine neue Datei mit den gleichen Einstellungen wie die Datei im Reader zu erstellen. In diesem Fall werden alle Änderungen, die Sie vor dem Festlegen des Profils im Writer an den Profilinformationen vornehmen, in den vom Writer registrierten Profilinformationen widergespiegelt.

## <a name="using-profile-editor"></a>Verwenden des Profil-Editors

Anstatt Profile mit dem Windows Media Format SDK zu erstellen, können Sie den Profil-Editor verwenden, ein Hilfsprogramm, das in Windows Media Encoder enthalten ist. Verwenden Sie in Ihrer Codierungsanwendung **die IWMProfileManager::LoadProfileByData-Methode,** um das gespeicherte Profil zu laden. In einigen Szenarien, z. B. wenn Sie eine begrenzte Anzahl von Profilen verwenden, die nie dynamisch geändert werden, ist es möglicherweise praktischer, den Profil-Editor zum Erstellen Ihrer Profile zu verwenden.

Wenn Sie jedoch den Profil-Editor verwenden, wird empfohlen, die Einstellung "Videogröße: Identisch mit Videoeingabe" nicht zu verwenden. Wenn dieses Kontrollkästchen aktivieren ist, erstellt der Profil-Editor ein Profil, bei dem die Höhe und Breite der Videoausgabe auf 0 (null) festgelegt ist. Wenn Windows Media Encoder auf diese Profile trifft, legt er die richtigen Werte für die Videoeingabe fest. Der Writer im Windows Media Format SDK führt dies jedoch nicht automatisch durch. Daher müssen Sie sicherstellen, dass Ihre Anwendung die Größe des Videoframes in Fällen fest legt, in denen das Profil keine hat.

**Hinweis:** Einige Streamkonfigurationselemente werden nicht im Profil gespeichert. Die Daten im Profil beschreiben das Format der fertigen ASF-Datei. Eingabemedieneigenschaften und andere Konfigurationsdaten, die vom Writer-Objekt zum Konfigurieren der Codecs verwendet werden, werden nicht im Profil gespeichert. Dies schließt alle Eigenschaften ein, die mithilfe der [**IWMPropertyVault::SetProperty-Methode festgelegt**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) wurden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Bandwidth Sharing Object**](bandwidth-sharing-object.md)
</dt> <dt>

[**Konzepte**](concepts.md)
</dt> <dt>

[**IWMProfile-Schnittstelle**](iwmprofile.md)
</dt> <dt>

[**IWMProfileManager-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Objekt für gegenseitigen Ausschluss**](mutual-exclusion-object.md)
</dt> <dt>

[**Profil-Manager-Objekt**](profile-manager-object.md)
</dt> <dt>

[**Stream-Konfigurationsobjekt**](stream-configuration-object.md)
</dt> <dt>

[**Streampriorisierungsobjekt**](stream-prioritization-object.md)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 




