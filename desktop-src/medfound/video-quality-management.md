---
description: Video Qualitäts Verwaltung
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: Video Qualitäts Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233ccd54cfcb98742abef9a91241e903c07ba549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959225"
---
# <a name="video-quality-management"></a>Video Qualitäts Verwaltung

In diesem Thema werden einige Verbesserungen an der Video Pipeline in Windows 7 beschrieben, sowohl für Microsoft Media Foundation als auch für Microsoft DirectShow.

In einer perfekten Welt würde das Video nie, unabhängig von der Videoauflösung oder der CPU-/GPU-Auslastung, nicht glatt verlaufen. Natürlich muss die Video Pipeline in der Lage sein, mit begrenzten Hardware Ressourcen umzugehen, und die Wiedergabe muss an die Systemumgebung angepasst werden. Die Ziele für die Video Qualitäts Verwaltung sind folgende:

-   Reduzieren Sie das Abgleiten (verworfene oder späte Rahmen).
-   Reduzieren Sie die Speicherauslastung, insbesondere in der GPU.
-   Reduzieren Sie den Stromverbrauch, insbesondere bei Laptops, die auf Akkuleistung ausgeführt werden.
-   Erzielen Sie die bestmögliche Bildqualität, und zwar anhand von Ressourceneinschränkungen.
-   Halten Sie das Video mit Audiodaten synchronisiert.

Einige dieser Ziele sind gegenseitig, insbesondere bei Low-End-Systemen. Im Allgemeinen gibt es einen Kompromiss zwischen Geschwindigkeit und Qualität. Das Abrufen von Problemen ist eher verwerflich als bei moderater Reduzierung der visuellen Qualität. Die relative Wichtigkeit des Stromverbrauchs variiert in Abhängigkeit von der Umgebung. auf einem Laptop, der mit Akkuleistung betrieben wird, ist es sehr wichtig.

In Windows 7 bietet der Enhanced Video Renderer (EVR) eine bessere Unterstützung für die Video Qualitäts Verwaltung. Sowohl die Media Foundation Pipeline als auch die DirectShow-Pipeline wurden aktualisiert, um diese Funktionen nutzen zu können. Eine zweistufige Vorgehensweise wird verwendet:

-   Vor dem Start der Wiedergabe kann die Pipeline basierend auf den Energie Verwaltungs Einstellungen des Benutzers und den Hardwareinformationen statische Optimierungen durchführen.
-   Nach dem Start der Wiedergabe kann die Pipeline basierend auf der Laufzeitleistung dynamische Optimierungen anwenden.

## <a name="quality-management-in-media-foundation"></a>Qualitäts Verwaltung in Media Foundation

Um statische Optimierungen zu aktivieren, legen Sie das-Attribut für [ \_ \_ statische \_ Wiedergabe \_ Optimierungen der MF-Topologie](mf-topology-static-playback-optimizations.md) in der partiellen Topologie fest, bevor Sie die Topologie auflösen. Das topologielader fragt dieses Attribut in der [**imftopoloader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) -Methode ab.

Wenn Sie statische Optimierungen aktivieren, sollten Sie zwei weitere Attribute in der Topologie festlegen:



| Attribut                                                                                                                                      | BESCHREIBUNG                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>maximal zulässige Anzahl von MF- \_ \_ topologiewiedergabe \_ \_<br/>   | Gibt die maximale Größe des Videowiedergabe Fensters an.<br/> |
| <span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>MF- \_ \_ topologiewiedergabe \_ Framerate<br/> | Gibt die Aktualisierungsrate des Monitors an.<br/>                      |



 

Diese beiden Attribute helfen der Pipeline, die effektivste Einstellung für die Qualitäts Verwaltung zu berechnen.

Dynamische Optimierungen werden vom Quality Manager ausgeführt. Sie müssen nichts tun, um den Quality Manager zu aktivieren. Er ist automatisch aktiviert. Der Quality Manager war in Windows Vista vorhanden. in Windows 7 kann der EVR besser auf Nachrichten vom Quality Manager reagieren.

## <a name="quality-management-in-directshow"></a>Qualitäts Verwaltung in DirectShow

DirectShow unterstützt statische und dynamische Optimierungen für die DVD-Wiedergabe. Um diese Optimierungen in einer DVD-Wiedergabe Anwendung zu aktivieren, legen Sie die folgenden Flags im *dwFlags* -Parameter der **idvdgraphbuilder:: renderdvdvideovolume** -Methode fest:



