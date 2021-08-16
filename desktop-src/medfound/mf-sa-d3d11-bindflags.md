---
description: Gibt die Bindungsflags an, die beim Zuordnen von Microsoft Direct3D 11-Oberflächen für Medienbeispiele verwendet werden sollen.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: MF_SA_D3D11_BINDFLAGS-Attribut (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65f0fbc607ccdc8f878e25109fcadfdf8956007d99909d9a21c0e668951106d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102463"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a>MF \_ SA \_ D3D11 \_ BINDFLAGS-Attribut

Gibt die Bindungsflags an, die beim Zuordnen von Microsoft Direct3D 11-Oberflächen für Medienbeispiele verwendet werden sollen.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Der Wert dieses Attributs ist ein bitweises **OR** von [**D3D11 \_ BIND FLAG-Flags. \_**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag)

### <a name="microsoft-media-foundation-transforms"></a>Microsoft Media Foundation Transformationen

In diesem Kontext gilt das -Attribut nur, wenn die Microsoft Media Foundation-Transformation (MFT) **TRUE** für das [MF SA \_ \_ D3D11 \_ AWARE-Attribut](mf-sa-d3d11-aware.md) zurückgibt.

Wenn ein MFT Direct3D 11 unterstützt, stellt dieses Attribut einen Hinweis auf den MFT bereit, wenn Microsoft Direct3D-Oberflächen für die Ausgabe zugeordnet werden. Legen Sie das Attribut wie folgt fest:

1.  Rufen Sie [**ÜBERTRANSFORM::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) auf, um den MFT-Attributspeicher abzurufen.
2.  Rufen Sie [**DIE ATTRIBUTEAttributes::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Die Media Foundation Pipeline legt das Attribut fest, bevor das Streaming gestartet wird. Der MFT sollte versuchen, die Einstellung beim Zuordnen von Oberflächen zu berücksichtigen. Wenn dies nicht möglich ist, kann der MFT das Attribut ignorieren, anstatt die Zuordnung zu verfehlen.

Wenn der MFT direct3D-Oberflächen für die Eingabe erfordert, kann dieses Attribut außerdem als Hinweis darauf verfügbar gemacht werden, wie die Eingabeoberflächen zugeordnet werden sollen. Fragen Sie das Attribut wie folgt ab:

1.  Rufen Sie [**ÜBERTRANSFORM::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) auf, um die Eingabestreamattribute abzurufen.
2.  Rufen Sie [**DIE ATTRIBUTEAttributes::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

### <a name="sample-allocator"></a>Beispielzuweisung

Dieses Attribut kann für die Zuweisung von Videobeispielen in der [**ALLOCATVideoSampleAllocatorEx::InitializeSampleAllocatorEx-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 \|Desktop-Apps UWP-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 \|Desktop-Apps UWP-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
