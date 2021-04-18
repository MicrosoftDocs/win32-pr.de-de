---
title: Autorisierungs-Plug-in-Methoden
description: Alle Autorisierungs-Plug-in-Einstiegspunkte verfügen über einen Rückrufmechanismus, um den Erfolg oder Misserfolg des Aufrufs zu melden. Einige Rückruf Mechanismen werden mehrmals aufgerufen, bis alle Ergebnisse gemeldet werden.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338590"
---
# <a name="authorization-plug-in-methods"></a>Autorisierungs-Plug-in-Methoden

Alle Autorisierungs-Plug-in-Einstiegspunkte verfügen über einen Rückrufmechanismus, um den Erfolg oder Misserfolg des Aufrufs zu melden. Einige Rückruf Mechanismen werden mehrmals aufgerufen, bis alle Ergebnisse gemeldet werden.

In der folgenden Tabelle finden Sie eine Übersicht über die Rückruf Methoden für die Autorisierung.



| Methode                                                                           | BESCHREIBUNG                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**Wsmanpluginauthzoperationcomplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | Meldet entweder einen erfolgreichen oder fehlgeschlagenen Benutzer Vorgang.                |
| [**Wsmanpluginauthzqueryquotacomplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | Meldet Kontingent Details, die für den angegebenen Benutzer relevant sind.      |
| [**Wsmanpluginauthzusercomplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | Meldet entweder eine erfolgreiche oder fehlgeschlagene Autorisierung der Benutzer Verbindung. |



 

 

 




