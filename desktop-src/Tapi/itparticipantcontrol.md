---
description: Die ITParticipantControl-Schnittstelle wird vom IPConf-MSP implementiert.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: ITParticipantControl-Schnittstelle (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e111a298069901a67d8b0ecbff365e0ab03f1885a247d41425afe7eb31085d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774750"
---
# <a name="itparticipantcontrol-interface"></a>ITParticipantControl-Schnittstelle

\[**ITParticipantControl** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **ITParticipantControl-Schnittstelle** wird vom IPConf-MSP implementiert. Diese Schnittstelle wird für das Aufrufobjekt verfügbar gemacht. Mit dieser Schnittstelle kann eine Anwendung Zeiger auf die Teilnehmer einer Konferenz abrufen. Die **ITParticipantControl-Schnittstelle** wird erstellt, indem **QueryInterface** auf [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)aufgerufen wird.

## <a name="members"></a>Member

Die **ITParticipantControl-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITParticipantControl** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ITParticipantControl-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                      | Beschreibung                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) | Listet die Teilnehmer auf, die derzeit an der Konferenz beteiligt sind.<br/>                                                                                                    |
| [**Get \_ Participants (Teilnehmer abrufen)**](itparticipantcontrol-get-participants.md)          | Erstellt eine Auflistung von Teilnehmern, die der aktuellen Konferenz zugeordnet sind. Wird für Automation-Clientanwendungen bereitgestellt, z. B. in Visual Basic geschriebene Anwendungen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

