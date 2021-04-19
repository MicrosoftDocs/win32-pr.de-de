---
description: Gibt die CLSID eines Nachbearbeitungs-Plug-Ins für ein Video Erfassungsgerät an.
ms.assetid: 8F626FAA-C7B8-4DBA-BD65-7CE97CBF3A86
title: MF_DEVICESTREAM_EXTENSION_PLUGIN_CLSID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25c7ea9973b73cf6f1157eb19609293f2766d38f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356519"
---
# <a name="mf_devicestream_extension_plugin_clsid-attribute"></a>\_CLSID-Attribut "MF devicestream \_ Extension \_ Plugin \_ "

Gibt die CLSID eines Nachbearbeitungs-Plug-Ins für ein Video Erfassungsgerät an.

## <a name="data-type"></a>Datentyp

**GUID**

## <a name="remarks"></a>Bemerkungen

Ein nachträglich verarbeitetes Plug-in ist eine MFT, die das Video Bild nach der Erfassung verarbeitet. Der Hardwarehersteller kann ein nachträglich verarbeitetes Plug-in als Teil des Installationspakets einschließen. Wenn dies der Fall ist, legt die Video Erfassungs Quelle das \_ CLSID-Attribut "MF devicestream \_ Extension \_ Plugin" \_ auf die CLSID des Plug-ins fest.

Gehen Sie folgendermaßen vor, um dieses Attribut zu erhalten:

1.  Fragen Sie die Medienquelle für die [**imfmediasourceex**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) -Schnittstelle ab.
2.  Aufrufen von [**imfmediasourceex:: getstreamattributs**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) , um einen [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Zeiger für den Stream zu erhalten.
3.  Aufrufen Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) , um das Attribut abzurufen.

Um das Plug-in zu erstellen, rufen Sie [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)auf.

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

 

 
