---
description: Ruft den Verdienst Wert eines Hardware Codecs ab.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf310ae3dafee7823119b2d5d5bd2c6b61fe822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215028"
---
# <a name="opm_get_codec_info"></a>OPM- \_ get- \_ Codec- \_ Informationen

Ruft den Verdienst Wert eines Hardware Codecs ab.



| Anforderung | Wert |
|--------------|-------------------------------------------------------------------------------------------|
| Anforderungs-GUID | **OPM- \_ get- \_ Codec- \_ Informationen**                                                                 |
| Eingabedaten   | Eine [**OPM- \_ get \_ Codec \_ Info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) -Struktur   |
| Daten zurückgeben  | Eine [**OPM- \_ get- \_ Codec- \_ \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) Struktur |



 

## <a name="remarks"></a>Bemerkungen

Obwohl dieser Befehl die Schnittstelle des [Output Protection Managers](output-protection-manager.md) (OPM) verwendet, gilt er nur für Hardware Encoder und-Decoder. Dies gilt nicht für Videoausgabe Geräte.

Im Allgemeinen sollten Sie diesen Befehl nicht direkt verwenden. Um den Wert für einen Hardwarecodec zu erhalten, müssen Sie die Funktion [**mfgetmftmerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) aufrufen. Diese Funktion führt alle OPM-Aufrufe aus, die erforderlich sind, um den **OPM \_ get \_ Codec \_ Info** -Befehl zu senden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OPM-Status Anforderungen](opm-status-requests.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




