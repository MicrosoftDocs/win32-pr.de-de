---
description: Gibt an, wie viele Puffer der Video-Sample-Zuweisung für jedes Video Beispiel erstellt.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: MF_SA_BUFFERS_PER_SAMPLE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d658ae72c53d986b364b2b6a3f405ae0052ea3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753176"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a>MF- \_ sa- \_ Puffer \_ pro Sample- \_ Attribut

Gibt an, wie viele Puffer der Video-Sample-Zuweisung für jedes Video Beispiel erstellt.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Wenn Sie Videobeispiele mit der [**imfvideosamplealloerorex**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) -Schnittstelle zuordnen, können Sie mit diesem Attribut Videobeispiele erstellen, die mehrere Puffer enthalten. Wenn der-Attribut Wert z. b. 2 ist, erstellt die Zuweisung zwei Video Puffer für jedes Video Beispiel. Legen Sie das-Attribut im *pattributes* -Parameter der [**IMF videosamplezuzuweisung:: initializesamplezuweisung**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) -Methode fest.

Der Standardwert ist 1. Wenn das-Attribut nicht festgelegt ist, erstellt die Zuweisung Videobeispiele, die einen einzelnen Puffer pro Stichprobe enthalten.

Dieses Attribut ist in der folgenden Situation primär für Media Foundation Transformationen (MFTs) vorgesehen, die eine Stereo-3D-Ausgabe unterstützen:

-   Der MFT unterstützt die Microsoft DirectX Graphics Infrastructure (DXGI).
-   Der MFT weist seine eigenen Ausgabe Beispiele zu.
-   Die MFT verwendet die [**imfvideosamplealloerorex**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) -Schnittstelle, um die Ausgabe Beispiele zuzuordnen.
-   Das 3D-Videoformat verwendet für jede Ansicht einen separaten Puffer.

Wenn alle diese Kriterien zutreffen, sollte der MFT den Attribut Wert auf 2 festlegen (ein Puffer pro Ansicht).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




