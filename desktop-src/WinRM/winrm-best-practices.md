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
# <a name="winrm-best-practices"></a><span data-ttu-id="a999f-103">Bewährte Methoden für WinRM</span><span class="sxs-lookup"><span data-stu-id="a999f-103">WinRM Best Practices</span></span>

<span data-ttu-id="a999f-104">In diesem Thema werden einige bewährte Methoden für die Verwendung der verschiedenen Features der WinRM-API erläutert.</span><span class="sxs-lookup"><span data-stu-id="a999f-104">This topic explains some of the best practices for using the various features of the WinRM API.</span></span>

## <a name="quotas"></a><span data-ttu-id="a999f-105">Kontingente</span><span class="sxs-lookup"><span data-stu-id="a999f-105">Quotas</span></span>

<span data-ttu-id="a999f-106">Wenn ein Kontingent getroffen wird, gibt der WinRM-Dienst einen Fehler an den Client zurück.</span><span class="sxs-lookup"><span data-stu-id="a999f-106">When a quota is hit, the WinRM service returns an error to the client.</span></span> <span data-ttu-id="a999f-107">Folglich muss die Client Logik den Vorgang auf der Grundlage des zurückgegebenen Fehlers explizit wiederholen.</span><span class="sxs-lookup"><span data-stu-id="a999f-107">As a result, the client logic must explicitly retry the operation based on the returned error.</span></span>

## <a name="event-subscriptions"></a><span data-ttu-id="a999f-108">Ereignisabonnements</span><span class="sxs-lookup"><span data-stu-id="a999f-108">Event subscriptions</span></span>

<span data-ttu-id="a999f-109">Wenn Sie vom Collector initiierte Abonnements verwenden, begrenzen Sie die Anzahl der Remote Computer auf 500, und isolieren Sie den [Windows-Ereignis](/windows/desktop/WEC/windows-event-collector) Sammlungs Dienst (Wecsvc) in einem separaten Host Prozess.</span><span class="sxs-lookup"><span data-stu-id="a999f-109">When using Collector-initiated subscriptions, limit the number of remote computers to 500 and isolate the [Windows Event Collector](/windows/desktop/WEC/windows-event-collector) service (wecsvc) in a separate host process.</span></span>

<span data-ttu-id="a999f-110">Ein Verbindungsfehler enthält einen Thread, bis ein Timeout eintritt. Eine große Anzahl von gleichzeitigen Verbindungsfehlern kann die Auslastung des Thread Pools verursachen und den Server als nicht reagierend Renten.</span><span class="sxs-lookup"><span data-stu-id="a999f-110">A connection error will hold a thread until it times out. A large number of simultaneous connection errors can cause thread pool exhaustion and render the server unresponsive.</span></span>

 

 