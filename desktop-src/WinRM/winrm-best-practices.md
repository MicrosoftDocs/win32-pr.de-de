---
title: Bewährte Methoden für WinRM
description: In diesem Thema werden einige der bewährten Methoden für die Verwendung der verschiedenen Funktionen der WinRM-API erläutert.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc780ec299c3249006085d348d983f8dab5b76a462c991a2d3665fed7d18f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733800"
---
# <a name="winrm-best-practices"></a>Bewährte Methoden für WinRM

In diesem Thema werden einige der bewährten Methoden für die Verwendung der verschiedenen Funktionen der WinRM-API erläutert.

## <a name="quotas"></a>Kontingente

Wenn ein Kontingent erreicht wird, gibt der WinRM-Dienst einen Fehler an den Client zurück. Daher muss die Clientlogik den Vorgang basierend auf dem zurückgegebenen Fehler explizit wiederholen.

## <a name="event-subscriptions"></a>Ereignisabonnements

Wenn Sie vom Collector initiierte Abonnements verwenden, beschränken Sie die Anzahl von Remotecomputern auf 500, und isolieren Sie den [Windows Event Collector-Dienst](/windows/desktop/WEC/windows-event-collector) (wecsvc) in einem separaten Hostprozess.

Ein Verbindungsfehler hält einen Thread so lange zurück, bis ein Zeitsendraum auftritt. Eine große Anzahl gleichzeitiger Verbindungsfehler kann zu einer Überschöpfung des Threadpools führen und dazu führen, dass der Server nicht mehr reagiert.

 

 