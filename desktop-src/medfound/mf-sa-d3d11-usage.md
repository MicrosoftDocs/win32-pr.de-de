---
description: Gibt an, wie Microsoft Direct3D 11-Oberflächen für Medienbeispiele reserviert werden.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: MF_SA_D3D11_USAGE -Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7364b9777d94baa1a6c25aead6631ad6b11dcddc12db83698da04affebe0fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663950"
---
# <a name="mf_sa_d3d11_usage-attribute"></a>MF \_ SA \_ D3D11 \_ USAGE-Attribut

Gibt an, wie Microsoft Direct3D 11-Oberflächen für Medienbeispiele reserviert werden. Die Nutzung gibt direkt an, ob die CPU oder GPU auf ein Beispiel zu zugegriffen werden kann.

## <a name="data-type"></a>Datentyp

**D3D11 \_ USAGE** als **UINT32 gespeichert**

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein [**D3D11 \_ USAGE-Wert.**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage)

### <a name="microsoft-media-foundation-transforms"></a>Microsoft Media Foundation Transformationen

In diesem Kontext gilt das -Attribut nur, wenn die Microsoft Media Foundation-Transformation (MFT) **TRUE** für das [MF \_ SA \_ D3D11 \_ AWARE-Attribut zurückgibt.](mf-sa-d3d11-aware.md)

Wenn ein MFT Direct3D 11 unterstützt, stellt dieses Attribut einen Hinweis für MFT bei der Zuweisung von Microsoft Direct3D-Oberflächen für die Ausgabe zur Verfügung. Legen Sie das Attribut wie folgt fest:

1.  Rufen [**Sie DEN MFT-Attributspeicher**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) auf, um DEN MFT-Attributspeicher zu erhalten.
2.  Rufen [**Sie DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Die Media Foundation-Pipeline legt das -Attribut fest, bevor das Streaming gestartet wird. MFT sollte versuchen, die Einstellung beim Zuordnen von Oberflächen zu verwenden. Wenn dies nicht möglich ist, kann MFT das Attribut ignorieren, anstatt die Zuordnung zu fehlschlagen.

Wenn für MFT Direct3D-Oberflächen für die Eingabe erforderlich sind, kann dieses Attribut außerdem als Hinweis dafür verfügbar sein, wie die Eingabeoberflächen zugeordnet werden sollen. Fragen Sie das Attribut wie folgt ab:

1.  Rufen [**Sie ZUM Erhalten der Eingabestreamattribute DEN WERT FÜR DIETRANSFORM::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) auf.
2.  Rufen [**Sie DIE ATTRIBUTE::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

### <a name="sample-allocator"></a>Beispielzuweisung

Dieses Attribut kann für die Videobeispielbelegung in der [**METHODE ALLOCATVideoSampleAllocatorEx::InitializeSampleAllocatorEx festgelegt**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
