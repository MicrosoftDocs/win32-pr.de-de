---
description: Gibt eine lokale Plug-In-Steuerungsrichtlinie an.
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: MF_LOCAL_PLUGIN_CONTROL_POLICY -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83f32280f48895b9b6a0633613d63f787836573fe13f046126639c28467abe02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956460"
---
# <a name="mf_local_plugin_control_policy-attribute"></a>MF \_ LOCAL PLUGIN CONTROL \_ \_ \_ POLICY-Attribut

Gibt eine lokale Plug-In-Steuerungsrichtlinie an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Hinweise

Legen Sie dieses Attribut auf einen der [**MF-PLUG-IN-STEUERUNGSRICHTLINIE-Werte \_ \_ \_**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) fest.

Mit diesen Attributen kann die App eine restriktivere lokale Richtlinie als die prozessweite Richtlinie angeben, die von [**DERPluginControl konfiguriert wurde.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientypattribute](media-type-attributes.md)
</dt> </dl>

 

 




