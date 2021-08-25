---
description: Die ITParticipantSubStreamControl-Schnittstelle wird vom IPConf MSP implementiert.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: ITParticipantSubStreamControl-Schnittstelle (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e910022d45ca9f9516adbe8aeebbdb172d66f28ab1bf8cb23219c2eee80f56cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774600"
---
# <a name="itparticipantsubstreamcontrol-interface"></a>ITParticipantSubStreamControl-Schnittstelle

\[**ITParticipantSubStreamControl** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITParticipantSubStreamControl-Schnittstelle** wird vom IPConf-MSP implementiert. Diese Schnittstelle wird für das Aufrufobjekt verfügbar gemacht. Diese Schnittstelle stellt Methoden bereit, mit denen eine Anwendung den Abgleich von Substream zu Teilnehmer entweder entdecken oder steuern kann. Die **ITParticipantSubStreamControl-Schnittstelle** wird durch Aufrufen **von QueryInterface** für [**ITCallInfo erstellt.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)

## <a name="members"></a>Member

Die **ITParticipantSubStreamControl-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITParticipantSubStreamControl** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITParticipantSubStreamControl-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                              | Beschreibung                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**get \_ ParticipantFromSubStream**](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | Ruft Teilnehmer ab, die einem angegebenen Unterstream zugeordnet sind.<br/> |
| [**get \_ SubStreamFromParticipant**](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | Ruft Einem bestimmten Teilnehmer zugeordnete Unterstreams ab.<br/> |
| [**SwitchTerminalToSubStream**](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | Legt einen Teilnehmer für einen Unterstream fest.<br/>                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

