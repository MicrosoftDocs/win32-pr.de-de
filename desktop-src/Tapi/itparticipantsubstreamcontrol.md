---
description: Die itparticipantsubstreamcontrol-Schnittstelle wird von ipconf MSP implementiert.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Itparticipantsubstreamcontrol-Schnittstelle (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799b1a85c6619e1175e620f2c5c5ef851005ba50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372765"
---
# <a name="itparticipantsubstreamcontrol-interface"></a>Itparticipantsubstreamcontrol-Schnittstelle

\[**Itparticipantsubstreamcontrol** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itparticipantsubstreamcontrol** -Schnittstelle wird von ipconf MSP implementiert. Diese Schnittstelle wird für das-Objekt aufgerufen. Diese Schnittstelle stellt Methoden bereit, die es einer Anwendung ermöglichen, die Übereinstimmung von unter Datenstrom und Teilnehmer zu ermitteln oder zu steuern. Die **itparticipantsubstreamcontrol** -Schnittstelle wird durch Aufrufen von **QueryInterface** für [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)erstellt.

## <a name="members"></a>Member

Die **itparticipantsubstreamcontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itparticipantsubstreamcontrol** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itparticipantsubstreamcontrol** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                              | BESCHREIBUNG                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**" \_ participantfromsubstream" erhalten**](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | Ruft Teilnehmer ab, die einem angegebenen teilstream zugeordnet sind.<br/> |
| [**\_substreamfromteilnehmer aufrufen**](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | Ruft die einem angegebenen Teilnehmer zugeordneten Substreams ab.<br/> |
| [**Switchterminalto substream**](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | Legt einen Teilnehmer an einem substream fest.<br/>                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itteilnehmer**](itparticipant.md)
</dt> <dt>

[**Itsubstream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

