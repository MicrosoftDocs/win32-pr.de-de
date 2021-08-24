---
description: Dieses Attribut gibt zusätzlichen Schutz an, der von einer Videoausgabe-Vertrauensstellungsstelle (Video Output Trust Authority, OTA) geboten wird, wenn ein Connector keinen Ausgabeschutz bietet.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: MFPROTECTION_CONSTRICTVIDEO_NOOPM-Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72d1d7cd858ec9cf254cca1dffc5fef4e24fbb5a3a288975a9f70c9ae118dde3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713740"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a>MFPROTECTION \_ CONSTRICTVIDEO \_ NOOPM-Attribut

Dieses Attribut gibt zusätzlichen Schutz an, der von einer Videoausgabe-Vertrauensstellungsstelle (Video Output Trust Authority, OTA) geboten wird, wenn ein Connector keinen Ausgabeschutz bietet.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Hinweise

Dies ist ein zusätzlicher Schutz, der von einer Videoausgabe-Vertrauensstellungsstelle (Video Output Trust Authority, OTA) geboten wird, wenn ein Connector keinen Ausgabeschutz bietet (weitere Informationen finden Sie unter [**DEROUTPUTTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)). In diesem Fall kann die OTA diesen Schutz bieten, dessen Auswirkung mit dem [MFPROTECTION \_ CONSTRICTVIDEO-Schutz](mfprotection-constrictvideo.md) identisch ist. Dies wird definiert, um Verwechslungen mit vorherigen Aufrufen von [**INTERACTIONSOutputPolicy::GenerateRequiredSchemas-Interaktionen**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) zu vermeiden, bei denen das Vorhandensein des MFPROTECTION \_ CONSTRICTVIDEO-Schutzes verwendet wurde, um den Pseudoconnector des Desktopfenster-Managers zu identifizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




