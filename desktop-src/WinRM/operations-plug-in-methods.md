---
title: Operations Plug-In-Methoden
description: Operations Plug-In-Methoden
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8bcfc2263a9ecd35c050499f0547b5bc5190e5896b430edabe6be8490239b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323892"
---
# <a name="operations-plug-in-methods"></a>Operations Plug-In-Methoden

Alle Plug-In-Einstiegspunkte für Vorgänge verfügen über einen Rückrufmechanismus, um den Erfolg oder Fehler des Aufrufs zu melden. Einige Rückrufmechanismen werden mehrmals aufgerufen, bis alle Ergebnisse gemeldet werden.

Die folgende Tabelle enthält eine Übersicht über die Rückrufmethoden für Vorgänge.



| Methode                                                                         | BESCHREIBUNG                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManPluginFreeRequestDetails**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | Gibt Arbeitsspeicher frei, der für die [**WSMAN-PLUG-IN-ANFORDERUNGsstruktur \_ \_ zugeordnet**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) ist.                                          |
| [**WSManPluginGetOperationParameters**](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | Ruft Betriebsinformationen ab, z. B. Time outs und Dateneinschränkungen, die einem Vorgang zugeordnet sind.                                         |
| [**WSManPluginOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | Zeichnet den Abschluss eines Vorgangs auf.                                                                                                              |
| [**WSManPluginReceiveResult**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | Meldet Ergebnisse an Windows-Plug-Ins (WinRM).                                                                                       |
| [**WSManPluginReportContext**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | Meldet die Shell und den Befehlskontext an die WinRM-Infrastruktur zurück, damit weitere Vorgänge für die Shell und/oder den Befehl ausgeführt werden können. |



 

 

 




