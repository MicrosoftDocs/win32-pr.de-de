---
description: Die ITParticipant-Schnittstelle wird vom IPConf-MSP implementiert. Es ermöglicht einer Anwendung, Informationen zu Konferenzteilnehmern abzurufen und Zeiger auf die Streams abzurufen, die diesen Teilnehmern zugeordnet sind.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: ITParticipant-Schnittstelle (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab4ff4c496616804efc1a65a728bbb658fba5bb1278939bdfb2185705684c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682650"
---
# <a name="itparticipant-interface"></a>ITParticipant-Schnittstelle

\[**ITParticipant** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITParticipant-Schnittstelle** wird vom [IPConf-MSP](ipconf-msp.md)implementiert. Es ermöglicht einer Anwendung, Informationen zu Konferenzteilnehmern abzurufen und Zeiger auf die Streams abzurufen, die diesen Teilnehmern zugeordnet sind.

Diese Schnittstelle wird für das Aufrufobjekt verfügbar gemacht, wenn ein Aufruf die IP-Konferenz verwendet. Ein Zeiger kann abgerufen werden, indem **QueryInterface** mithilfe eines [**ITCallInfo-Zeigers**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) aufgerufen wird.

## <a name="members"></a>Member

Die **ITParticipant-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITParticipant** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITParticipant-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                      | Beschreibung                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateStreams**](itparticipant-enumeratestreams.md)                  | Listet Streams auf, die dem aktuellen Teilnehmer zugeordnet sind.<br/>                                                                                                  |
| [**Get \_ MediaTypes**](itparticipant-get-mediatypes.md)                     | Ruft die einem Teilnehmer zugeordneten [**Medientypen**](tapimediatype--constants.md) ab.<br/>                                                                      |
| [**get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) | Ruft eine BSTR-Darstellung des erforderlichen Informationstyps ab, z. B. PTI \_ EMAILADDRESS.<br/>                                                                     |
| [**\_Get Status**](itparticipant-get-status.md)                             | Ruft den Status des Teilnehmers ab.<br/>                                                                                                                          |
| [**get \_ Streams**](itparticipant-get-streams.md)                           | Erstellt eine Auflistung von Streams, die dem aktuellen Teilnehmer zugeordnet sind. Wird für Automation-Clientanwendungen bereitgestellt, z. B. in Visual Basic geschriebene Anwendungen.<br/> |
| [**put \_ Status**](itparticipant-put-status.md)                             | Legt fest, ob ein dem Teilnehmer zugeordneter Stream aktiviert ist.<br/>                                                                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[IPConf-MSP-Schnittstellen](ipconf-msp-interfaces.md)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

