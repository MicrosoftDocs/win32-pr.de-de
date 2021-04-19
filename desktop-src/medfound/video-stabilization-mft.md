---
description: Die MFT für die Videostabilisierung ist eine Microsoft Media Foundation Transformation (MFT), die eine Bildstabilisierung für einen Videostream ausführt.
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: Videostabilisierung MFT (camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373976"
---
# <a name="video-stabilization-mft"></a>Videostabilisierung-MFT

Die MFT für die Videostabilisierung ist eine Microsoft Media Foundation Transformation (MFT), die eine Bildstabilisierung für einen Videostream ausführt.

## <a name="clsid"></a>CLSID

CLSID \_ cmsvideodspmft

## <a name="interfaces"></a>Schnittstellen

-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**Imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMF-Empfehlung**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**Imediaextension**](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a>Eingabeformate

Der Eingabe Medientyp und die Untertypen, die von der Video Stabilisierungs-MFT für unkomprimierte Videos akzeptiert werden, lauten wie folgt:

-   **MediaType- \_ Video**
-   **Mediasubtype \_ NV12**
-   **Mediasubtype \_ im YUY2**

## <a name="output-formats"></a>Ausgabeformate

Der von der Video Stabilisierungs-MFT akzeptierte Ausgabe Medientyp und untergeordnete typkombinationen lauten:

-   **MediaType- \_ Video**
-   **Mediasubtype \_ NV12**

Der Eingabe Medientyp muss vor dem Ausgabe Medientyp festgelegt werden. In den meisten Fällen stellt die eingeschränkte Formatunterstützung kein Problem dar, da die Pipeline automatisch die erforderlichen Farb Konvertierungen einfügt.

Die MFT-Komponente für die Videostabilisierung ist in der Lage, sich bei Eingabe Änderungen dynamisch zu ändern. Wenn sich die Größe des Eingabe Bilds ändert oder der Untertyp geändert wird, löst er eine dynamische Formatänderung im Ausgabestream aus.

Die MFT für die Videostabilisierung führt in den folgenden Fällen zu einer Farbkonvertierung:

-   Wenn das Eingabeformat **mediasubtype \_ im YUY2** ist.
-   Wenn der Microsoft DirectX 9,0-Kompatibilitätsmodus verwendet wird.

### <a name="attributes"></a>Attribute

Die folgenden Attribute werden von der Video Stabilisierungs-MFT über die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle unterstützt.

-   Das Attribut [MF \_ videodsp \_ Mode](mf-videodsp-mode.md) versetzt die Videostabilisierung in den Stabilisierungs Modus oder den Pass-Through-Modus. Die Anwendung sollte [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) für den GUID- **MF- \_ videodsp- \_ Typ** mit einer Ganzzahl aufrufen, die einem der folgenden gültigen Werte entspricht: **mfvideodspmode \_ Stabilisierung** = 4, **mfvideodspmode \_ Passthrough** = 1. Der MF- \_ videodsp- \_ Modus kann jederzeit während der Wiedergabe geändert werden. Dies bewirkt eine Änderung des dynamischen Modus. Die Ausgabe wird nach dem Ändern des Attributs entweder nach einem 16-oder 2-Rahmen (abhängig vom Latenz Modus) zu "stabilisiert" oder "durchlaufen" gewechselt.
-   Das Attribut [MF \_ niedrige \_ Latenz](mf-low-latency.md) versetzt die Videostabilisierung in den Modus mit niedriger Latenz oder den Modus für hohe Qualität. Die Anwendung sollte [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) für die GUID- **MF- \_ niedrige \_ Latenz** mit einer Ganzzahl, die einem der folgenden gültigen Werte entspricht, anrufen: geringe Latenz = 1 hohe Qualität = 0
-   Das Attribut [MF \_ sa \_ D3D11 \_ bindflags](mf-sa-d3d11-bindflags.md) wird von der Pipeline verwendet, um die D3D11-Bindungsflags anzugeben, mit denen die Ausgabe Beispiele erstellt werden. Eine beliebige Kombination von Werten aus der [**D3D11 \_ Bind- \_ Flag**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) -Enumeration ist gültig.
-   Die **\_ \_ Mindestanzahl von \_ Ausgabe \_ Beispielen \_** für das Attribut MF wird von der Pipeline verwendet, um die Mindestanzahl von Samplings anzugeben, die von dieser Komponente bei der Ausgabe unterstützt werden müssen.
-   Das Attribut [mfsampleextension \_ videodspmode](mfsampleextension-videodspmode.md) wird für jedes durch die Stabilisierung erzeugte Beispiel festgelegt, um den effektiven [MF- \_ videodsp- \_ Modus](mf-videodsp-mode.md) anzugeben, der auf das Beispiel angewendet wurde (unabhängig davon, ob das Beispiel stabilisiert wurde). Unter bestimmten Bedingungen werden Stichproben möglicherweise nicht stabilisiert (aufgrund einer hohen Systemlast oder von Anforderungen des Benutzers). Dieses Attribut hat die gleichen Werte wie das MF \_ videodsp \_ mode-Attribut (**MF videodspmode- \_ Stabilisierung** und **MF videodspmode \_ Passthrough**). Wenn Sie den Wert dieses Attributs abrufen möchten, sollten Anwendungen [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) für die GUID **mfsampleextension \_ videodspmode** aufrufen.

## <a name="remarks"></a>Bemerkungen

Eine Instanz des Video Stabilisierungs-DSP kann auf eine der folgenden Arten erstellt werden:

-   Durch Aufrufen von [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Der Video Stabilisierungs-DSP ist unter der Kategorie **\_ \_ Video \_ Effekt der MFT-Kategorie** registriert.
-   Durch Aufrufen der com-Funktion **CoCreateInstance** , die ihr die CLSID- **CLSID \_ cmsvideodspmft** übergibt. Um diese Methode verwenden zu können, müssen Sie "wmcodecdsp. h" einschließen und eine Verknüpfung mit "wmcodecdspuuid. lib" herstellen.

Darüber hinaus unterstützt der videostabilisierungs-DSP die Instanziierung mithilfe von Windows-Runtime als Windows Media-Erweiterung. Es wird auf [**Windows. Media. videoeffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)definiert, und der vollständige Name lautet "Windows. Media. videoeffects. videostabilization".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Digitale Signal Prozessoren](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
