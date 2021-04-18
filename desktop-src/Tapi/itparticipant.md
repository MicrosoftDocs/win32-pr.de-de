---
description: Die itteilnehmer-Schnittstelle wird von ipconf MSP implementiert. Sie ermöglicht einer Anwendung das Abrufen von Informationen zu Konferenzteilnehmern und das Abrufen von Zeigern auf die Streams, die diesen Teilnehmern zugeordnet sind.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Itteilnehmer-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371676"
---
# <a name="itparticipant-interface"></a>Itteilnehmer-Schnittstelle

\[Der **itteilnehmer** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itteilnehmer** -Schnittstelle wird von [ipconf MSP](ipconf-msp.md)implementiert. Sie ermöglicht einer Anwendung das Abrufen von Informationen zu Konferenzteilnehmern und das Abrufen von Zeigern auf die Streams, die diesen Teilnehmern zugeordnet sind.

Diese Schnittstelle wird für das-Objekt aufgerufen, wenn ein-Rückruf die IP-Konferenzen verwendet. Ein Zeiger kann durch Aufrufen von **QueryInterface** mithilfe eines [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) -Zeigers abgerufen werden.

## <a name="members"></a>Member

Die **itteilnehmer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. Der **itparticipants** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itparticipants** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                      | BESCHREIBUNG                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Enumeratestreams**](itparticipant-enumeratestreams.md)                  | Listet Streams auf, die dem aktuellen Teilnehmer zugeordnet sind.<br/>                                                                                                  |
| [**\_mediatypes erhalten**](itparticipant-get-mediatypes.md)                     | Ruft die einem Teilnehmer zugeordneten [**Medientypen**](tapimediatype--constants.md) ab.<br/>                                                                      |
| [**Informationen zu " \_ participanttypeer" erhalten**](itparticipant-get-participanttypedinfo.md) | Ruft eine BSTR-Darstellung des benötigten Informations Typs, z. b. PTI \_ EmailAddress, ab.<br/>                                                                     |
| [**\_Status erhalten**](itparticipant-get-status.md)                             | Ruft den Status des Teilnehmers ab.<br/>                                                                                                                          |
| [**Daten \_ Ströme erhalten**](itparticipant-get-streams.md)                           | Erstellt eine Auflistung von Streams, die dem aktuellen Teilnehmer zugeordnet sind. Wird für Automatisierungs Client Anwendungen bereitgestellt, wie z. b. die in Visual Basic geschriebenen.<br/> |
| [**Put- \_ Status**](itparticipant-put-status.md)                             | Legt fest, ob ein dem Teilnehmer zugeordneter Stream aktiviert ist.<br/>                                                                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ipconf-msp](ipconf-msp.md)
</dt> <dt>

[Ipconf-MSP-Schnittstellen](ipconf-msp-interfaces.md)
</dt> <dt>

[**Itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

