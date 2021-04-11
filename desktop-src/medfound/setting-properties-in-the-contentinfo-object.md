---
description: Beim Erstellen einer ASF-Datei muss das ContentInfo-Objekt die Merkmale des Medien Inhalts kennen, damit die verschiedenen Header Objekte mit den richtigen Werten aufgefüllt werden.
ms.assetid: 30e3c10b-1310-4194-8b83-221dfe73b03c
title: Festlegen von Eigenschaften im ContentInfo-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e386d5eb33dd1893b195a870425b2336ab9c316f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130473"
---
# <a name="setting-properties-in-the-contentinfo-object"></a>Festlegen von Eigenschaften im ContentInfo-Objekt

Beim Erstellen einer ASF-Datei muss das ContentInfo-Objekt die Merkmale des Medien Inhalts kennen, damit die verschiedenen Header Objekte mit den richtigen Werten aufgefüllt werden.

-   [Inhalts bezogene Einstellungen im ContentInfo-Objekt](#content-related-settings-in-the-contentinfo-object)
-   [Konfigurieren des ContentInfo-Objekts mit Encodereinstellungen](#configuring-the-contentinfo-object-with-encoder-settings)
-   [Zugehörige Themen](#related-topics)

## <a name="content-related-settings-in-the-contentinfo-object"></a>Inhalts bezogene Einstellungen im ContentInfo-Objekt

Inhalts Konfigurationseinstellungen sind Stream-Einstellungen, die im Profil enthalten sind, und geben den Datenstrom Bezeichner, den Medientyp und die Parameter für den Leaky Bucket für die Medien Senke an. Nachdem das Profil für das ContentInfo-Objekt durch Aufrufen von [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)festgelegt wurde, werden diese Werte in das generierte ASF-Header Objekt übernommen. Weitere Informationen zu diesen Einstellungen finden Sie unter [Erstellen und Konfigurieren von ASF-Streams](creating-and-configuring-asf-streams.md).

## <a name="configuring-the-contentinfo-object-with-encoder-settings"></a>Konfigurieren des ContentInfo-Objekts mit Encodereinstellungen

Digitale Medien-oder Videodaten sind komplex und nehmen eine große Menge an Arbeitsspeicher in Rechnung. In den meisten Fällen werden sowohl Audiodaten als auch Videos mithilfe von Encodern komprimiert, bevor Sie zu einer ASF-Datei hinzugefügt werden. In Media Foundation werden Encoder als [Media Foundation Transformationen](media-foundation-transforms.md) (MFTs) mit einer Eingabe und einer Ausgabe implementiert. Sie müssen den Typ des Ausgabe Mediums abhängig vom Medientyp des Eingabedaten Stroms und dem Codierungstyp auswählen, den Sie für die Komprimierung des Datenstroms ausgewählt haben.

Vor der Codierungs Sitzung muss der Encoder konfiguriert werden, indem die relevanten Eigenschaften abhängig vom Codierungstyp festgelegt werden.

Nach dem Konfigurieren des Encoders müssen Sie das ContentInfo-Objekt mit den Encoderwerten konfigurieren, da der [ASF Multiplexer](asf-multiplexer.md) und die ASF-Medien Senke, die mit dem aufgefüllten ContentInfo-Objekt initialisiert werden, Einstellungen wie die Leaky-Bucket-Werte zum Generieren von ASF-Datenpaketen verwenden. Die Werte werden im endgültigen ASF-Header Objekt nicht gespeichert. Die Codierungs Einstellungen werden als Eigenschaften verfügbar gemacht. Gehen Sie folgendermaßen vor, um das ContentInfo-Objekt mit den Codierungs Eigenschaften zu konfigurieren:

1.  Sie können einen Zeiger auf den Eigenschaften Speicher des Encoders abrufen, indem Sie den Encoder ([**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle) direkt für die **IPropertyStore** -Schnittstelle Abfragen.
2.  [**Imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)aufrufen. Um streamspezifische Eigenschaften festzulegen, geben Sie den Datenstrom Bezeichner im *wstreamnumber* -Parameter an. übergeben Sie für Eigenschaften auf Dateiebene 0. Der *ppistore* -Parameter erhält einen Zeiger auf die **IPropertyStore** -Schnittstelle. Der empfangene Eigenschaften Speicher ist leer.
3.  Aufrufen von **IPropertyStore:: GetValue** für den Encoder und Abrufen des Eigenschafts Werts durch Angeben der Eigenschafts Schlüssel Konstanten. Eine umfassende Liste der Codierungs Eigenschaften finden Sie in der [Codec-Programmier Referenz](/previous-versions//aa384554(v=vs.85)).
4.  Aufrufen von **IPropertyStore:: SetValue** für das ContentInfo-Objekt, um die erforderliche Eigenschaft im Eigenschaften Speicher festzulegen.
5.  Wiederholen Sie die Schritte 3 und 4 für jede Eigenschaft, die Sie festlegen möchten.

Die ASF-Medien Senke kann mithilfe eines Aktivierungs Objekts erstellt werden, indem [**mfcreateasfmediasinkaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)aufgerufen wird. Das neue Medien Senk Objekt wird basierend auf den Einstellungen für die Medien Senke konfiguriert, die im Eigenschaften Speicher des ContentInfo-Objekts festgelegt werden können. In der folgenden Tabelle sind die Eigenschaften Konstanten der ASF-Medien Senke aufgeführt.



| Eigenschaft                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**mfpkey \_ asfmediasink- \_ Basis \_ sendtime**](mfpkey-asfmediasink-base-sendtime-property.md)                   | Die Sendezeit gibt an, wann die Nutzlast innerhalb des Lecks "Leaky" freigegeben wird. Dieser Eigenschafts Wert gibt die erste Sende Zeit an. Der Multiplexer verwendet diesen Wert, um die nachfolgenden Sendezeiten für die generierten Pakete zu berechnen, und stellt sicher, dass die Daten kontinuierlich über den Bucket "Leaky" fließen. |
| [**mfpkey \_ asfmediasink \_ autoanpassung- \_ Bitrate**](mfpkey-asfmediasink-autoadjust-bitrate-property.md)         | Dieser **boolesche** Wert gibt an, ob der Multiplexer die Bitrate automatisch anpassen muss, um sicherzustellen, dass die Daten keinen Überlauf des Lecks verursachen.                                                                                                                                              |
| [**mfpkey \_ asfmediasink \_ drmaction**](mfpkey-asfmediasink-drmaction-property.md)                            | Gibt die DRM-Medien-Sink-DRM-Aktion für die Datei Generierung an. In dieser Version wird nur DRM-transcodieren unterstützt.                                                                                                                                                                                   |
| [**mfpkey \_ asfstreamsink \_ korrigiert \_ leakybucket**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) | Diese Eigenschaft muss festgelegt werden, wenn der Encoder entscheidet, welches Puffer Fenster und welche Bitrate verwendet werden sollen. Um diese Werte festzulegen, verwenden Sie die [**iwmcodecleakybucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) -Schnittstelle. Dies muss für jeden Stream in der ASF-Datei festgelegt werden.                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben eines ASF-Header Objekts für eine neue Datei](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 
