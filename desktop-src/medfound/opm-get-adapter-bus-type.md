---
description: Gibt den Typ des e/a-Busses zurück, der von der Videoausgabe verwendet wird.
ms.assetid: 1aff4c81-ffa0-4116-b7ea-60b1b83042df
title: OPM_GET_ADAPTER_BUS_TYPE (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde3611eb00977670c59c4326f793c1cb9037fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347272"
---
# <a name="opm_get_adapter_bus_type"></a>OPM \_ get \_ Adapter \_ \_ Bustyp

Gibt den Typ des e/a-Busses zurück, der von der Videoausgabe verwendet wird.



| Anforderung | Wert |
|--------------|-----------------------------------------------------------------------------|
| Anforderungs-GUID | OPM \_ get \_ Adapter \_ \_ Bustyp                                                |
| Eingabedaten   | Keine                                                                        |
| Daten zurückgeben  | Eine [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur |



 

## <a name="remarks"></a>Bemerkungen

Der Bustyp wird im **ulinformation** -Member der [**OPM- \_ Standard \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Struktur zurückgegeben. Der Wert ist ein bitweises **or** von [**OPM-bustyps**](opm-bus-type-flags.md).

Diese Abfrage entspricht der DXVA- \_ Abfrage "coppquerybusdata", die im Certified Output Protection Protocol (COPP) verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[OPM-Status Anforderungen](opm-status-requests.md)
</dt> </dl>

 

 




