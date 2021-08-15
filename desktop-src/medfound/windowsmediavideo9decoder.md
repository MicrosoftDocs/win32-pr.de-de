---
description: Der Windows Media Video 9-Decoder decodiert Videostreams, die vom Windows Media Video Encoder codiert wurden.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Windows Media Video 9-Decoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b251b46c94ef88283577dbd8268c3275d8ed6aab9321c98e115a42501e2729ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237262"
---
# <a name="windows-media-video-9-decoder"></a>Windows Media Video 9-Decoder

Der Windows Media Video 9-Decoder decodiert Videostreams, die vom Media Video Encoder Windows [**wurden.**](windowsmediavideo9encoder.md) Der Encoder und der Decoder unterstützen die folgenden vier Kategorien von codiertem Video.

-   Windows Media Video 9 Simple Profile
-   Windows Media Video 9-Hauptprofil
-   Windows Media Video 9 Advanced Profile
-   Windows Media Video 9.1 Image

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) für den Windows Media Video-Decoder wird durch die Konstante **CLSID \_ CWMVDecMediaObject dargestellt.** Sie können eine Instanz des Videodecoders erstellen, indem Sie **CoCreateInstance aufrufen.**

## <a name="interfaces"></a>Schnittstellen

Ein Videodecoderobjekt macht die [**IMediaObject-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und macht die [**BERTRANSFORM-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) verfügbar, sodass das Objekt als Media Foundation Transform (MFT) verwendet werden kann.

Ein Videodecoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie abrufen und welche Version Windows wird. Die folgende Tabelle zeigt die Bedingungen, unter denen sich ein Videodecoder als DMO MFT verhält.



| Betriebssystem            | Decoderverhalten                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Ein Windows Medienvideodecoder verhält sich immer wie ein DMO.                                                                                                                |
| Windows Vista und Windows 7 | Standardmäßig verhält sich ein Windows Medienvideodecoder wie ein DMO. Wenn Sie eine [**DURCHSICHTTransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) für einen Videodecoder erhalten, verhält sie sich wie ein MFT. |



 

Ab Windows 7 implementiert der Windows Media Video-Decoder die [**IDMOQualityControl-Schnittstelle.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol)

## <a name="input-formats"></a>Eingabeformate

In der folgenden Tabelle sind die vier Zeichencodes (FOURCCs) aufgeführt, die den Kategorien der codierten Eingabe entsprechen, die vom Windows Media Video-Decoder unterstützt werden.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Media Video 9 Simple Profile   | "WMV3"                                   |
| Windows Media Video 9-Hauptprofil     | "WMV3"                                   |
| Windows Media Video 9 Advanced Profile | "WVC1"                                   |
| Windows Media Video 9.1 Image          | "WMVP" für 9.1, "WVP2" für 9.1 Version 2 |



 

## <a name="output-formats"></a>Ausgabeformate

Der Windows Media Video-Decoder unterstützt die folgenden Ausgabemedienuntertypen, wenn er als DMO.

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UY WIE
-   MEDIASUBTYPE \_ YVINNEN
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Der Windows Media Video-Decoder unterstützt die folgenden Ausgabemedienuntertypen, wenn er als MFT agiert.

-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UY FORMAT
-   MFVideoFormat \_ YV FORMAT
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

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
<td>Gibt an, ob der Codec Interlaced-Videoframes aus dem komprimierten Stream als progressive Frames decodiert.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></td>
<td>Gibt an, ob der Decoder die DirectX-Videobeschleunigungshardware verwendet, falls verfügbar.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></td>
<td>Gibt den Leistungspegel für den Decoder an.<br/> <dl> Windows 7.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></td>
<td>Gibt an, ob der Decoder Frameinterpolation verwenden soll.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></td>
<td>Gibt an, ob der Decoder Frameinterpolation unterstützt.<br/> <dl> Windows XP und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild<br />
Schreibgeschützt.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></td>
<td>Gibt die Anzahl der Threads an, die der Decoder verwendet.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Lese-/Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></td>
<td>Gibt den Nachverarbeitungsmodus für den Decoder an.<br/> <dl> Windows Vista und höher.<br />
Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />
Nur Schreibzugriff.<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>g_wszWMVCNeedsDrain</strong></td>
<td>Gibt an, ob der Decoder entleert werden soll.<br/> <dl> Windows 8<br />
Schreibgeschützt.<br />
</dl> Diese Eigenschaft wird von der Windows Media Format-Runtime verwendet. Der Eigenschaftentyp ist <strong>VARIANT_BOOL.</strong> Wenn der Wert <strong>VARIANT_TRUE</strong>ist, sollte der Decoder nach einer Diskontinuität entleert werden. Weitere Informationen zum Leeren eines MFT finden Sie unter <a href="basic-mft-processing-model.md">Grundlegendes MFT-Verarbeitungsmodell.</a><br/>
<blockquote>
[!Note]<br />
Verwenden Sie zum Abfragen dieser Eigenschaft die <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag-Schnittstelle.</strong></a>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

Die maximale Auflösung, die vom Windows Media Video 9-Decoder zugelassen wird, beträgt 4096 x 4096.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codecimplementierung](codecimplementation.md)
</dt> </dl>

 

 
