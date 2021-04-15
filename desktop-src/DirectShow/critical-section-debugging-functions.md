---
description: Kritische Abschnitts Debuggingfunktionen
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Kritische Abschnitts Debuggingfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520992"
---
# <a name="critical-section-debugging-functions"></a>Kritische Abschnitts Debuggingfunktionen

Diese Funktionen helfen Ihnen, kritische Abschnitte in Ihrem Code zu debuggen, was die Auffinden der Ursache eines Deadlocks vereinfachen kann. Diese Funktionen verwenden die [**ccritsec**](ccritsec.md) -Hilfsklasse.



| Funktion                             | BESCHREIBUNG                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [**Critcheckin**](critcheckin.md)   | Gibt " **true** " zurück, wenn der aktuelle Thread den angegebenen kritischen Abschnitt besitzt.  |
| [**Critcheckout**](critcheckout.md) | Gibt **false** zurück, wenn der aktuelle Thread den angegebenen kritischen Abschnitt besitzt. |
| [**Dbglocktrace**](dbglocktrace.md) | Aktiviert oder deaktiviert die Debugprotokollierung für einen bestimmten kritischen Abschnitt.              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debugging-Hilfsprogramme](debugging-utilities.md)
</dt> </dl>

 

 



