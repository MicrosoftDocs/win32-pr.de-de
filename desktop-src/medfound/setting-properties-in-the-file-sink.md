---
description: Die ASF-Datei Senke ist eine Implementierung von imfmediasink, die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann. Weitere Informationen zum Objektmodell der ASF-Medien senken und zur allgemeinen Verwendung finden Sie unter ASF-Medien senken.
ms.assetid: a47caabd-23e3-4d22-b4b6-5fdb79d62ca1
title: Festlegen von Eigenschaften in der Datei Senke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30af39cf13e88f6edf2a6ab68caac27c2400955a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344399"
---
# <a name="setting-properties-in-the-file-sink"></a>Festlegen von Eigenschaften in der Datei Senke

Die ASF-Datei Senke ist eine Implementierung von [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann. Weitere Informationen zum Objektmodell und zur allgemeinen Verwendung von ASF Medien senken finden Sie unter [ASF-Medien senken](asf-media-sinks.md).

Nach [dem Erstellen der ASF-Datei-Senke](creating-the-asf-file-sink.md)muss Sie mit Informationen zu den Datenströmen in der Ausgabedatei konfiguriert werden. Dieses Verfahren wird unter [Hinzufügen von Datenstrom Informationen zur-Senke der ASF-Datei](adding-stream-information-to-the-asf-file-sink.md)beschrieben. Abhängig vom Codierungstyp können Sie zusätzliche Eigenschaften für die Datei-Senke festlegen. Lecks; allgemeine Dateieigenschaften. Diese Einstellungen werden nicht im endgültigen ASF-Header Objekt geschrieben. In diesem Thema wird beschrieben, wie Sie diese Eigenschaften im Eigenschaften Speicher der Datei Senke hinzufügen.

Das ContentInfo-Objekt verwaltet die globalen Dateieigenschaften und die einzelnen streameigenschaften für die dateisenke. Informationen zum erhalten eines Verweises auf das ASF-ContentInfo-Objekt der Datei Senke finden Sie unter [Erstellen der ASF-Datei-Senke](creating-the-asf-file-sink.md).

Um einen Verweis auf den Eigenschaften Speicher der Datei Senke ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) abzurufen, nennen Sie [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) für den Verweis auf das ContentInfo-Objekt der Datei Senke.

## <a name="stream-encoding-properties"></a>Stream Encoding-Eigenschaften

Um Inhalte ordnungsgemäß zu codieren, muss die Datei bestimmte Codierungsinformationen, z. b. Codierungstyp, und die zugehörigen Codierungs Parameter kennen. Diese Werte werden für die dateisenke als Eigenschaftswerte in einem Eigenschaften Speicher festgelegt, der vom ASF ContentInfo-Objekt verwaltet wird. Wenn Sie die Datei-Senke vor dem Instanziieren der relevanten Encoder konfigurieren, können Sie das ContentInfo-Objekt mit allen aufgefüllten Eigenschaften zum Erstellen der Windows Media Encoder verwenden. In diesem Fall werden die Eigenschaften automatisch auf den instanziierten Encodern festgelegt. Wenn Sie hingegen die Encoder vor der Senke erstellen, stellen Sie sicher, dass die Eigenschaften, die Sie für die Encoder festlegen, in den Eigenschaften Speicher der Datei Senke kopiert werden.

Um Codierungs Eigenschaften festzulegen, benötigen Sie Zugriff auf den Eigenschafts Speicher auf Datenstrom Ebene der Datei Senke. Übergeben Sie die Datenstrom Nummer im *wstreamnumber* -Parameter der [**imfasf ContentInfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) -Methode. Die streamnummern müssen den Werten entsprechen, die beim Konfigurieren der einzelnen Datenströme im Profil festgelegt wurden. Eigenschaftswerte werden durch Aufrufen von [**IPropertyStore:: SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore)festgelegt. In der folgenden Tabelle werden die unterstützten Eigenschaften beschrieben.

Die Eigenschaften sind abhängig vom Codierungstyp. Informationen zu den Eigenschaften und den entsprechenden Werten, die Sie festlegen müssen, finden Sie unter [Codierungs Eigenschaften](configuring-the-encoder.md).

## <a name="leaky-bucket-property"></a>Leaky-Bucket-Eigenschaft

Unechte Bucket-Parameter bestimmen das tatsächliche Puffer Fenster, das vom Encoder für den Stream verwendet wird. Die [**korrigierte mfpkey \_ asfstreamsink \_ \_**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) -Eigenschaft der File-Senke enthält die Leaky-Bucket-Parameter, die Bitrate, das Puffer Fenster und die anfängliche Puffer Auslastung. Diese Eigenschaft wird im Eigenschaften Speicher der Datenstrom Ebene für die Datei Senke festgelegt und muss festgelegt werden, nachdem Encoder erstellt und konfiguriert wurden. Dieser Wert wird in festgelegt. Während der Medientyp Aushandlung entscheidet der Encoder das Puffer Fenster und die zu verwendende Bitrate. Sie können diese Werte über die **iwmcodecleakybucket** -Schnittstelle abrufen, die in wmcodecigesichter. h definiert ist, und Sie müssen eine Verknüpfung mit wmcodecdspuuid. lib herstellen, um die zugehörigen Methoden aufzurufen.

Die abgerufenen Werte können für diese Eigenschaft für jeden Stream in der ASF-Datei-Senke festgelegt werden.

## <a name="global-file-sink-properties"></a>Globale dateisenke-Eigenschaften

Um den globalen Eigenschafts Speicher der Datei Senke zu erhalten, übergeben Sie 0 im *wstreamnumber* -Parameter der [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) -Methode. Eigenschaftswerte werden durch Aufrufen von [**IPropertyStore:: SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore)festgelegt. In der folgenden Tabelle werden die unterstützten Eigenschaften beschrieben.

| Eigenschaften auf Dateiebene                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**mfpkey \_ asfmediasink- \_ Basis \_ sendtime**](mfpkey-asfmediasink-base-sendtime-property.md)           | Die Sendezeit gibt an, wann die Nutzlast innerhalb des Lecks "Leaky" freigegeben wird. Dieser Eigenschafts Wert gibt die erste Sende Zeit an. Der Multiplexer verwendet diesen Wert, um die nachfolgenden Sendezeiten für die generierten Pakete zu berechnen, und stellt sicher, dass die Daten kontinuierlich über den Bucket "Leaky" fließen. |
| [**mfpkey \_ asfmediasink \_ autoanpassung- \_ Bitrate**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) | Dieser boolesche Wert gibt an, ob der Multiplexer die Bitrate automatisch anpassen muss, um sicherzustellen, dass die Daten keinen Überlauf des Lecks verursachen.                                                                                                                                                  |
| [**mfpkey \_ asfmediasink \_ drmaction**](mfpkey-asfmediasink-drmaction-property.md)                    | Gibt die DRM-Medien-Sink-DRM-Aktion für die Datei Generierung an. In dieser Version wird nur DRM-transcodieren unterstützt.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Medien senken](asf-media-sinks.md)
</dt> <dt>

[Komponenten der Pipeline Schicht-ASF](pipeline-layer-asf-components.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
