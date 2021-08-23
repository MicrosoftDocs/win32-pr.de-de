---
description: Die CMediaControl-Klasse stellt die Basisklassenbehandlung der IDispatch-Methoden des Dual-Interface-IMediaControl bereit. Die Eigenschaften und Methoden der IMediaControl-Schnittstelle bleiben rein virtuell.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: CMediaControl-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: 119ffb93cb307db1da3bc8c7562851d63c5f9eeb8e0e3b80be62c8110181c32b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074078"
---
# <a name="cmediacontrol-class"></a>CMediaControl-Klasse

![cmediacontrol-Klassenhierarchie](images/cutil02.png)

Die `CMediaControl` -Klasse stellt die Basisklassenbehandlung der [**IDispatch-Methoden**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) von [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)mit dualer Schnittstelle bereit. Die Eigenschaften und Methoden der **IMediaControl-Schnittstelle** bleiben rein virtuell.

In der Regel ist der Filtergraph-Manager das einzige Objekt, das die [**IMediaControl-Schnittstelle**](/windows/desktop/api/Control/nn-control-imediacontrol) implementiert. (Filter implementieren die von [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)geerbte [**IMediaFilter-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) um Steuerungsbefehle vom Filtergraph-Manager zu empfangen.) Daher ist diese Klassenbibliothek nur von begrenztem Nutzen zum Filtern von Entwicklern.

Die [**Memberfunktionen CMediaControl::GetIDsOfNames,**](cmediacontrol-getidsofnames.md) [**CMediaControl::GetTypeInfo,**](cmediacontrol-gettypeinfo.md) [**CMediaControl::GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)und [**CMediaControl::Invoke**](cmediacontrol-invoke.md) sind Standardimplementierungen der [**IDispatch-Methoden,**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) die die [**CBaseDispatch-Klasse**](cbasedispatch.md) (und eine Typbibliothek) verwenden, um die Befehle zu analysieren und an die reinen virtuellen Methoden der [**IMediaControl-Schnittstelle**](/windows/desktop/api/Control/nn-control-imediacontrol) zu übergeben.

Die in control.odl definierten [**IMediaControl-Methoden**](/windows/desktop/api/Control/nn-control-imediacontrol) bleiben rein virtuell.



| Elementfunktionen                                           | Beschreibung                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CMediaControl**](cmediacontrol-cmediacontrol.md)       | Erstellt ein **CMediaControl-Objekt.**                                                                                                                                                                                                  |
| IDispatch-Methoden                                          | Beschreibung                                                                                                                                                                                                                             |
| [**GetIDsOfNames**](cmediacontrol-getidsofnames.md)       | Karten einen einzelnen Member und einen optionalen Satz von Parametern zu einem entsprechenden Satz von ganzzahligen Dispatchbezeichnern (DISPIDs), die bei nachfolgenden Aufrufen der [**CMediaControl::Invoke-Methode**](cmediacontrol-invoke.md) verwendet werden können. |
| [**GetTypeInfo**](cmediacontrol-gettypeinfo.md)           | Ruft ein Typinformationsobjekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.                                                                                                                                          |
| [**GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md) | Ruft die Anzahl der Typinformationsschnittstellen ab, die von einem -Objekt bereitgestellt werden.                                                                                                                                                              |
| [**Invoke**](cmediacontrol-invoke.md)                     | Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.                                                                                                                                                                         |



 

 

 
