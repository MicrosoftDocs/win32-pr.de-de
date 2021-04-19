---
description: Die erweiterten Telefoniefunktionen sind in den folgenden Tabellen nach Kategorie aufgelistet.
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: Referenz zu erweiterten Telefoniediensten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359845"
---
# <a name="extended-telephony-services-reference"></a>Referenz zu erweiterten Telefoniediensten

Die erweiterten Telefoniefunktionen sind in den folgenden Tabellen nach Kategorie aufgelistet.

## <a name="extended-telephony-functions-for-line-devices"></a>Erweiterte Telefoniefunktionen für Linien Geräte



| Funktion                                                   | BESCHREIBUNG                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**linenegotiateextversion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | Ermöglicht einer Anwendung das Aushandeln einer Erweiterungs Version, die mit dem angegebenen Zeilen Gerät verwendet werden soll. Asynchron. |
| [**linedevspecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | Bietet Dienstanbietern Zugriff auf gerätespezifische Funktionen, die nicht von anderen TAPI-Funktionen angeboten werden. Synchronous. |
| [**linedevspecificfeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | Sendet gerätespezifische Switchfeatures an den Schalter. Asynchron.                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a>Erweiterte Telefoniefunktionen für Telefongeräte



| Funktion                                                     | BESCHREIBUNG                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**phonedevspecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | Gerätespezifische escapefunktion, um Hersteller abhängige Erweiterungen zuzulassen. Asynchron.                          |
| [**Phonenegotiateextversion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Ermöglicht einer Anwendung das Aushandeln einer Erweiterungs Version, die mit dem angegebenen Telefongerät verwendet werden soll. Synchronous. |



 

 

 



