---
description: Gibt den kernelstreamingbezeichner für einen Datenstrom auf einem Video Erfassungsgerät an.
ms.assetid: 03C48CBA-FAD0-4127-89E5-3F1874BF32DB
title: MF_DEVICESTREAM_STREAM_ID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f7143487af1125da9334fc39c152aee9363b97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041961"
---
# <a name="mf_devicestream_stream_id-attribute"></a>Das MF- \_ Attribut "devicestream \_ Stream \_ ID"

Gibt den kernelstreamingbezeichner für einen Datenstrom auf einem Video Erfassungsgerät an.

## <a name="data-type"></a>Datentyp

**UINT32**

## <a name="remarks"></a>Bemerkungen

Gehen Sie folgendermaßen vor, um dieses Attribut zu erhalten:

1.  Fragen Sie die Medienquelle für die [**imfmediasourceex**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) -Schnittstelle ab.
2.  Aufrufen von [**imfmediasourceex:: getstreamattributs**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , um einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger für den Stream zu erhalten.
3.  Zum Abrufen des Attributs muss [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




