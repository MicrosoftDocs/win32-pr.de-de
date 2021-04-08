---
description: Gibt an, ob die MPEG-4-Datei Senke Sequence Parameter Set (SPS) und Picture Parameter Set (PPS) nalus filtert.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: MF_MPEG4SINK_SPSPPS_PASSTHROUGH-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754273"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>MF \_ MPEG4SINK \_ spspps- \_ Passthrough-Attribut

Gibt an, ob die [**MPEG-4-Datei Senke**](mpeg-4-file-sink.md) Sequence Parameter Set (SPS) und Picture Parameter Set (PPS) nalus filtert.

## <a name="data-type"></a>Datentyp

**Bool** gespeichert als **UInt32**

## <a name="applies-to"></a>Gilt für:

[**Imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>Bemerkungen

Die [**MPEG-4-Datei Senke**](mpeg-4-file-sink.md) schreibt die SPS-und PPS-Parameter in das Feld für die Beispiel Beschreibung der MP4-Datei. Standardmäßig werden SPS und PPS nalus aus dem Videostream herausgefiltert. Um dieses Verhalten zu überschreiben, legen \_ Sie das Attribut "MF MPEG4SINK \_ spspps \_ Passthrough" auf **true** fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