| Flag                  | Beschreibung                    |
|-----------------------|--------------------------------|
| AM- \_ DVD- \_ Anpassungs \_ Diagramm | Aktiviert statische Optimierungen.  |
| AM \_ DVD- \_ EVR- \_ QoS     | Aktiviert dynamische Optimierungen. |



 

Andere DirectShow-Anwendungen können dynamische Optimierungen aktivieren, indem Sie die [**ievrfilterconfigex:: setconfigprefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) -Methode direkt für den EVR-Filter aufrufen. Geben Sie das Flag " **evrfilterconfigprefs \_ enableqos** " an.

> [!Note]  
> Statische Optimierungen in DirectShow sind auf die DVD-Wiedergabe beschränkt.

 

## <a name="quality-management-in-the-evr"></a>Qualitäts Verwaltung im EVR

Der EVR unterstützt einige neue Konfigurationsflags für die Qualitäts Verwaltung. Wenn Sie die zuvor beschriebenen Optimierungen der Qualitäts Verwaltung aktivieren, müssen diese Flags nicht direkt festgelegt werden. Sie sind jedoch für Anwendungen dokumentiert, die eine präzisetere Kontrolle über den EVR wünschen.

Legen Sie die folgenden Flags auf dem EVR-Mixer fest, indem Sie die [**IMFVideoMixerControl2:: setmixingprefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) -Methode aufrufen:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flags</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></li>
<li><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></li>
</ul></td>
<td>Überspringen Sie das zweite Feld jedes Zeilen Sprung Bilds.</td>
</tr>
<tr class="even">
<td><ul>
<li><strong>MFVideoMixPrefs_AllowDropToBob</strong></li>
<li><strong>MFVideoMixPrefs_ForceBob</strong></li>
</ul></td>
<td>Verwenden Sie Bob Deinterlacing, auch wenn der Treiber einen Modus mit höherer Qualität unterstützt.</td>
</tr>
</tbody>
</table>



 

Legen Sie die folgenden Flags auf dem EVR Presenter fest, indem Sie die [**imfvideodisplaycontrol:: setrenderingprefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) -Methode aufrufen:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flags</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></li>
<li><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></li>
</ul></td>
<td>Drosselung der Ausgabe, um die GPU-Bandbreite zu</td>
</tr>
<tr class="even">
<td><ul>
<li><strong>MFVideoRenderPrefs_ForceBatching</strong></li>
<li><strong>MFVideoRenderPrefs_AllowBatching</strong></li>
</ul></td>
<td>Batch Direct3D vorhandene Aufrufe. Durch diese Optimierung kann das System häufiger in den Leerlauf Status eintreten, wodurch der Energieverbrauch reduziert werden kann.</td>
</tr>
<tr class="odd">
<td><ul>
<li>MFVideoRenderPrefs_ForceScaling</li>
<li>MFVideoRenderPrefs_AllowScaling</li>
</ul></td>
<td>Führen Sie eine Video Mischung mit einem Rechteck aus, das kleiner als das Ausgabe Rechteck ist. Skalieren Sie das Ergebnis auf die richtige Ausgabegröße.</td>
</tr>
</tbody>
</table>



 

Außerdem unterstützt die EVR-Medien Senke Konfigurations Attribute, die den einzelnen Flags entsprechen:

-   [Evrconfig \_ allowbatching](evrconfig-allowbatching.md)
-   [Evrconfig \_ allowdropto Bob](evrconfig-allowdroptobob.md)
-   [Evrconfig \_ allowdropabhalfinterlace](evrconfig-allowdroptohalfinterlace.md)
-   [Evrconfig \_ allowscaling](evrconfig-allowscaling.md)
-   ["Evrconfig \_ allowdropto Throttle"](evrconfig-allowdroptothrottle.md)
-   [Evrconfig \_ forcebatching](evrconfig-forcebatching.md)
-   [Evrconfig \_ forcebob](evrconfig-forcebob.md)
-   [Evrconfig \_ forcehalfinterlace](evrconfig-forcehalfinterlace.md)
-   [Evrconfig- \_ forcescaleing](evrconfig-forcescaling.md)
-   [Evrconfig- \_ forcethrottle](evrconfig-forcethrottle.md)

Vor dem Start der Wiedergabe können Sie diese Attribute direkt auf der EVR-Medien Senke festlegen, als Alternative zum Aufrufen der [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) -Methode und der [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Methode. Um diese Attribute festzulegen, Fragen Sie die EVR-Medien Senke nach [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Sitzung](media-session.md)
</dt> </dl>

 

 




