---
description: Erfahren Sie mehr über das Festlegen von Eigenschaften in der ASF-Dateisenke, mit denen eine Anwendung ASF-Mediendaten in einer Datei archivieren kann.
ms.assetid: a47caabd-23e3-4d22-b4b6-5fdb79d62ca1
title: Festlegen von Eigenschaften in der Dateisenke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b6b000ed04c7858251f7388d3edc6a40e0b213
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407513"
---
# <a name="setting-properties-in-the-file-sink"></a>Festlegen von Eigenschaften in der Dateisenke

Die ASF-Dateisenke ist eine Implementierung von [**ABERMEDIASink,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) die von Media Foundation bereitgestellt wird, mit der eine Anwendung ASF-Mediendaten in einer Datei archivieren kann. Informationen zum Objektmodell und zur allgemeinen Verwendung von ASF-Mediensenken finden Sie unter [ASF-Mediensenken.](asf-media-sinks.md)

Nach [dem Erstellen der ASF-Dateisenke](creating-the-asf-file-sink.md)muss sie mit Informationen zu den Datenströmen in der Ausgabedatei konfiguriert werden. Dieses Verfahren wird unter [Hinzufügen von Streaminformationen zur ASF-Dateisenke beschrieben.](adding-stream-information-to-the-asf-file-sink.md) Sie können je nach Codierungstyp zusätzliche Eigenschaften für die Dateisenke festlegen. Leaky Buckets; allgemeine Dateieigenschaften. Diese Einstellungen werden nicht in das endgültige ASF-Headerobjekt geschrieben. In diesem Thema wird beschrieben, wie diese Eigenschaften im Eigenschaftenspeicher der Dateisenke hinzugefügt werden.

Das ContentInfo-Objekt verwaltet die globalen Dateieigenschaften und einzelnen Streameigenschaften für die Dateisenke. Informationen zum Abrufen eines Verweises auf das ASF ContentInfo-Objekt der Dateisenke finden Sie unter [Erstellen der ASF-Dateisenke.](creating-the-asf-file-sink.md)

Um einen Verweis auf den Eigenschaftenspeicher der Dateisenke [**(IPropertyStore)**](/windows/win32/api/propsys/nn-propsys-ipropertystore)zu erhalten, rufen Sie [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) für den Verweis des ContentInfo-Objekts der Dateisenke auf.

## <a name="stream-encoding-properties"></a>Streamcodierungseigenschaften

Um Inhalte ordnungsgemäß zu codieren, muss die Datei bestimmte Codierungsinformationen kennen, z. B. den Codierungstyp und die zugehörigen Codierungsparameter. Diese Werte werden in der Dateisenke als Eigenschaftswerte in einem Eigenschaftenspeicher festgelegt, der vom ASF ContentInfo-Objekt verwaltet wird. Wenn Sie die Dateisenke vor dem Instanziieren der relevanten Encoder konfigurieren, können Sie das ContentInfo-Objekt mit allen aufgefüllten Eigenschaften verwenden, um die Windows Media Encoder zu erstellen. In diesem Fall werden die Eigenschaften automatisch für die instanziierten Encoder festgelegt. Wenn Sie hingegen die Encoder vor der Senke erstellen, stellen Sie sicher, dass die Eigenschaften, die Sie für die Encoder festlegen, in den Eigenschaftenspeicher der Dateisenke kopiert werden.

Zum Festlegen von Codierungseigenschaften benötigen Sie Zugriff auf den Eigenschaftenspeicher der Dateisenke auf Streamebene. Übergeben Sie die Streamnummer im *wStreamNumber-Parameter* der [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore-Methode.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) Die Streamnummern müssen mit den Werten übereinstimmen, die beim Konfigurieren der einzelnen Datenstroms im Profil festgelegt wurden. Eigenschaftswerte werden durch Aufrufen von [**IPropertyStore::SetValue festgelegt.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) In der folgenden Tabelle werden die unterstützten Eigenschaften beschrieben.

Die Eigenschaften hängen vom Typ der Codierung ab. Informationen zu den Eigenschaften und den entsprechenden Werten, die Sie festlegen müssen, finden Sie unter [Codierungseigenschaften](configuring-the-encoder.md).

## <a name="leaky-bucket-property"></a>Leaky Bucket-Eigenschaft

Leaky Bucket-Parameter bestimmen das tatsächliche Pufferfenster, das vom Encoder für den Stream verwendet wird. Die [**MFPKEY \_ ASFSTREAMSINK \_ CORRECTED \_ LEAKYBUCKET-Eigenschaft**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) der Dateisenke enthält die Bucketparameter, die Bitrate, das Pufferfenster und die anfängliche Pufferüberlung. Diese Eigenschaft wird im Eigenschaftenspeicher auf Streamebene für die Dateisenke festgelegt und muss festgelegt werden, nachdem Encoder erstellt und konfiguriert wurden. Dieser Wert wird in der festgelegt. Während der Medientypaushandlung entscheidet der Encoder über das Pufferfenster und die zu verwendende Bitrate. Sie können diese Werte mithilfe der **IWMCodecLeakyBucket-Schnittstelle** erhalten, die in wmcodecifaces.h definiert ist, und Sie müssen eine Verknüpfung mit wmcodecdspuuid.lib erstellen, um deren Methoden aufrufen zu können.

Die abgerufenen Werte können für diese Eigenschaft für jeden Stream in der ASF-Dateisenke festgelegt werden.

## <a name="global-file-sink-properties"></a>Eigenschaften der globalen Dateisenke

Um den globalen Eigenschaftenspeicher der Dateisenke zu erhalten, übergeben Sie 0 im *wStreamNumber-Parameter* der [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore-Methode.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) Eigenschaftswerte werden durch Aufrufen von [**IPropertyStore::SetValue festgelegt.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) In der folgenden Tabelle werden die unterstützten Eigenschaften beschrieben.

| Eigenschaften auf Dateiebene                                                                                | Beschreibung                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFPKEY \_ ASFMEDIASINK \_ BASE \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md)           | Die Sendezeit gibt an, wann die Nutzlast innerhalb des unverlusten Buckets freigegeben wird. Dieser Eigenschaftswert gibt die erste Sendezeit an. Der Multiplexer verwendet diesen Wert, um die nachfolgenden Sendezeiten für die generierten Pakete zu berechnen, und stellt sicher, dass Daten kontinuierlich durch den unverlusten Bucket fließen. |
| [**MFPKEY \_ ASFMEDIASINK \_ AUTOADJUST \_ BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) | Dieser BOOL-Wert gibt an, ob der Multiplexer die Bitrate automatisch anpassen muss, um sicherzustellen, dass die Daten nicht über den unzulätigen Bucket überlaufen.                                                                                                                                                  |
| [**MFPKEY \_ ASFMEDIASINK \_ DRMACTION**](mfpkey-asfmediasink-drmaction-property.md)                    | Dies gibt die DRM-Aktion der ASF-Mediensenke für die Dateigenerierung an. In dieser Version wird nur DRM-Transcodierung unterstützt.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Mediensenken](asf-media-sinks.md)
</dt> <dt>

[ASF-Komponenten auf Pipelineebene](pipeline-layer-asf-components.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
