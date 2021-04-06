---
title: Vorgangs-Plug-in-Methoden
description: Vorgangs-Plug-in-Methoden
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff64a53c4c63b9e552efe90ac057b8a31d603b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947292"
---
# <a name="operations-plug-in-methods"></a>Vorgangs-Plug-in-Methoden

Alle Vorgänge Plug-in-Einstiegspunkte verfügen über einen Rückrufmechanismus, um den Erfolg oder Misserfolg des Aufrufs zu melden. Einige Rückruf Mechanismen werden mehrmals aufgerufen, bis alle Ergebnisse gemeldet werden.

In der folgenden Tabelle finden Sie eine Übersicht über die Vorgangs Rückruf Methoden.



| Methode                                                                         | BESCHREIBUNG                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wsmanpluginfreerequestdetails**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | Gibt Arbeitsspeicher frei, der der [**WSMAN-Plug-in- \_ \_ Anforderungs**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) Struktur zugeordnet ist.                                          |
| [**Wsmanplugingetoperationparameters**](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | Ruft Betriebsinformationen ab, z. b. Timeouts und Daten Einschränkungen, die einem Vorgang zugeordnet sind.                                         |
| [**Wsmanpluginoperationcomplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | Zeichnet den Abschluss eines Vorgangs auf.                                                                                                              |
| [**Wsmanpluginreceiveresult**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | Meldet Ergebnisse an Windows-Remoteverwaltung (WinRM)-Plug-ins.                                                                                       |
| [**Wsmanpluginreportcontext**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | Meldet die Shell und den Befehls Kontext zurück zur WinRM-Infrastruktur, sodass weitere Vorgänge für die Shell und/oder den Befehl ausgeführt werden können. |



 

 

 




