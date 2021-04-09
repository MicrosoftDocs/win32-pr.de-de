---
description: Übersicht über die Fehlerbehandlung bei Verwendung der StylusInput-APIs (Application Programming Interfaces).
ms.assetid: 7d7ff5b2-3eda-4570-96fe-b3b8f41ff69b
title: Überlegungen zur Fehlerbehandlung für die StylusInput-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fa582a8dbf531588f6d3d0c142c4ec7b40a058
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958980"
---
# <a name="error-handling-considerations-for-the-stylusinput-api"></a>Überlegungen zur Fehlerbehandlung für die StylusInput-API

Nicht behandelte Ausnahmen, die von einem Plug-in ausgelöst werden, werden durch das [**RealTimeStylus**](realtimestylus-class.md) -Objekt abgefangen. Wenn ein Plug-in eine Ausnahme auslöst, wird der normale Datenfluss unterbrochen. Das **RealTimeStylus** -Objekt:

1.  Erstellt ein [ErrorData](/previous-versions/ms575221(v=vs.100)) -Objekt (in verwaltetem Code).
2.  Ruft die [**Fehler**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) Methode (in verwaltetem Code, entweder die [Microsoft. StylusInput. IStylusSyncPlugin. Error](/previous-versions/ms824754(v=msdn.10)) -oder [Microsoft. StylusInput. IStylusAsyncPlugin. Error](/previous-versions/ms824771(v=msdn.10)) -Methode) des Plug-Ins auf, das die Ausnahme ausgelöst hat.
3.  Ruft die [**Fehler**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) Methode der restlichen Plug-ins in dieser Auflistung auf.
4.  Wenn das Plug-in, das die Ausnahme ausgelöst hat, ein synchrones Plug-in ist, wird das [ErrorData](/previous-versions/ms575221(v=vs.100)) -Objekt (in verwaltetem Code) der Ausgabe Warteschlange hinzugefügt.
5.  Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt nimmt die normale Verarbeitung der ursprünglichen Daten wieder auf.

Wenn ein Plug-in eine Ausnahme von der [**Fehler**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-error) Methode auslöst, fängt das [**RealTimeStylus**](realtimestylus-class.md) -Objekt die Ausnahme ab, generiert jedoch kein neues [ErrorData](/previous-versions/ms575221(v=vs.100)) -Objekt. Weitere Informationen zum Hinzufügen von ErrorData zur Warteschlange finden Sie unter [Plug-in-Daten und die RealTimeStylus-Klasse](plug-in-data-and-the-realtimestylus-class.md).

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt beendet die Verarbeitung von Daten aus dem Datenstrom des Tablettstifts nicht, wenn eines der Plug-ins eine Ausnahme auslöst. Abhängig vom Entwurf müssen einige der Plug-ins möglicherweise die [ErrorData](/previous-versions/ms575221(v=vs.100)) -Benachrichtigung abonnieren und ihr Verhalten ändern, wenn eine Ausnahme auftritt.

 

 
