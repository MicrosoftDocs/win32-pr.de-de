---
description: Gibt an, ob die Medien Sitzung vorab auf der Medien Senke, die durch diesen topologieknoten dargestellt wird, verwendet wird.
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: MF_TOPONODE_DISABLE_PREROLL-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373314"
---
# <a name="mf_toponode_disable_preroll-attribute"></a>MF- \_ toponode- \_ Attribut deaktivieren ( \_ vorab)

Gibt an, ob die Medien Sitzung vorab auf der Medien Senke, die durch diesen topologieknoten dargestellt wird, verwendet wird.

## <a name="data-type"></a>Datentyp

**UINT32**

Als booleschen Wert behandeln.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut gilt für Ausgabe Knoten (**MF- \_ topologieausgabe- \_ \_ Knoten**).

Wenn der Wert dieses Attributs **true** ist, werden von der Medien Sitzung keine Daten für die Medien Senke vorab erstellt, auch wenn die Medien Senke die [**imfmediasinkpreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) -Schnittstelle verfügbar macht. Wenn der Wert **false** ist, werden die Daten in der Medien Sitzung vorab erstellt, wenn die Medien Senke **imfmediasinkpreroll** implementiert. Der Standardwert ist **FALSE**.

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

 

 




