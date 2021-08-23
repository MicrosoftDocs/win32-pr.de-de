---
description: Die CMediaEvent-Klasse stellt die Basisklassenimplementierungen der IDispatch-Methoden des Dual-Interface-IMediaEvent bereit. Die Eigenschaften und Methoden der IMediaEvent-Schnittstelle bleiben rein virtuell.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: CMediaEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 505a11b9a8d3c12586e25faa822b127e0b8bb636f6655eb617125a47fb84feaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832484"
---
# <a name="cmediaevent-class"></a>CMediaEvent-Klasse

![cmediaevent-Klassenhierarchie](images/cutil03.png)

Die `CMediaEvent` -Klasse stellt die Basisklassenimplementierungen der **IDispatch-Methoden** des [**Dual-Interface-IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)bereit. Die Eigenschaften und Methoden der **IMediaEvent-Schnittstelle** bleiben rein virtuell.

Die `CMediaEvent` -Klasse stellt auch die Basisklassenimplementierungen der [**IMediaEventEx-Schnittstelle**](/windows/desktop/api/Control/nn-control-imediaeventex) bereit, die von [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)abgeleitet wird.

Die [**Memberfunktionen CMediaEvent::GetIDsOfNames,**](cmediaevent-getidsofnames.md) [**CMediaEvent::GetTypeInfo,**](cmediaevent-gettypeinfo.md) [**CMediaEvent::GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)und [**CMediaEvent::Invoke**](cmediaevent-invoke.md) sind Standardimplementierungen der **IDispatch-Schnittstelle,** die die [**CBaseDispatch-Klasse**](cbasedispatch.md) (und eine Typbibliothek) verwenden, um die Befehle zu analysieren und an die reinen virtuellen Methoden der [**IMediaEvent-Schnittstelle**](/windows/desktop/api/Control/nn-control-imediaevent) zu übergeben.



| Elementfunktionen                                         | Beschreibung                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaEvent**](cmediaevent-cmediaevent.md)           | Erstellt ein **CMediaEvent-Objekt.**                                                                                                                                                          |
| IDispatch-Methoden                                        | Beschreibung                                                                                                                                                                                   |
| [**GetIDsOfNames**](cmediaevent-getidsofnames.md)       | Karten einen einzelnen Member und einen optionalen Satz von Parametern zu einem entsprechenden Satz von ganzzahligen Dispatchbezeichnern, die bei nachfolgenden Aufrufen der **IDispatch::Invoke-Methode** verwendet werden können. |
| [**GetTypeInfo**](cmediaevent-gettypeinfo.md)           | Ruft ein Typinformationsobjekt ab, das die Typinformationen für eine Schnittstelle abruft.                                                                                                   |
| [**GetTypeInfoCount**](cmediaevent-gettypeinfocount.md) | Ruft die Anzahl der Typinformationsschnittstellen ab, die von einem -Objekt bereitgestellt werden.                                                                                                                    |
| [**Invoke**](cmediaevent-invoke.md)                     | Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.                                                                                                                               |



 

 

 



