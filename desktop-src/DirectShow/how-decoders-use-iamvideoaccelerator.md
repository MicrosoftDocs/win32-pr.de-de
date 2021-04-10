---
description: Verwenden von IAMVideoAccelerator durch Decoder
ms.assetid: 0bc6b65b-4502-4c6f-a0f2-82a2bd444d1d
title: Verwenden von IAMVideoAccelerator durch Decoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436768b3561a999f6708ef4f6438b816e0ad303b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957715"
---
# <a name="how-decoders-use-iamvideoaccelerator"></a>Verwenden von IAMVideoAccelerator durch Decoder

Die [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) -Schnittstelle ermöglicht generische Video Beschleunigungs Vorgänge, einschließlich DirectX-Videobeschleunigung (VA). Bei einer nicht-DirectX-VA-Beschleunigung müssen der Decoder und der Videotreiber beide einem gemeinsamen Protokoll entsprechen.

In diesem Abschnitt wird die allgemeine Reihenfolge der Vorgänge beschrieben, die jeder Decoder bei der Verwendung dieser Schnittstelle befolgen sollte. Weitere Informationen zu DirectX-VA-basierten Decodern finden Sie unter [Mapping DirectX Video Acceleration to iamvideoaccelerator](mapping-directx-video-acceleration-to-iamvideoaccelerator.md).

> [!Note]  
> Diese Schnittstelle ist in Windows 2000 und höher verfügbar.

 

Die [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) -Schnittstelle wird in der Eingabe-PIN des [Überlagerungs](overlay-mixer-filter.md) -oder Video Mischungs-Renderers (VMR) verfügbar gemacht. Die [**iamvideoacceleratornotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) -Schnittstelle wird in der Ausgabe-PIN des Decoders verfügbar gemacht. Die Reihenfolge der Ereignisse zum Verbinden der Filter Pins lautet wie folgt:

