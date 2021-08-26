---
title: Ausgabeeinstellungen
description: Ausgabeeinstellungen
ms.assetid: effe6c07-e6df-45b0-b865-2a025c466d6f
keywords:
- Windows Medienformat-SDK, globale Konstanten
- Advanced Systems Format (ASF), globale Konstanten
- ASF (Advanced Systems Format), globale Konstanten
- globale Konstanten,Liste von
- Windows Medienformat-SDK, Konstanten
- Advanced Systems Format (ASF),constants
- ASF (Advanced Systems Format),constants
- constants,list of
- Windows Medienformat-SDK, Ausgabeeinstellungen
- Advanced Systems Format (ASF), Ausgabeeinstellungen
- ASF (Advanced Systems Format), Ausgabeeinstellungen
- Ausgabeeinstellungen
- Synchrone Reader,Ausgabeeinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966cd350d379170f9f19c44967ef932bf41a15cb1910b865432ce499b006161e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929940"
---
# <a name="output-settings"></a>Ausgabeeinstellungen

Die folgenden globalen Konstanten werden verwendet, um Ausgabeeinstellungen für das Reader- und synchrone Readerobjekt zu identifizieren.



| Globale Konstante                | WMT \_ \_ ATTR-DATENTYP  | Beschreibung von *pValue*                                                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszAllowInterlacedOutput    | **\_WMT-TYP \_ BOOL**  | True gibt an, dass der Reader Frames mit Interlacing liefert, sofern dies von der Ausgabe unterstützt wird.                                                                                                                                                                                                                                            |
| g \_ wszDedicatedDeliveryThread  | **\_WMT-TYP \_ BOOL**  | True gibt an, dass für diese Ausgabe ein dedizierter Thread für die Übermittlung der Beispiele erstellt wird. Wird auf dem synchronen Reader nicht unterstützt.                                                                                                                                                                                            |
| g \_ wszDeliverOnReceive         | **\_WMT-TYP \_ BOOL**  | True gibt an, dass Beispiele für diese Ausgabe übermittelt werden, sobald sie über den Reader verfügbar sind. Dies kann dazu führen, dass Stichproben aus dieser Ausgabe in der reihenfolgen- und vor den entsprechenden Stichproben aus anderen Ausgaben übermittelt werden.                                                                                            |
| g \_ wszDynamicRangeControl      | **WMT \_ TYPE \_ DWORD** | Gibt die Ebene des dynamischen Bereichssteuer steuerelements an, das für die Ausgabe verwendet werden soll. Legen Sie auf einen Wert von 0 bis 2 fest, wobei 0 kein dynamisches Bereichssteuersystem angibt (Standardeinstellung), und 2 ist die maximale Ebene des dynamischen Bereichssteuerwerts (der kleinste dynamische Bereich).                                                                                |
| g \_ wszEarlyDataDelivery        | **WMT \_ TYPE \_ DWORD** | Zeit in Millisekunden, die angibt, wie viel früher die Beispiele zu liefern sind. Wenn der Wert größer als 0 (null) ist, werden die Stichproben aus dieser Ausgabe abgerufen und decodiert, sodass die Beispiele vor den Beispielen für andere Ausgaben übermittelt werden. Normalerweise liefert der Reader Stichproben in der Reihenfolge der Präsentationszeit.         |
| g \_ wszEnableDiscreteOutput     | **\_WMT-TYP \_ BOOL**  | True gibt an, dass der Reader eine Audioausgabe mit mehreren Kanälen mit hoher Definition aktiviert. Diese Einstellung ist nur für Audiostreams gültig, die mit dem Windows Media Audio 9-Professional codiert sind. Wenn diese Einstellung auf TRUE festgelegt ist, müssen Sie auch die Sprecherkonfiguration des Clientcomputers angeben, indem Sie g \_ wszSpeakerConfig festlegen. |
| g \_ wszEnableFrameInterpolation | **\_WMT-TYP \_ BOOL**  | True gibt an, dass der Codec den Videostream mit einer höheren Bildfrequenz liefert [*und*](wmformat-glossary.md)die Frames algorithmisch interpoliert.                                                                                                                                                          |
| g \_ wszJustInTimeDecode         | **\_WMT-TYP \_ BOOL**  | True gibt an, dass die Daten so spät wie möglich decodiert werden müssen. Wird im synchronen Reader nicht unterstützt.                                                                                                                                                                                                                            |
| g \_ wszNeedsPreviousSample      | **\_WMT-TYP \_ BOOL**  | True gibt an, dass das vorherige Beispiel dekomprimiert werden muss. Diese Einstellung gilt nur für Deltaframes in komprimierten Videos und ist schreibgeschützt.                                                                                                                                                                       |
| g \_ wszScrambledAudio           | **\_WMT-TYP \_ BOOL**  | True gibt an, dass für diese Ausgabe das Scrambled Audio Error-Verdeckenschema verwendet wird. Dies ist eine gültige Einstellung nur für Audioausgabe.                                                                                                                                                                                                |
| g \_ wszSingleOutputBuffer       | **\_WMT-TYP \_ BOOL**  | True gibt an, dass ein einzelner Ausgabepuffer verwendet werden muss (z. B. ein DirectDraw® Videopuffer). Wird im synchronen Reader nicht unterstützt.                                                                                                                                                                                           |
| g \_ wszSoftwareScaling          | **\_WMT-TYP \_ BOOL**  | False gibt an, dass das Video nicht skaliert wird. (Es darf keine Änderung an der Auflösung geben.)                                                                                                                                                                                                                                                |
| g \_ wszSpeakerConfig            | **WMT \_ TYPE \_ DWORD** | Wenn die Multichannel-Audiodecodierung durch Festlegen von g wszEnableDiscreteOutput aktiviert wird, gibt diese Einstellung die Sprecherkonfiguration des \_ Clientcomputers an. Legen Sie auf eine der DirectSound-Sprecherkonfigurationskonst constants fest.                                                                                                   |
| g \_ wszStreamLanguage           | **WMT-TYP \_ \_ WORD**  | Der Index in der Sprachliste der Sprache, die für diese Ausgabe übermittelt werden soll. Wird für Ausgaben verwendet, die Streams darstellen, die sich durch die Sprache gegenseitig ausschließen.                                                                                                                                                                      |
| g \_ wszVideoSampleDurations     | **\_WMT-TYP \_ BOOL**  | True gibt an, dass der Reader genaue Stichprobendauern liefert.                                                                                                                                                                                                                                                                |
| g \_ wszEnableWMAProSPDIFOutput  | **\_WMT-TYP \_ BOOL**  | True gibt an, dass der Reader das Format für die digitale Schnittstelle (S/PDIF) des Formats"/" in die aufzählten Ausgabetypen einträgt.                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMReaderAdvanced2::GetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getoutputsetting)
</dt> <dt>

[**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**IWMSyncReader::GetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputsetting)
</dt> <dt>

[**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting)
</dt> </dl>

 

 




