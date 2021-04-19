---
description: Die itparticipantcontrol-Schnittstelle wird von ipconf MSP implementiert.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: Itparticipantcontrol-Schnittstelle (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373788"
---
# <a name="itparticipantcontrol-interface"></a>Itparticipantcontrol-Schnittstelle

\[**Itparticipantcontrol** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itparticipantcontrol** -Schnittstelle wird von ipconf MSP implementiert. Diese Schnittstelle wird für das-Objekt aufgerufen. Diese Schnittstelle ermöglicht es einer Anwendung, Zeiger auf die Teilnehmer einer Konferenz abzurufen. Die **itparticipantcontrol** -Schnittstelle wird durch Aufrufen von **QueryInterface** für [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)erstellt.

## <a name="members"></a>Member

Die **itparticipantcontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Itparticipantcontrol** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itparticipantcontrol** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                      | BESCHREIBUNG                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Enumerateparticipants**](itparticipantcontrol-enumerateparticipants.md) | Listet die Teilnehmer auf, die derzeit an der Konferenz beteiligt sind.<br/>                                                                                                    |
| [**\_Teilnehmer erhalten**](itparticipantcontrol-get-participants.md)          | Erstellt eine Auflistung von Teilnehmern, die der aktuellen Konferenz zugeordnet sind. Wird für Automatisierungs Client Anwendungen bereitgestellt, wie z. b. die in Visual Basic geschriebenen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