1.  Der Filter Graph-Manager ruft [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) auf dem Ausgabepin des Decoder-Filters auf. Ein [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) ist ein optionaler Parameter.
    -   [**Am \_ Der \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) ist eine Datenstruktur, die einen Medientyp beschreibt. Sie enthält eine majortype-GUID (in unserem Fall "MediaType \_ Video"), eine Untertyp-GUID (in unserem Fall eine Video Zugriffs-GUID) und eine Vielzahl anderer Dinge. Eines dieser Dinge ist eine GUID im Formattyp, die Informationen zu den Medien enthält, einschließlich der Breite und Höhe eines unkomprimierten Video Bilds, höchstwahrscheinlich in einer [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)-, [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)-, [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo)-oder [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur.
    -   Die [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, falls vorhanden, weist den Decoder an, mithilfe des angegebenen Medientyps zu arbeiten, der "vollständig angegeben" oder "teilweise angegeben" sein kann. Wenn "vollständig angegeben", versucht der Decoder normalerweise einfach, mit diesem Medientyp zu arbeiten. Wenn "teilweise angegeben", wird versucht, einen "vollständig angegebenen" kompatiblen Betriebsmodus zu finden, der für die Verbindungs Herstellung mit dem "teilweise angegebenen" Medientyp verwendet werden kann.
    -   Die übliche Vorgehensweise für den Versuch, einen "vollständig angegebenen" Medientyp für eine Verbindung zu finden, besteht darin, einfach eine Liste mit jedem vollständig angegebenen Medientyp auszuführen, der von der Ausgabepin unterstützt wird. dieser ist mit dem Medientyp "teilweise angegeben" kompatibel und versucht, eine Verbindung mit diesen herzustellen, bis der Vorgang erfolgreich war. Der Prozess wäre normalerweise ähnlich, wenn kein \_ \_ Medientyp im [**IPin:: Connect-Befehl**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) enthalten ist, aber mit der Ausgabepin, die alle Medientypen überprüfen muss.
2.  Wenn der Decoder überprüfen möchte, ob ein bestimmter [**am- \_ Medientyp \_**](/windows/win32/api/strmif/ns-strmif-am_media_type) (einschließlich einer Video Zugriffs-GUID) von der nachgeschalteten Eingabe-PIN unterstützt wird, kann er die [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) -Eigenschaft der PIN (mit der Video-Zugriffstasten-GUID als Untertyp des **\_ \_ Medientyps des am-Mediums**) abrufen
3.  Wenn der Decoder nicht weiß, welche Video-Accelerator-GUIDs die downstreameingabepin unterstützt, und nicht nur eine bestimmte Candidate-Video Zugriffs-GUID durch Aufrufen des [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept)der nachgeschalteten Eingabe-PIN aufrufen möchte, kann der Decoder [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids)
4.  Für einige spezielle Video-Accelerator-GUIDs kann der Decoder den [**iamvideoaccelerator:: getuncompformatssupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) der nachgeschalteten Eingabe-PIN aufrufen, um eine Liste der **ddpixelformat** -Pixel Formate abzurufen, die zum Rendern einer bestimmten Video Zugriffs-GUID verwendet werden kann. Die zurückgegebene Liste sollte als in absteigender Reihenfolge betrachtet werden (d. h., das am meisten bevorzugte Format ist zuerst aufgeführt).
5.  Der Decoder Ruft die [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)der nachgeschalteten Eingabe-PIN auf und übergibt ihm einen [**am- \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) mit der richtigen Video Zugriffs-GUID als Untertyp des Medientyps. Dadurch wird die Verbindung für den Betrieb eingerichtet, einschließlich der Erstellung der nicht komprimierten Ausgabe Oberflächen (die mithilfe der Breite und der Höhe von **am \_ \_ Medientyp** gefunden werden, und der Anzahl der zu zugebenden Oberflächen, die von einem unten beschriebenen Befehl gefunden werden, sowie von weiteren Informationen, die die Video Zugriffstaste bietet und für diesen Zweck verwendet werden soll – beispielsweise die Video Zugriffs-GUID Wenn die downstreameingabepin die Video Zugriffs-GUID oder einen anderen Aspekt der Verbindung ablehnt, kann dies dazu führen, dass die **IPin:: receiveconnection** fehlschlägt. Wenn **IPin:: receiveconnection** fehlschlägt, wird dies in einem zurückgegebenen **HRESULT** angezeigt, und der Decoder kann versuchen, den Rückruf erneut auszuführen, z. b. mit einer neuen Video Zugriffs-GUID in der **am- \_ \_ Medientyp** Struktur.
    -   [!Note]  
        > Dies ist eine weitere Möglichkeit (und die definitive Methode), mit der der Decoder feststellen kann, was von der nachgeschalteten Eingabe-PIN unterstützt wird – indem Sie einfach [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) aufrufen und versuchen, eine Verbindung herzustellen, und dann prüfen, ob der Verbindungsversuch erfolgreich war.

         

    -   Während der [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)ruft der Renderer den [**iamvideoacceleratornotify:: getuncompsurfakesinfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo)-Member des Decoders auf und übergibt ihm die Video-Accelerator-GUID und eine [**amvauncompbufferinfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompbufferinfo) -Struktur, um herauszufinden, wie viele nicht komprimierte Oberflächen zuzuordnen sind. Der Decoder füllt die-Struktur auf und gibt Sie zurück, die die minimale und maximale Anzahl von Oberflächen enthält, die dem jeweiligen Typ zugeordnet werden sollen, sowie eine **ddpixelformat** -Struktur, die das Pixel Format der zu zugebenden Oberflächen beschreibt.
    -   [!Note]  
        > Beim Aufrufen von [**iamvideoacceleratornotify:: getuncompsurfakesinfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo) über die Video Zugriffs-GUID wird tatsächlich nichts an den Decoder übergeben.

         

6.  Der Renderer Ruft die [**iamvideoacceleratornotify:: setesinfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo)des Decoders auf und übergibt die tatsächliche Anzahl der zugeordneten unkomprimierten Oberflächen an den Decoder.
7.  Der Renderer ruft [**iamvideoacceleratornotify:: getcreatevideoacceleratordata**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) des Decoders auf, um alle Daten zu erhalten, die zum Initialisieren der Video Zugriffstaste benötigt werden.
8.  Der Decoder ruft [**iamvideoaccelerator:: getcompbufferinfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo)auf und übergibt ihm eine Video Zugriffs-GUID, eine [**amvauncompdatainfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) -Struktur und die Anzahl der komprimierten Puffer Typen, um eine Menge von [**amvacompbufferinfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) -Datenstrukturen zurückzugeben, die den einzelnen komprimierten Daten Puffern entspricht, die von der Video Zugriffs-GUID verwendet werden
    -   Die [**amvauncompdatainfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvauncompdatainfo) -Struktur enthält die Breite und Höhe der decodierten unkomprimierten Daten (in Pixel) und das ddpixel-Format des nicht komprimierten Bilds.
    -   Die zurückgegebenen [**amvacompbufferinfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) -Datenstrukturen enthalten jeweils Folgendes:
        -   Die Anzahl der komprimierten Puffer, die für den jeweiligen Typ erforderlich sind.
        -   Die Breite und Höhe der zu erstellenden Oberfläche (Felder, die eine tatsächliche Bedeutung haben können oder nicht).
            > [!Note]  
            > Der DirectDraw-Oberflächen Zuordnungs Vorgang für die komprimierten Puffer gibt derzeit nicht an, dass die Breite oder Höhe dieser Oberflächen größer oder gleich 2 ^ 15 ist, obwohl der Oberflächen Belegungs aufrufungs Vorgang möglicherweise nicht zu einem Fehler führt, wenn dieser Grenzwert verletzt wird. Aus diesem Grund kann der Treiber seine Anforderungen für komprimierten Puffer Arbeitsspeicher so strukturieren, dass solch extrem große Größen vermieden werden. Anstatt z. b. einen Puffer mit width = "1" und Height = "65536" anzufordern, sollte der Treiber einen Puffer der Breite = "1024" und Height = "64" anfordern.

             

        -   Die Gesamtanzahl der Bytes, die von der-Oberfläche verwendet werden sollen.
        -   Eine Struktur vom Typ **DDSCAPS2** definiert ein directdrawsurface-Objekt, das die Funktionen zum Erstellen von Oberflächen zum Speichern komprimierter Daten beschreibt.
        -   Ein ddpixelformat, das das Pixel Format beschreibt, das zum Erstellen von Oberflächen zum Speichern komprimierter Daten verwendet wird (ein Feld, das möglicherweise eine wirkliche Bedeutung hat).

> [!Note]  
> Die Aufrufe des Renderers an einige der [**iamvideoacceleratornotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) -Schnittstellen Methoden des Decoders treten möglicherweise (und normalerweise) im Aufruf des Decoders von [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection)auf. Dies gilt insbesondere für Folgendes:
>
> -   [**Iamvideoacceleratornotify:: getuncompsurfakesinfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getuncompsurfacesinfo),
> -   [**Iamvideoacceleratornotify:: stuncompsurfakesinfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-setuncompsurfacesinfo), und
> -   [**Iamvideoacceleratornotify:: getcreatevideoacceleratordata**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata).

 

> [!Note]  
> Um dynamische Formatänderungen zu unterstützen, kann der Decoder auch [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) und andere Methoden pro oben aufruft, während die Filter verbunden sind und ausgeführt werden. Diese Funktion wird bereitgestellt, um dynamische Formatänderungen zu unterstützen (obwohl Sie nicht in H. 263, Anhang P, Sense) enthalten sind, da alle Datasets von Grund auf neu gestartet werden und alle Verweis Bild Informationen verloren gehen.

 

Im folgenden finden Sie eine Beschreibung der Verwendung von [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) während des Vorgangs nach der Initialisierung:

1.  Für jede nicht komprimierte Oberfläche ruft der Decoder [**iamvideoaccelerator:: beginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) auf, um mit der Verarbeitung zu beginnen, um die Ausgabe Abbildung zu erstellen. Wenn dies der Fall ist, sendet der Decoder eine [**amvabeginframeinfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) -Struktur.
    -   Die [**amvabeginframeinfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabeginframeinfo) -Struktur enthält einen Index für einen Ziel Puffer, einen Zeiger auf einige Daten, die nachgeschaltete Daten gesendet werden sollen, und einen Zeiger auf einen Speicherort, an dem die Zugriffstaste einige Daten einfügen kann, die der Decoder lesen kann.
    -   Hinweis 1: die Zugriffstaste empfängt den Ziel Puffer Index nicht, da Sie vom Renderer übersetzt wird, bevor Sie nach unten verschoben wird.
    -   Hinweis 2: [**iamvideoaccelerator:: beginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) kann zwischen Aufrufen von [**iamvideoaccelerator:: Endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe)mehrmals aufgerufen werden.
    -   Hinweis 3: Es gibt keine Annahme innerhalb des Schnittstellen Vorgangs, dass [**iamvideoaccelerator:: beginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) und [**iamvideoaccelerator:: Endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) für die Verarbeitung jedes einzelnen Bilds im Bitstream aufgerufen werden müssen.

        Was [**iamvideoaccelerator:: beginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) tut, wenn die Schnittstelle betroffen ist, erstellt eine Zuordnung innerhalb des Renderers zwischen einem Index und einer nicht komprimierten Oberfläche. Außerdem bietet es die Möglichkeit, eine bestimmte Funktion in einem Gerätetreiber aufzurufen (mit Unterstützung einer Möglichkeit, beliebige Daten zwischen dem Decoder und dem Gerätetreiber zu übergeben).

        (Im DirectX-VA-Vorgang muss jedoch eine Anforderung unten beschrieben werden, die [**iamvideoaccelerator:: beginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) und [**iamvideoaccelerator:: Endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) erfordert, dass die Verarbeitung jedes einzelnen Bilds im Bitstream erfolgt.)

2.  Zum Senden unkomprimierter Daten an die Zugriffstaste ruft der Decoder Folgendes auf:
    -   [**Iamvideoaccelerator:: queryrenderstatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) , um zu bestimmen, ob ein Puffer für das Lesen oder schreiben in sicher ist.
    -   [**Iamvideoaccelerator:: GetBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) zum Sperren und Abrufen des Zugriffs auf einen angegebenen Puffer (sofern dieser zuvor nicht aufgerufen wurde, um diesen Zugriff zu erhalten). **GetBuffer** kann auch verwendet werden, um eine Kopie des Inhalts des letzten nicht komprimierten Ausgabe Bilds zu erhalten, für das [**iamvideoaccelerator:: beginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) aufgerufen wurde. die Bereitstellung von [**iamvideoaccelerator:: Endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) wurde für diesen Ziel Puffer Index nicht aufgerufen. Wenn der DDI einen Renderstatus von dderr \_ wasdeaddrawing für den angeforderten Puffer zurückgibt, wird eine Ruhe Schleife innerhalb von **GetBuffer** ausgeführt, bis diese Bedingung gelöscht wird. Um **GetBuffer** aufzurufen, benötigt der Decoder einige Informationen aus einer [**amvacompbufferinfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvacompbufferinfo) -Datenstruktur, die durch Aufrufen von [**iamvideoaccelerator:: getcompbufferinfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo)abgerufen wird.
    -   [**Iamvideoaccelerator:: Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) , um anzugeben, dass die Daten in einem Satz komprimierter Puffer, wie in einem Array von [**amvabufferinfo**](/previous-versions/windows/desktop/api/amva/ns-amva-amvabufferinfo) -Datenstrukturen angegeben, verarbeitet werden sollen. Eine Funktionscode-dwfunction wird in diesem-Befehl an den Treiber übermittelt. Ein lpprivateinputdata-Zeiger wird auch an einige Daten übergeben, um die downstreamdaten zu senden, und ein lpprivateoutputdata-Zeiger wird an eine Stelle übergeben, an der der Downstream-Prozess einige Daten für den Decoder ablegen kann.
    -   [**Iamvideoaccelerator:: ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) gibt an, dass der Decoder für den Moment die Verwendung eines angegebenen Puffers abgeschlossen hat und keinen gesperrten Zugriff auf den Puffer mehr benötigt. (Wenn der Decoder den Puffer weiterhin verwenden möchte, kann er für den Moment einfach nicht **iamvideoaccelerator:: ReleaseBuffer** aufrufen. dadurch ist es nicht erforderlich, [**iamvideoaccelerator:: GetBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getbuffer) aufzurufen, bis der Puffer nicht mehr verwendet wird.) Der Decoder sollte nicht in den Puffer schreiben, nachdem [**Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) aufgerufen wurde, bis [**queryrenderstatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) angibt, dass der Puffer sicher zum Schreiben ist.
3.  Der Decoder ruft [**iamvideoaccelerator:: Endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe)auf, um die Ausgabe Verarbeitung für einen Ziel Puffer abzuschließen. Mit diesem-Befehl können einige beliebige Daten downstreamdaten übergeben werden, und das ist im Grunde das Ergebnis dieses Aufrufes. In diesem Fall wird kein Ziel Puffer Index gesendet, sodass die Zugriffstaste nicht genau angeben kann, welcher Ziel Puffer abgeschlossen wird, es sei denn, diese Angabe ist in den beliebigen Daten enthalten, die übermittelt werden.
4.  Um einen Frame anzuzeigen, ruft der Decoder [**iamvideoaccelerator auf::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) mit dem Index des Frames, der angezeigt werden soll, und eine [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Struktur, die Start-und Endzeit-Zeitstempel und relevante Flags wie **dwtypespecificflags** in der [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) -Struktur und **dwinterlaceflags** in der [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur enthält. Der Decoder muss überprüfen, ob alle dekomprimierungsaktionen, die den Inhalt des Frames beeinflussen, vor dem Aufruf von **Display Frame** abgeschlossen wurden.
5.  Schließlich sollte der Decoder bei Abschluss der gesamten Verarbeitung angeben, dass alle verbleibenden, gestarteten Ausgabe Frames durch Aufrufen von [**iamvideoaccelerator:: Endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) abgeschlossen und alle gesperrten Puffer freigegeben werden, indem [**iamvideoaccelerator:: ReleaseBuffer**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-releasebuffer) für jeden nicht freigegebenen Puffer aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Decoder-Schnittstellen und Spezifikationen](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



