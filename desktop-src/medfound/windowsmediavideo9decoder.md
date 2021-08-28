---
description: Der Windows Media Video 9-Decoder decodiert Videostreams, die vom Windows Media Video Encoder codiert wurden.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Windows Media Video 9-Decoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df973e78f69e1f1ff0e649b2c4f5637380be9f27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474306"
---
# <a name="windows-media-video-9-decoder"></a>Windows Media Video 9-Decoder

Der Windows Media Video 9-Decoder decodiert Videostreams, die vom [**Windows Media Video Encoder**](windowsmediavideo9encoder.md)codiert wurden. Encoder und Decoder unterstützen die folgenden vier Kategorien codierter Videos.

-   Windows Media Video 9 Simple Profile
-   Windows Medienvideo 9: Hauptprofil
-   Windows Media Video 9 – Erweitertes Profil
-   Windows Media Video 9.1 Image

## <a name="class-identifier"></a>Klassenbezeichner

Der Klassenbezeichner (CLSID) für den Windows Media Video-Decoder wird durch die konstante **CLSID \_ CWMVDecMediaObject** dargestellt. Sie können eine Instanz des Videodecoders erstellen, indem Sie **CoCreateInstance** aufrufen.

## <a name="interfaces"></a>Schnittstellen

Ein Videodecoderobjekt macht die [**IMediaObject-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) verfügbar, sodass das Objekt als DirectX-Medienobjekt (DMO) verwendet werden kann, und macht die [**INTERFACESTransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) verfügbar, sodass das Objekt als Media Foundation Transform (MFT) verwendet werden kann.

Ein Videodecoder verhält sich als DMO oder MFT, je nachdem, welche Schnittstellen Sie erhalten und welche Version von Windows ausgeführt wird. Die folgende Tabelle zeigt die Bedingungen, unter denen sich ein Videodecoder als DMO oder MFT verhält.



| Betriebssystem            | Decoderverhalten                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Ein Windows Medienvideodecoder verhält sich immer als DMO.                                                                                                                |
| Windows Vista und Windows 7 | Standardmäßig verhält sich ein Windows Media-Videodecoder als DMO. Wenn Sie eine [**DECODERTransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) für einen Videodecoder erhalten, verhält sie sich wie ein MFT. |



 

Ab Windows 7 implementiert der Windows Media Video-Decoder die [**IDMOQualityControl-Schnittstelle.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol)

## <a name="input-formats"></a>Eingabeformate

Die folgende Tabelle zeigt die vierstelligen Codes (FOURCCs), die den Kategorien codierter Eingaben entsprechen, die vom Windows Media Video-Decoder unterstützt werden.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Media Video 9 Simple Profile   | "WMV3"                                   |
| Windows Medienvideo 9: Hauptprofil     | "WMV3"                                   |
| Windows Media Video 9 – Erweitertes Profil | "WVC1"                                   |
| Windows Media Video 9.1 Image          | "WMVP" für 9.1, "WVP2" für Version 2 9.1 |



 

## <a name="output-formats"></a>Ausgabeformate

Der Windows Media Video-Decoder unterstützt die folgenden Ausgabemedienuntertypen, wenn er als DMO fungiert.

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYO
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Der Windows Media Video-Decoder unterstützt die folgenden Ausgabemedienuntertypen, wenn er als MFT fungiert.

-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ YVTEROPERABILITÄT
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="properties"></a>Eigenschaften

Der Windows Media Video-Decoder unterstützt die folgenden Eigenschaften.




| Eigenschaft | BESCHREIBUNG | 
|----------|-------------|
| <a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a> | Gibt an, ob der Codec Videoframes mit Zeilensprung aus dem komprimierten Stream als progressive Frames decodiert.<br /><dl> Windows XP und höher.<br />Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />Lese-/Schreibzugriff.<br /></dl> | 
| <a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a> | Gibt an, ob der Decoder DirectX-Videobeschleunigungshardware verwendet, falls verfügbar.<br /><dl> Windows XP und höher.<br />Einfaches Profil, Hauptprofil, Erweitertes Profil.<br />Nur Schreibzugriff.<br /></dl> | 
| <a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a> | Gibt die Leistungsstufe für den Decoder an.<br /><dl> Windows 7.<br />Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />Lese-/Schreibzugriff.<br /></dl> | 
| <a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a> | Gibt an, ob der Decoder die Frameinterpolation verwenden soll.<br /><dl> Windows XP und höher.<br />Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />Nur Schreibzugriff.<br /></dl> | 
| <a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a> | Gibt an, ob der Decoder die Frameinterpolation unterstützt.<br /><dl> Windows XP und höher.<br />Einfaches Profil, Hauptprofil, Erweitertes Profil, Image<br />Schreibgeschützt.<br /></dl> | 
| <a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a> | Gibt die Anzahl der Threads an, die vom Decoder verwendet werden.<br /><dl> Windows Vista und höher.<br />Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />Lese-/Schreibzugriff.<br /></dl> | 
| <a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a> | Gibt den Nachverarbeitungsmodus für den Decoder an.<br /><dl> Windows Vista und höher.<br />Einfaches Profil, Hauptprofil, Erweitertes Profil, Bild.<br />Nur Schreibzugriff.<br /></dl> | 
| <strong>g_wszWMVCNeedsDrain</strong> | Gibt an, ob der Decoder entladen werden soll.<br /><dl> Windows 8<br />Schreibgeschützt.<br /></dl> Diese Eigenschaft wird von der Windows Media Format Runtime verwendet. Der Eigenschaftentyp ist <strong>VARIANT_BOOL</strong>. Wenn der Wert <strong>VARIANT_TRUE</strong>ist, sollte der Decoder nach einer Diskontinuität entladen werden. Weitere Informationen zum Entladen eines MFT finden Sie unter <a href="basic-mft-processing-model.md">Grundlegendes MFT-Verarbeitungsmodell.</a><br /><blockquote>[!Note]<br />Verwenden Sie die <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag-Schnittstelle,</strong></a> um diese Eigenschaft abzufragen.</blockquote><br /> | 




 

## <a name="remarks"></a>Hinweise

Die maximale Auflösung, die vom Windows Media Video 9-Decoder zugelassen wird, beträgt 4096 x 4096.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista oder Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> <dt>

[Codecimplementierung](codecimplementation.md)
</dt> </dl>

 

 
