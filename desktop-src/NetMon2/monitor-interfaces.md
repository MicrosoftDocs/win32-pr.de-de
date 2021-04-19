---
description: Die folgenden COM-Schnittstellen werden verwendet, um Monitore zu entwickeln.
ms.assetid: 619991f5-1db1-400a-bf18-d4a6dd6999a8
title: Monitor Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66bb06e6153d18c7b0a4291df1c7520380a29844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347797"
---
# <a name="monitor-interfaces"></a><span data-ttu-id="019c0-103">Monitor Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="019c0-103">Monitor Interfaces</span></span>

<span data-ttu-id="019c0-104">Die folgenden COM-Schnittstellen werden verwendet, um Monitore zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="019c0-104">The following COM interfaces are used to develop monitors.</span></span>



| <span data-ttu-id="019c0-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="019c0-105">Interface</span></span>                              | <span data-ttu-id="019c0-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="019c0-106">Description</span></span>                                                                                                                                             |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="019c0-107">Imonitor</span><span class="sxs-lookup"><span data-stu-id="019c0-107">IMonitor</span></span>](imonitor.md)               | <span data-ttu-id="019c0-108">Stellt Methoden bereit, mit denen der Monitor Vorgang gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="019c0-108">Provides methods that control monitor operation.</span></span> <span data-ttu-id="019c0-109">Diese Schnittstelle muss vom Monitor implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="019c0-109">This interface must be implemented by the monitor.</span></span>                                                     |
| [<span data-ttu-id="019c0-110">Imonitoreventer Enter</span><span class="sxs-lookup"><span data-stu-id="019c0-110">IMonitorEventer</span></span>](imonitoreventer.md) | <span data-ttu-id="019c0-111">Stellt Methoden bereit, die zum Senden von Ereignissen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="019c0-111">Provides methods used to send events.</span></span> <span data-ttu-id="019c0-112">Diese Schnittstelle wird vom [*Überwachungs Steuerungs Dienst (Monitor Control Service*](m.md) , mcsvc) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="019c0-112">This interface is provided by the [*Monitor Control Service*](m.md) (MCSVC).</span></span> |



 

 

 



