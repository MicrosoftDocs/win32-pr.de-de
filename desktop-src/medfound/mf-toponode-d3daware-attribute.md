---
description: Gibt an, ob die einem topologieknoten zugeordnete Transformation die DirectX-Video Beschleunigung (DXVA) unterstützt.
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: MF_TOPONODE_D3DAWARE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d94d06f2834092159fb813ecffd69ec8a157c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485811"
---
# <a name="mf_toponode_d3daware-attribute"></a>MF \_ toponode \_ D3DAWARE-Attribut

Gibt an, ob die einem topologieknoten zugeordnete Transformation die DirectX-Video Beschleunigung (DXVA) unterstützt.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Transformations Knoten (**MF- \_ topologietransformations- \_ \_ Knoten**).

Anwendungen verwenden dieses Attribut in der Regel nicht direkt. Die Medien Sitzung legt dieses Attribut für einen Transformations Knoten fest, wenn die zugrunde liegende Media Foundation Transformation über das D3D-Attribut " [**MF \_ sa \_ \_**](mf-sa-d3d-aware-attribute.md) " verfügt.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Topologieknotenattribute](topology-node-attributes.md)
</dt> </dl>

 

 




