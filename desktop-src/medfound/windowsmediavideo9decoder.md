---
description: Der Windows Media Video 9-Decoder decodiert Videostreams, die vom Windows Media Video Encoder codiert wurden.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Windows Media Video 9-Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371632"
---
# <a name="windows-media-video-9-decoder"></a>Windows Media Video 9-Decoder

Der Windows Media Video 9-Decoder decodiert Videostreams, die vom [**Windows Media Video Encoder**](windowsmediavideo9encoder.md)codiert wurden. Der Encoder und der Decoder unterstützen die folgenden vier Kategorien codierter Videos.

-   Windows Media Video 9 einfaches Profil
-   Windows Media Video 9 Hauptprofil
-   Erweiterte profile Windows Media Video 9
-   Windows Media Video 9,1-Image

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) für den Windows Media Video Decoder wird durch die Konstante **CLSID \_ cwmvdecmediaobject** dargestellt. Sie können eine Instanz des Video-Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="interfaces"></a>Schnittstellen

Ein Video Decoder-Objekt macht die [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und stellt die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle zur Verfügung, sodass das Objekt als Media Foundation Transformation (MFT) verwendet werden kann.

Ein Video Decoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird. In der folgenden Tabelle sind die Bedingungen aufgeführt, unter denen sich ein Video Decoder als DMO oder MFT verhält.



| Betriebssystem            | Decoderverhalten                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Ein Windows Media-Video Decoder verhält sich immer als DMO.                                                                                                                |
| Windows Vista und Windows 7 | Standardmäßig verhält sich ein Windows Media-Video Decoder als DMO. Wenn Sie eine [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle in einem Video Decoder erhalten, verhält sie sich wie eine MFT. |



 

Ab Windows 7 implementiert der Windows Media Video Decoder die [**idmuqualitycontrol**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) -Schnittstelle.

## <a name="input-formats"></a>Eingabeformate

In der folgenden Tabelle werden die vier Zeichen Codes (fourccs) angezeigt, die den Kategorien codierter Eingaben entsprechen, die vom Windows Media Video Decoder unterstützt werden.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Media Video 9 einfaches Profil   | "WMV3"                                   |
| Windows Media Video 9 Hauptprofil     | "WMV3"                                   |
| Erweiterte profile Windows Media Video 9 | "WVC1"                                   |
| Windows Media Video 9,1-Image          | "Wmvp" für 9,1, "WVP2" für 9,1 Version 2 |



 

## <a name="output-formats"></a>Ausgabeformate

Der Windows Media Video-Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als DMO fungiert.

-   Mediasubtype \_ NV12
-   Mediasubtype \_ YV12
-   Mediasubtype \_ im YUY2
-   mediasubtype \_ UYVY
-   mediasubtype \_ yvyu
-   Mediasubtype \_ NV11
-   Mediasubtype \_ RGB32
-   Mediasubtype \_ RGB24
-   Mediasubtype \_ RGB565
-   Mediasubtype \_ RGB555
-   Mediasubtype \_ RGB8

Der Windows Media Video-Decoder unterstützt die folgenden Ausgabemedien-Untertypen, wenn er als MFT fungiert.

-   MF-Format \_ NV12
-   MF-Format \_ YV12
-   MF-Format \_ im YUY2
-   MF-Format ( \_ UYVY)
-   Mfvideoformat \_ yvyu
-   MF-Format \_ NV11
-   MF-Format \_ RGB32
-   MF-Format \_ RGB24
-   MF-Format \_ RGB565
-   MF-Format \_ RGB555
-   MF-Format \_ RGB8

## <a name="properties"></a>Eigenschaften

Der Windows Media Video-Decoder unterstützt die folgenden Eigenschaften.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></td>
<td>Gibt an, ob der Codec interpackt Video Frames aus dem komprimierten Stream als progressive Frames decodiert.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></td>
<td>Gibt an, ob der Decoder die DirectX-Video Beschleunigungs Hardware verwendet, falls verfügbar.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></td>
<td>Gibt die Leistungs Ebene für den Decoder an.<br/> <dl> Windows 7.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></td>
<td>Gibt an, ob der Decoder die Frame Interpolation verwenden soll.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></td>
<td>Gibt an, ob der Decoder Frame Interpolation unterstützt.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Bild<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></td>
<td>Gibt die Anzahl der Threads an, die vom Decoder verwendet werden.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></td>
<td>Gibt den postverarbeitungs Modus für den Decoder an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, erweitertes Profil, Image.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>g_wszWMVCNeedsDrain</strong></td>
<td>Gibt an, ob der Decoder entladen werden soll.<br/> <dl> Windows 8<br />
Schreibgeschützt.<br />
</dl> Diese Eigenschaft wird von der Windows Media-Format Laufzeit verwendet. Der Eigenschaftentyp ist <strong>VARIANT_BOOL</strong>. Wenn der Wert <strong>VARIANT_TRUE</strong>ist, sollte der Decoder nach einer Diskontinuität entladen werden. Weitere Informationen zum Entleeren von MFT finden Sie unter <a href="basic-mft-processing-model.md">Grundlegendes MFT-Verarbeitungsmodell</a>.<br/>
<blockquote>
[!Note]<br />
Um diese Eigenschaft abzufragen, verwenden Sie die <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> -Schnittstelle.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Die vom Windows Media Video 9-Decoder maximal zulässige Auflösung ist 4096x4096.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codec-Implementierung](codecimplementation.md)
</dt> </dl>

 

 
