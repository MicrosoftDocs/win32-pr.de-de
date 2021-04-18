---
description: Gibt eine lokale Plug-in-Steuerungs Richtlinie an.
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: MF_LOCAL_PLUGIN_CONTROL_POLICY-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1bdaee17651cebfdc844bb5b6998907b1cd295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351155"
---
# <a name="mf_local_plugin_control_policy-attribute"></a>\_ \_ \_ Richtlinien Attribut für lokales MF-Plug-in \_

Gibt eine lokale Plug-in-Steuerungs Richtlinie an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Legen Sie dieses Attribut auf eines der MF-Plug-in- [**\_ \_ Steuerungs \_ Richtlinien**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) Werte fest.

Diese Attribute ermöglichen der APP, eine restriktivere lokale Richtlinie als die Prozess weite Richtlinie anzugeben, die von [**imfplugincontrol**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)konfiguriert wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




