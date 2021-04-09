---
description: Dieses Attribut gibt zusätzlichen Schutz an, der von einer Video-Output Trust Authority (OTA) geboten wird, wenn ein Connector keinen Ausgabe Schutz bietet.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: MFPROTECTION_CONSTRICTVIDEO_NOOPM-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959241"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a>Noopm-Attribut für MF Protection- \_ \_ Attribut

Dieses Attribut gibt zusätzlichen Schutz an, der von einer Video-Output Trust Authority (OTA) geboten wird, wenn ein Connector keinen Ausgabe Schutz bietet.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Dies ist ein zusätzlicher Schutz, der von einer Video-Output Trust Authority (OTA) geboten wird, wenn ein Connector keinen Ausgabe Schutz bietet (siehe [**IMF outputtrustauthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)). In diesem Fall bietet das OTA ggf. diesen Schutz, dessen Auswirkung mit dem Schutz durch den Schutz durch den [mfprotection-Schutz \_ überein](mfprotection-constrictvideo.md) stimmt. Dies wird definiert, um Verwechslungen mit vorherigen Aufrufen von [**imfoutputpolicy:: generaterequiredschemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) -Interaktionen zu vermeiden, bei denen das vorhanden sein von "mfprotection" \_ für den Connector "Windows-Manager" verwendet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




