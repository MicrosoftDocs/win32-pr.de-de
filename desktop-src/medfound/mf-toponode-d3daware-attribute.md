---
description: Gibt an, ob die einem Topologieknoten zugeordnete Transformation DirectX Video Acceleration (DXVA) unterstützt.
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: MF_TOPONODE_D3DAWARE-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e49735a1178cc521efd152f4fa11ab7c84069b07d0e5001f0f0e8e38bec940ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607150"
---
# <a name="mf_toponode_d3daware-attribute"></a>MF \_ TOPONODE \_ D3DAWARE-Attribut

Gibt an, ob die einem Topologieknoten zugeordnete Transformation DirectX Video Acceleration (DXVA) unterstützt.

## <a name="data-type"></a>Datentyp

**UINT32**

Als boolescher Wert behandeln.

## <a name="remarks"></a>Hinweise

Dieses Attribut gilt für Transformationsknoten (**MF \_ TOPOLOGY \_ TRANSFORM \_ NODE**).

Anwendungen verwenden dieses Attribut in der Regel nicht direkt. Die Mediensitzung legt dieses Attribut auf einem Transformationsknoten fest, wenn die zugrunde liegende Media Foundation Transformation über das [**MF \_ SA \_ D3D \_ AWARE-Attribut verfügt.**](mf-sa-d3d-aware-attribute.md)

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**DENKattribute::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**TOPOLOGYNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




