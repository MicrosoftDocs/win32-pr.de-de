---
description: Ruft den Wert eines Hardwarecodecs ab.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ffa9a962d9ed04b6a978da1534a6da4fa506e873d89d238bcbb2aa00fd865
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847980"
---
# <a name="opm_get_codec_info"></a>OPM \_ GET \_ CODEC \_ INFO

Ruft den Wert eines Hardwarecodecs ab.



| Anforderung | Wert |
|--------------|-------------------------------------------------------------------------------------------|
| Anforderungs-GUID | **OPM \_ GET \_ CODEC \_ INFO**                                                                 |
| Eingabedaten   | Eine [**OPM \_ GET CODEC \_ INFO \_ \_ PARAMETERS-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)   |
| Daten zurückgeben  | EINE [**OPM \_ GET CODEC \_ INFO \_ \_ INFORMATION-Struktur**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) |



 

## <a name="remarks"></a>Hinweise

Dieser Befehl verwendet zwar die [OPM-Schnittstelle (Output Protection Manager),](output-protection-manager.md) gilt jedoch nur für Hardwareencoder und Decoder. Dies gilt nicht für Videoausgabegeräte.

Im Allgemeinen sollten Sie diesen Befehl nicht direkt verwenden. Rufen Sie die [**MFGetMFTMerit-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) auf, um den Wert für einen Hardwarecodec abzurufen. Diese Funktion führt alle OPM-Aufrufe aus, die zum Senden des **BEFEHLs OPM \_ GET CODEC \_ \_ INFO** erforderlich sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[OPM-Statusanforderungen](opm-status-requests.md)
</dt> <dt>

[Ausgabeschutz-Manager](output-protection-manager.md)
</dt> <dt>

[**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




