---
description: Gibt an, dass Nalu-Längen Informationen als BLOB mit jedem komprimierten H. 264-Beispiel gesendet werden.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: MF_NALU_LENGTH_SET-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350144"
---
# <a name="mf_nalu_length_set-attribute"></a>Attribut "MF \_ Nalu \_ length \_ Set"

Gibt an, dass Nalu-Längen Informationen als **BLOB** mit jedem komprimierten H. 264-Beispiel gesendet werden.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Legen Sie dieses Attribut für den Eingabe Medientyp mediasubtype \_ H264 fest.

Legen Sie \_ \_ \_ die für den Eingabe Medientyp des H. 264-Decoders festgelegte MF-Nalu-Länge fest, und geben Sie an, dass für jedes Eingabe Beispiel eine Nalu-Länge verfügbar ist und jede Eingabe Stichprobe ein ganzes

Das **BLOB** , das die Nalu-Längen Informationen enthält, kann aus dem [MF- \_ Nalu- \_ Längen \_ Informations](mf-nalu-length-information.md) Attribut für das Eingabe Beispiel abgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Medientyp Attribute](media-type-attributes.md)
</dt> </dl>

 

 




