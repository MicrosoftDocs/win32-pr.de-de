---
description: Zwei-Pass-Codierungs Modi werden von bestimmten Windows Media Encoder und Media Foundation auf der Pipeline Ebene unterstützt.
ms.assetid: 3fd5baff-142f-453e-bb97-b355ee6678fc
title: Erstellen einer Topologie für Two-Pass Windows-Medien Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c813b9a3c31fafaa3efbea83180c997bc46079d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961135"
---
# <a name="how-to-create-a-topology-for-two-pass-windows-media-encoding"></a>Erstellen einer Topologie für Two-Pass Windows-Medien Codierung

Zwei-Pass-Codierungs Modi werden von bestimmten Windows Media Encoder und Media Foundation auf der Pipeline Ebene unterstützt. Die Anwendung muss die Codierungs Topologie konfigurieren und einrichten, ähnlich wie bei der Codierung mit nur einem Durchlauf, aber im 2-Pass-Codierungs Modus muss die Anwendung die Codierungs Sitzung zweimal ausführen. Beim ersten Durchlauf sammelt der Encoder Informationen zum Inhalt des Streams. Beim zweiten Durchlauf wird die endgültige Ausgabedatei generiert, indem die beim ersten Durchlauf gesammelten Informationen verwendet werden. Durch die zweimalige Verarbeitung der Stichproben für den Stream wird der Codierungsprozess durch die zwei-Pass-Codierung optimiert und qualitativ hochwertige codierte Dateien erstellt. Die zwei-Pass-Codierungs Modi können nicht für Livestreams verwendet werden.

Media Foundation unterstützt die folgenden zwei-Durchlauf-Codierungs Modi:

-   [Unbeschränkte Variablen Bitrate-Codierung](unconstrained-variable-bit-rate--vbr--encoding.md)
-   [Mit Spitzenwerten beschränkte Variable Bitrate-Codierung](peak-constrained-variable-bit-rate--vbr--encoding.md)

Das Entwickeln einer Codierungs Topologie für die zwei-Pass-Codierung ähnelt den einzelnen Pass Modi. In der folgenden Liste sind die wichtigsten Unterschiede aufgeführt.

-   Die Encoderkonfiguration muss die Eigenschaft " [**mfpkey \_ passesused**](mfpkey-passesusedproperty.md) " enthalten, die auf 2 festgelegt ist, und die Eigenschaft " [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) " auf Variant \_ true. Dadurch werden die Funktionen des Encoders auf zweistufige Modi gefiltert. Wenn Sie Aktivierungs Objekte verwenden, übergeben Sie diese Eigenschaften an [**mfkreatewmaencoderactivation**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) oder [**mfkreatewmvencoderactivation**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).
-   Verwenden Sie für den ersten Durchlauf eine Pseudo Medien-Senke im Ausgabe Knoten, da die in diesem Durchlauf generierten Beispiele nicht der endgültigen Datei hinzugefügt werden.
-   Fragen Sie für den zweiten Durchlauf den Encoder nach den erforderlichen nach Codierungs Eigenschaften ab, und ersetzen Sie den Knoten für den Dummy-Medien Sink durch die ASF-Medien Senke, wobei diese Eigenschaften festgelegt sind.

Weitere Informationen zum Einrichten einer Codierungs Topologie finden Sie unter [Tutorial: Single Pass Windows Media Encoding](tutorial--1-pass-windows-media-encoding.md).

Im folgenden Verfahren werden die Schritte zum Codieren von Windows Media-Inhalten in einem ASF-Container mithilfe eines zwei-Pass-Codierungs Modus zusammengefasst.

1.  Erstellen Sie eine Medienquelle für die angegebene mithilfe des Quell Resolvers.
2.  Listet die Streams in der Medienquelle auf.
3.  Erstellen Sie die ASF-Medien Senke, und fügen Sie in Abhängigkeit von den Streams in der Medienquelle, die codiert werden müssen, streamsenken hinzu.
4.  Erstellen Sie die Medien Senke.
5.  Erstellen Sie die Windows Media Encoder für die Streams in der Ausgabedatei.
6.  Konfigurieren Sie die Encoder mit den 2-Pass-Codierungs Eigenschaften.
7.  Erstellen Sie eine partielle Codierungs Topologie, indem Sie die Quelle, die Encoder und die Medien Senke verbinden.
8.  Instanziieren Sie die Medien Sitzung, und legen Sie die Topologie für die Medien Sitzung fest.
9.  Führen Sie den ersten Codierungs Durchlauf aus, indem Sie die Medien Sitzung Steuern und alle relevanten Ereignisse aus der Medien Sitzung erhalten.
10. Schließen und beenden Sie die Codierungs Sitzung.
11. Fragen Sie den Encoder abhängig vom Codierungstyp nach den folgenden Eigenschaften ab: 

    | Codierungstyp                                                                                        | Eigenschaftenname                                                                                                                                                                                                                                                                                                                                                     |
    |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [Unbeschränkte Variablen Bitrate-Codierung](unconstrained-variable-bit-rate--vbr--encoding.md)       | [**mfpkey- \_ passesused**](mfpkey-passesusedproperty.md)<br/> [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md)<br/> [**mfpkey \_ bavg**](mfpkey-bavgproperty.md)<br/> [**mfpkey \_ Ravg**](mfpkey-ravgproperty.md)<br/>                                                                                                               |
    | [Mit Spitzenwerten beschränkte Variable Bitrate-Codierung](peak-constrained-variable-bit-rate--vbr--encoding.md) | [**mfpkey- \_ passesused**](mfpkey-passesusedproperty.md)<br/> [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md)<br/> [**mfpkey \_ bavg**](mfpkey-bavgproperty.md)<br/> [**mfpkey \_ Ravg**](mfpkey-ravgproperty.md)<br/> [**mfpkey ( \_ bmax)**](mfpkey-bmaxproperty.md)<br/> [**mfpkey- \_ Rmax**](mfpkey-rmaxproperty.md)<br/> |

    

     

12. Erstellen Sie die ASF-Datei Senke, und fügen Sie abhängig von den Datenströmen, die Sie in die endgültige Ausgabedatei einschließen möchten, die erforderlichen streamsenken hinzu.
13. Legen Sie die in Schritt 11 abgerufenen Codierungs Eigenschaften in der Datei Senke fest.
14. Ersetzen Sie die Medien Senke im Ausgabe Knoten durch die neu erstellte dateisenke.
15. Instanziieren Sie die Medien Sitzung, und legen Sie die aktualisierte Topologie für die Medien Sitzung fest.
16. Führen Sie einen zweiten Codierungs Durchlauf aus, indem Sie die Medien Sitzung Steuern und alle relevanten Ereignisse aus der Medien Sitzung erhalten.
17. Warten Sie auf das [meendof Presentation](meendofpresentation.md) -Ereignis aus der Medien Sitzung, und legen Sie im Ereignishandler die Codierungs Eigenschaftswerte aus dem Encoder ab, und legen Sie Sie auf die Datei Senke fest. Weitere Informationen finden Sie unter "Aktualisieren von Codierungs Eigenschaften in der Datei Senke" in [Tutorial: Single Pass Windows Media Encoding](tutorial--1-pass-windows-media-encoding.md).
18. Schließen und beenden Sie die Codierungs Sitzung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponenten der Pipeline Schicht-ASF](pipeline-layer-asf-components.md)
</dt> </dl>

 

 




