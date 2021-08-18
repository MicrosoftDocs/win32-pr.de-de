---
description: Gibt an, wie viele Puffer die Videobeispielzuweisung für jedes Videobeispiel erstellt.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: MF_SA_BUFFERS_PER_SAMPLE -Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6b54cc5b2589649c954d9f2f41923af04fdf4aa7c00714067bee0b11dabbee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740367"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a>MF \_ SA \_ BUFFERS PER \_ \_ SAMPLE-Attribut

Gibt an, wie viele Puffer die Videobeispielzuweisung für jedes Videobeispiel erstellt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Wenn Sie die [**BENUTZEROBERFLÄCHENVIDEOSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) zum Zuordnen von Videobeispielen verwenden, können Sie dieses Attribut verwenden, um Videobeispiele zu erstellen, die mehrere Puffer enthalten. Wenn der Attributwert beispielsweise 2 ist, erstellt die Zuweisung zwei Videopuffer für jedes Videobeispiel. Legen Sie das -Attribut im *pAttributes-Parameter* der [**METHODE PICKVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) fest.

Der Standardwert ist 1. Wenn das Attribut nicht festgelegt ist, erstellt die Zuweisung Videobeispiele, die einen einzelnen Puffer pro Stichprobe enthalten.

Dieses Attribut ist in der folgenden Situation Media Foundation Transformationen (MFTs) vorgesehen, die Stereo-3D-Ausgaben unterstützen:

-   MFT unterstützt Microsoft DirectX Graphic Infrastructure (DXGI).
-   MFT weist eigene Ausgabebeispiele zu.
-   Der MFT verwendet die [**BENUTZEROBERFLÄCHEVideoSampleAllocatorEx-Schnittstelle,**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) um die Ausgabebeispiele zu zuordnen.
-   Das 3D-Videoformat verwendet für jede Ansicht einen separaten Puffer.

Wenn alle diese Kriterien erfüllt sind, sollte MFT den Attributwert auf 2 (einen Puffer pro Ansicht) festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




