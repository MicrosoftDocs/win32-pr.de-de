---
description: Im folgenden Material finden Sie Informationen zu den Basisklassen für den Media Services-Anbieter.
ms.assetid: ef845c44-1ff5-42a1-8e91-38d66e6fe363
title: Referenz zu TAPI 3-MSP-Basisklassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4cca24b69a645b18cc0950288e0de983b54355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215987"
---
# <a name="tapi-3-msp-base-classes-reference"></a>Referenz zu TAPI 3-MSP-Basisklassen

Im folgenden Material finden Sie Informationen zu den Basisklassen für den Media Services-Anbieter.



| Basisklassen für den Media Service-Anbieter (alphabetische Reihenfolge) | BESCHREIBUNG                                                                                                                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Caudiocaptureterminal](caudiocaptureterminal.md)       | Wird von [csinglefilterterminal](csinglefilterterminal.md) abgeleitet und implementiert ein statisches audioerfassungs-Terminal für Wave-Geräte mithilfe des DirectShow WaveIn-Filters. Definiert in "msptmac. h".               |
| [Caudiorenderterminal](caudiorenderterminal.md)         | Wird von [csinglefilterterminal](csinglefilterterminal.md) abgeleitet und implementiert ein statisches audiorendering-Terminal für Wave-Geräte, das den DirectShow-waveout-Filter verwendet. Definiert in "msptrmar. h".              |
| [Cbaseterminal](cbaseterminal.md)                       | Eine Terminal Basisklasse, die sowohl auf statische als auch dynamische Terminals anwendbar ist. Es ist vollständig generisch, sodass jede Terminal Implementierung direkt oder indirekt von dieser Klasse abgeleitet werden kann. Definiert in "mspterm. h" |
| [**Cmspaddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)                       | Implementiert das MSP-Adress Objekt und unterstützt die [**itmspaddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) -Schnittstelle. Definiert in "mspaddr. h".                                                                                |
| [Cmsparray](cmsparray.md)                               | Eine Vorlage, die ein intelligentes Array implementiert, das bei Bedarf vergrößert wird. Definiert in "msputils. h".                                                                                                               |
| [**Cmspcallbase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)                     | Stellt eine generische Implementierung des calljektobjekts bereit und unterstützt die [**itstreamcontrol**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) -Schnittstelle. Definiert in "mspcall. h".                                                       |
| [**Cmspcallmultigraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)         | Definiert einen Aufruf, der ein Filter Diagramm für jeden Stream verwendet. Definiert in "mspcall. h".                                                                                                                          |
| [**Cmspstream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)                         | Macht Methoden verfügbar, die einer Anwendung das starten, anhalten oder Beenden eines Substreams sowie das auswählen oder Aufheben der Auswahl von Terminals ermöglichen. Definiert in "mspstraum. h".                                                              |
| [Cmspthread](cmspthread.md)                             | Implementiert den MSP-Arbeits Thread. Definiert in "mspthrd. h".                                                                                                                                               |
| [Csinglefilterterminal](csinglefilterterminal.md)       | Eine zusätzliche Terminal Basisklasse, die sowohl auf statische als auch dynamische Terminals anwendbar ist. Vereinfacht die Implementierung, indem angenommen wird, dass das Terminal über einen einzelnen DirectShow-Filter verfügt. Definiert in "mspterm. h".    |
| [Cvideocaptureterminal](cvideocaptureterminal.md)       | Wird von [csinglefilterterminal](csinglefilterterminal.md) abgeleitet und implementiert ein statisches Video Aufzeichnungs Terminal mit einem einzelnen DirectShow-Filter. Definiert in "msptmvc. h".                                  |



 

 

 
