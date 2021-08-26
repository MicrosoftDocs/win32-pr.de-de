---
description: Das folgende Material enthält Details zu den Basisklassen des Media Service-Anbieters.
ms.assetid: ef845c44-1ff5-42a1-8e91-38d66e6fe363
title: TAPI 3 MSP-Basisklassenreferenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1c0b2f19f372e60972c66d965f689ec79f930f343080be21471fbc4ba59f67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905740"
---
# <a name="tapi-3-msp-base-classes-reference"></a>TAPI 3 MSP-Basisklassenreferenz

Das folgende Material enthält Details zu den Basisklassen des Media Service-Anbieters.



| Basisklassen des Mediendienstanbieters (alphabetische Reihenfolge) | BESCHREIBUNG                                                                                                                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CAudioCaptureTerminal](caudiocaptureterminal.md)       | Abgeleitet von [CSingleFilterTerminal](csinglefilterterminal.md) und implementiert ein statisches Audioaufnahmeterminal für Wellengeräte mithilfe des DirectShow-Waveinfilters. Definiert in MSPtmac.h.               |
| [CAudioRenderTerminal](caudiorenderterminal.md)         | Abgeleitet von [CSingleFilterTerminal und](csinglefilterterminal.md) implementiert ein statisches Audiorenderingterminal für Wellengeräte mithilfe des DirectShow Waveout-Filters. Definiert in MSPtrmar.h.              |
| [CBaseTerminal](cbaseterminal.md)                       | Eine Terminalbasisklasse, die sowohl für statische als auch für dynamische Terminals gilt. Sie ist vollständig generisch, sodass jede Terminalimplementierung direkt oder indirekt von dieser Klasse ableiten kann. Definiert in MSPterm.h |
| [**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)                       | Implementiert das MSP-Adressobjekt und unterstützt die [**ITMSPAddress-Schnittstelle.**](/windows/desktop/api/msp/nn-msp-itmspaddress) Definiert in MSPaddr.h.                                                                                |
| [CMSPArray](cmsparray.md)                               | Eine Vorlage, die ein intelligentes Array implementiert, das bei Bedarf wächst. Definiert in MSPutils.h.                                                                                                               |
| [**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)                     | Stellt eine generische Implementierung des Aufrufobjekts bereit und unterstützt die [**ITStreamControl-Schnittstelle.**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) Definiert in MSPcall.h.                                                       |
| [**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)         | Definiert einen Aufruf, der ein Filterdiagramm für jeden Stream verwendet. Definiert in MSPcall.h.                                                                                                                          |
| [**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)                         | Macht Methoden verfügbar, die es einer Anwendung ermöglichen, einen Unterstream zu starten, anzuhalten oder zu beenden und Terminals auszuwählen oder die Auswahl aufzuheben. Definiert in MSPstrm.h.                                                              |
| [CMSPThread](cmspthread.md)                             | Implementiert den Arbeitsthread des MSP. Definiert in MSPthrd.h.                                                                                                                                               |
| [CSingleFilterTerminal](csinglefilterterminal.md)       | Eine zusätzliche Terminalbasisklasse, die sowohl für statische als auch für dynamische Terminals gilt. Macht die Implementierung spezifischer, indem angenommen wird, dass das Terminal über einen einzelnen DirectShow-Filter verfügt. Definiert in MSPterm.h.    |
| [CVideoCaptureTerminal](cvideocaptureterminal.md)       | Wird von [CSingleFilterTerminal](csinglefilterterminal.md) abgeleitet und implementiert ein statisches Videoaufnahmeterminal mit einem einzelnen DirectShow-Filter. Definiert in MSPtmvc.h.                                  |



 

 

 
