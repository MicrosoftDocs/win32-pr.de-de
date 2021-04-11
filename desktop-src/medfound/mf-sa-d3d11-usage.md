---
description: Gibt an, wie Microsoft Direct3D 11-Oberflächen für Medien Beispiele zugeteilt werden.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: MF_SA_D3D11_USAGE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0609435cf42134f28e8464fd3173412836c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214885"
---
# <a name="mf_sa_d3d11_usage-attribute"></a>MF \_ sa \_ D3D11 \_ Usage-Attribut

Gibt an, wie Microsoft Direct3D 11-Oberflächen für Medien Beispiele zugeteilt werden. Die Verwendung gibt direkt an, ob eine Stichprobe für die CPU oder die GPU zugänglich ist.

## <a name="data-type"></a>Datentyp

**D3D11 \_** Als **UInt32** gespeicherte Verwendung

## <a name="remarks"></a>Bemerkungen

Der Wert dieses Attributs ist ein [**D3D11 \_ Usage**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) -Wert.

### <a name="microsoft-media-foundation-transforms"></a>Microsoft Media Foundation Transformationen

In diesem Kontext wird das-Attribut nur angewendet, wenn die Microsoft Media Foundation Transformation (MFT) **true** für das MF-Attribut [ \_ \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) zurückgibt.

Wenn eine MFT Direct3D 11 unterstützt, stellt dieses Attribut einen Hinweis für die MFT bereit, wenn Microsoft Direct3D-Oberflächen für die Ausgabe zugewiesen werden. Legen Sie das-Attribut wie folgt fest:

1.  Aufrufen von [**imftransform:: getoutputstreamtribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) zum Abrufen des MFT-Attribut Speicher.
2.  Rückrufe [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Die Media Foundation Pipeline legt das-Attribut vor dem Starten des Streamings fest. Der MFT sollte die Einstellung bei der Zuweisung von Oberflächen berücksichtigen. Wenn dies nicht möglich ist, kann das MFT das Attribut ignorieren und nicht die Zuordnung.

Wenn der MFT außerdem Direct3D-Oberflächen für die Eingabe erfordert, kann er dieses Attribut als Hinweis dafür verfügbar machen, wie die Eingabe Oberflächen zugeordnet werden sollen. Fragen Sie das Attribut wie folgt ab:

1.  Aufrufen von [**imftransform:: getinputstreamattributs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) , um die Eingabedaten Strom Attribute abzurufen.
2.  Rückrufe [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

### <a name="sample-allocator"></a>Beispiel Zuweisung

Dieses Attribut kann für die Video Sample-Zuweisung in der [**IMF-Methode IMF videosamplezuordcatorex:: initializesampledepcatorex**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) festgelegt werden.

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

 

 
