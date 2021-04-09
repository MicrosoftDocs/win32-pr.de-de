---
title: Bewährte Methoden für WinRM
description: In diesem Thema werden einige bewährte Methoden für die Verwendung der verschiedenen Features der WinRM-API erläutert.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948793"
---
# <a name="winrm-best-practices"></a>Bewährte Methoden für WinRM

In diesem Thema werden einige bewährte Methoden für die Verwendung der verschiedenen Features der WinRM-API erläutert.

## <a name="quotas"></a>Kontingente

Wenn ein Kontingent getroffen wird, gibt der WinRM-Dienst einen Fehler an den Client zurück. Folglich muss die Client Logik den Vorgang auf der Grundlage des zurückgegebenen Fehlers explizit wiederholen.

## <a name="event-subscriptions"></a>Ereignisabonnements

Wenn Sie vom Collector initiierte Abonnements verwenden, begrenzen Sie die Anzahl der Remote Computer auf 500, und isolieren Sie den [Windows-Ereignis](/windows/desktop/WEC/windows-event-collector) Sammlungs Dienst (Wecsvc) in einem separaten Host Prozess.

Ein Verbindungsfehler enthält einen Thread, bis ein Timeout eintritt. Eine große Anzahl von gleichzeitigen Verbindungsfehlern kann die Auslastung des Thread Pools verursachen und den Server als nicht reagierend Renten.

 

 