---
description: Die cmediacontrol-Klasse stellt die Basisklassen Behandlung der IDispatch-Methoden der Dual-Interface IMediaControl bereit. Die Eigenschaften und Methoden der IMediaControl-Schnittstelle werden als rein virtuell angezeigt.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: Cmediacontrol-Klasse
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
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869595"
---
# <a name="cmediacontrol-class"></a>Cmediacontrol-Klasse

![cmediacontrol-Klassenhierarchie](images/cutil02.png)

Die- `CMediaControl` Klasse stellt die Basisklassen Behandlung der [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) -Methoden der Dual-Interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)bereit. Die Eigenschaften und Methoden der **IMediaControl** -Schnittstelle werden als rein virtuell angezeigt.

In der Regel ist der Filter Graph-Manager das einzige Objekt, das die [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) -Schnittstelle implementiert. (Filter implementieren die [**imediafilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) -Schnittstelle, die von [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)geerbt wurde, um Steuerungsbefehle vom Filter Graph-Manager zu empfangen.) Daher ist diese Klassenbibliothek nur für das Filtern von Entwicklern eingeschränkt.

[**Cmediacontrol:: GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**cmediacontrol:: die Funktionen "GetTypeInfo**](cmediacontrol-gettypeinfo.md)", " [**cmediacontrol:: GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)" und " [**cmediacontrol:: Aufrufen**](cmediacontrol-invoke.md) " sind Standard Implementierungen der [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) -Methoden mithilfe der [**cbasedispatch**](cbasedispatch.md) -Klasse (und einer Typbibliothek) zum Analysieren der Befehle und zum übergeben an die reinen virtuellen Methoden der Schnittstelle " [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) "

Die in Control. ODL definierten [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) -Methoden werden als rein virtuell belassen.



| Elementfunktionen                                           | BESCHREIBUNG                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cmediacontrol**](cmediacontrol-cmediacontrol.md)       | Erstellt ein **cmediacontrol** -Objekt.                                                                                                                                                                                                  |
| IDispatch-Methoden                                          | BESCHREIBUNG                                                                                                                                                                                                                             |
| [**GetIDsOfNames**](cmediacontrol-getidsofnames.md)       | Ordnet einen einzelnen Member und einen optionalen Satz von Parametern einem entsprechenden Satz von ganzzahligen Dispatchbezeichnern (DispIds) zu, der bei nachfolgenden Aufrufen der [**cmediacontrol:: Aufrufen**](cmediacontrol-invoke.md) -Methode verwendet werden kann. |
| [**GetTypeInfo**](cmediacontrol-gettypeinfo.md)           | Ruft ein Type-Information-Objekt ab, das die Typinformationen für eine Schnittstelle abrufen kann.                                                                                                                                          |
| [**Gettypeingefocount**](cmediacontrol-gettypeinfocount.md) | Ruft die Anzahl der von einem-Objekt bereitgestellten Typ-Informations Schnittstellen ab.                                                                                                                                                              |
| [**Invoke**](cmediacontrol-invoke.md)                     | Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.                                                                                                                                                                         |



 

 

 
