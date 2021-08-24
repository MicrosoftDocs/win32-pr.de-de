---
description: Zwei-Pass-Codierungsmodi werden von bestimmten Windows Media-Encodern und Media Foundation auf Pipelineebene unterstützt.
ms.assetid: 3fd5baff-142f-453e-bb97-b355ee6678fc
title: Erstellen einer Topologie für Two-Pass Windows Mediencodierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525a98faa424371f2d80739e5c68f199cfc7ed6443c25ab3d15b575afdd003e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724880"
---
# <a name="how-to-create-a-topology-for-two-pass-windows-media-encoding"></a>Erstellen einer Topologie für Two-Pass Windows Mediencodierung

Zwei-Pass-Codierungsmodi werden von bestimmten Windows Media-Encodern und Media Foundation auf Pipelineebene unterstützt. Die Anwendung muss die Codierungstopologie ähnlich wie bei der Single-Pass-Codierung konfigurieren und einrichten, aber im 2-Pass-Codierungsmodus muss die Anwendung die Codierungssitzung zweimal ausführen. Beim ersten Durchlauf sammelt der Encoder Informationen zum Inhalt des Streams. Im zweiten Durchlauf wird mithilfe der informationen, die im ersten Durchlauf gesammelt wurden, die endgültige Ausgabedatei generiert. Durch die zweimalige Verarbeitung der Beispiele für den Stream optimiert die Zwei-Durchlauf-Codierung den Codierungsprozess und erzeugt codierte Dateien höherer Qualität. Zwei-Pass-Codierungsmodi können nicht für Livestreams verwendet werden.

Media Foundation unterstützt die folgenden Zwei-Pass-Codierungsmodi:

-   [Codierung der uneingeschränkten Variablenbitrate](unconstrained-variable-bit-rate--vbr--encoding.md)
-   [Codierung der spitzenbeschränkten Variablenbitrate](peak-constrained-variable-bit-rate--vbr--encoding.md)

Das Erstellen einer Codierungstopologie für die Zwei-Durchlauf-Codierung ähnelt den Einzeldurchlaufmodi. Die folgende Liste zeigt die wichtigsten Unterschiede.

-   Die Encoderkonfiguration muss die [**MFPKEY \_ PASSESUSED-Eigenschaft**](mfpkey-passesusedproperty.md) enthalten, die auf 2 festgelegt ist, und die [**MFPKEY \_ VBRENABLED-Eigenschaft**](mfpkey-vbrenabledproperty.md) auf VARIANT \_ TRUE. Dadurch werden die Funktionen des Encoders in Zwei-Pass-Modi gefiltert. Wenn Sie Aktivierungsobjekte verwenden, übergeben Sie diese Eigenschaften an [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) oder [**MFCreateWMVEncoderActivate.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)
-   Verwenden Sie für den ersten Durchlauf eine Dummymediensenke im Ausgabeknoten, da die in diesem Durchlauf generierten Beispiele nicht der endgültigen Datei hinzugefügt werden.
-   Fragen Sie für den zweiten Durchlauf den Encoder nach den erforderlichen Eigenschaften nach der Codierung ab, und ersetzen Sie den Knoten dummy media sink durch die ASF-Mediensenke, und legen Sie diese Eigenschaften fest.

Weitere Informationen zum Einrichten einer Codierungstopologie finden Sie unter [Tutorial: Single Pass Windows Media Encoding](tutorial--1-pass-windows-media-encoding.md).

Das folgende Verfahren fasst die Schritte zum Codieren Windows Medieninhalts in einem ASF-Container mithilfe eines Zwei-Pass-Codierungsmodus zusammen.

1.  Erstellen Sie mit dem Quell resolver eine Medienquelle für den angegebenen .
2.  Aufzählen der Streams in der Medienquelle.
3.  Erstellen Sie die ASF-Mediensenke, und fügen Sie abhängig von den Streams in der Medienquelle, die codiert werden müssen, Streamsenken hinzu.
4.  Erstellen Sie die Mediensenke.
5.  Erstellen Sie die Windows Medienencoder für die Streams in der Ausgabedatei.
6.  Konfigurieren Sie die Encoder mit den 2-Pass-Codierungseigenschaften.
7.  Erstellen Sie eine partielle Codierungstopologie, indem Sie die Quelle, die Encoder und die Mediensenke verbinden.
8.  Instanziieren Sie die Mediensitzung, und legen Sie die Topologie für die Mediensitzung fest.
9.  Führen Sie den ersten Codierungsdurchlauf aus, indem Sie die Mediensitzung steuern und alle relevanten Ereignisse aus der Mediensitzung abrufen.
10. Schließen Sie die Codierungssitzung, und fahren Sie sie herunter.
11. Fragen Sie den Encoder je nach Codierungstyp nach den folgenden Eigenschaften ab: 

    | Codierungstyp                                                                                        | Eigenschaftenname                                                                                                                                                                                                                                                                                                                                                     |
    |------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [Codierung der uneingeschränkten Variablenbitrate](unconstrained-variable-bit-rate--vbr--encoding.md)       | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**\_MFPKEY-MAUSG**](mfpkey-ravgproperty.md)<br/>                                                                                                               |
    | [Codierung der spitzenbeschränkten Variablenbitrate](peak-constrained-variable-bit-rate--vbr--encoding.md) | [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md)<br/> [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)<br/> [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)<br/> [**\_MFPKEY-MAUSG**](mfpkey-ravgproperty.md)<br/> [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md)<br/> [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)<br/> |

    

     

12. Erstellen Sie die ASF-Dateisenke, und fügen Sie abhängig von den Streams, die Sie in die endgültige Ausgabedatei einschließen möchten, die erforderlichen Streamsenken hinzu.
13. Legen Sie die encoder-Eigenschaften fest, die in Schritt 11 für die Dateisenke abgerufen wurden.
14. Ersetzen Sie die Mediensenke im Ausgabeknoten durch die neu erstellte Dateisenke.
15. Instanziieren Sie die Mediensitzung, und legen Sie die aktualisierte Topologie für die Mediensitzung fest.
16. Führen Sie den zweiten Codierungsdurchlauf aus, indem Sie die Mediensitzung steuern und alle relevanten Ereignisse aus der Mediensitzung abrufen.
17. Warten Sie auf das [MEEndOfPresentation-Ereignis](meendofpresentation.md) aus der Mediensitzung, und erhalten Sie im Ereignishandler die Codierungseigenschaftswerte vom Encoder, und legen Sie sie in der Dateisenke fest. Weitere Informationen finden Sie unter "Aktualisieren von Codierungseigenschaften in der Dateisenke" in [Tutorial: Single Pass Windows Media Encoding](tutorial--1-pass-windows-media-encoding.md).
18. Schließen Sie die Codierungssitzung, und fahren Sie sie herunter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Komponenten auf Pipelineebene](pipeline-layer-asf-components.md)
</dt> </dl>

 

 




