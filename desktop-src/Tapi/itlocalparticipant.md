---
description: Die itlocalteilnehmer-Schnittstelle wird für das Stream-Objekt verfügbar gemacht, wenn der ipconf-MSP den-Befehl unterstützt.
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: Itlocalteilnehmer-Schnittstelle (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355978"
---
# <a name="itlocalparticipant-interface"></a>Itlocalteilnehmer-Schnittstelle

Die **itlocalteilnehmer** -Schnittstelle wird für das Stream-Objekt verfügbar gemacht, wenn der ipconf-MSP den-Befehl unterstützt. Der MSP implementiert Methoden, die es einer Anwendung ermöglichen, Teilnehmer Informationen zu erhalten und festzulegen. Die **itlocalteilnehmer** -Schnittstelle wird durch Aufrufen von **QueryInterface** in [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)erstellt.

## <a name="members"></a>Member

Die **itlocalteilnehmer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itlocalparticipants** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itlocalparticipants** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                     | BESCHREIBUNG                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**\_localparticipanttypdinfo erhalten**](itlocalparticipant-get-localparticipanttypedinfo.md) | Ruft Teilnehmer Informationen ab, z. b. e-Mail-Name oder geografischer Standort<br/> |
| [**\_localparticipanttypeer dinfo platzieren**](itlocalparticipant-put-localparticipanttypedinfo.md) | Legt Teilnehmer Informationen fest.<br/>                                               |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

