---
description: Die cmediaevent-Klasse stellt die Basisklassen Implementierung der IDispatch-Methoden der Dual-Interface imediaevent bereit. Die Eigenschaften und Methoden der imediaevent-Schnittstelle werden als rein virtuell angezeigt.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: Cmediaevent-Klasse
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
ms.openlocfilehash: 927e561fa557ac33b1669ca7353377f7814ca448
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104219024"
---
# <a name="cmediaevent-class"></a>Cmediaevent-Klasse

![cmediaevent-Klassenhierarchie](images/cutil03.png)

Die- `CMediaEvent` Klasse stellt die Basisklassen Implementierung der **IDispatch** -Methoden der Dual-Interface [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent)bereit. Die Eigenschaften und Methoden der **imediaevent** -Schnittstelle werden als rein virtuell angezeigt.

Die- `CMediaEvent` Klasse stellt auch die Basisklassen Implementierung der [**imediaeventex**](/windows/desktop/api/Control/nn-control-imediaeventex) -Schnittstelle bereit, die von [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent)abgeleitet ist.

[**Cmediaevent:: GetIDsOfNames**](cmediaevent-getidsofnames.md), [**cmediaevent:: GetTypeInfo**](cmediaevent-gettypeinfo.md), [**cmediaevent:: GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)und [**cmediaevent:: Aufrufen**](cmediaevent-invoke.md) Member-Funktionen sind Standard Implementierungen der **IDispatch** -Schnittstelle mithilfe der [**cbasedispatch**](cbasedispatch.md) -Klasse (und einer Typbibliothek), um die Befehle zu analysieren und an die reinen virtuellen Methoden der [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) -Schnittstelle zu übergeben.



| Elementfunktionen                                         | BESCHREIBUNG                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cmediaevent**](cmediaevent-cmediaevent.md)           | Erstellt ein **cmediaevent** -Objekt.                                                                                                                                                          |
| IDispatch-Methoden                                        | BESCHREIBUNG                                                                                                                                                                                   |
| [**GetIDsOfNames**](cmediaevent-getidsofnames.md)       | Ordnet einen einzelnen Member und einen optionalen Satz von Parametern einem entsprechenden Satz von ganzzahligen Dispatchbezeichnern zu, der bei nachfolgenden Aufrufen der **IDispatch:: Aufrufen** -Methode verwendet werden kann. |
| [**GetTypeInfo**](cmediaevent-gettypeinfo.md)           | Ruft ein Type-Information-Objekt ab, das die Typinformationen für eine Schnittstelle abruft.                                                                                                   |
| [**Gettypeingefocount**](cmediaevent-gettypeinfocount.md) | Ruft die Anzahl der von einem-Objekt bereitgestellten Typ-Informations Schnittstellen ab.                                                                                                                    |
| [**Invoke**](cmediaevent-invoke.md)                     | Stellt den Zugriff auf von einem Objekt verfügbar gemachte Eigenschaften und Methoden bereit.                                                                                                                               |



 

 

 



