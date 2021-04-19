---
description: Führen Sie die folgenden Schritte aus, um die Anwendungs Leistungsindikatoren aus dem System zu entfernen.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Löschen von Leistungsindikatoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba257a1a44b5272543b7e61dcdc4b4e96225c160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360543"
---
# <a name="deleting-performance-counters"></a><span data-ttu-id="89d83-103">Löschen von Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="89d83-103">Deleting Performance Counters</span></span>

<span data-ttu-id="89d83-104">Führen Sie die folgenden Schritte aus, um die Leistungsindikatoren der Anwendung aus dem System zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="89d83-104">To remove your application's performance counters from the system, perform the following steps.</span></span>

1.  <span data-ttu-id="89d83-105">Verwenden Sie das **unlodctr** -Tool, das auf dem Computer enthalten ist, um die gegenseitig relevanten Daten aus der Registrierung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="89d83-105">Use the **unlodctr** tool included with the computer to remove the counter related data from the registry.</span></span> <span data-ttu-id="89d83-106">Beachten Sie, dass der **Leistungs** Schlüssel der Anwendung vorhanden sein muss, damit das **unlodctr** -Tool erfolgreich ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="89d83-106">Note that the application's **Performance** key must exist for the **unlodctr** tool to succeed.</span></span> <span data-ttu-id="89d83-107">Weitere Informationen finden Sie unter [Entfernen von Counter-Namen und Beschreibungen aus der Registrierung](removing-counter-names-and-descriptions-from-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="89d83-107">For details, see [Removing Counter Names and Descriptions from the Registry](removing-counter-names-and-descriptions-from-the-registry.md).</span></span>
2.  <span data-ttu-id="89d83-108">Löschen Sie die **Leistungs** -und **Verknüpfungs** Schlüssel unter dem **Dienst** Schlüssel der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="89d83-108">Delete the **Performance** and **Linkage** keys under the application's **Services** key.</span></span> <span data-ttu-id="89d83-109">Um diese Schlüssel zu löschen, verwenden Sie entweder das Regedt32.exe-Hilfsprogramm oder den Befehl [**regdeletekey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span><span class="sxs-lookup"><span data-stu-id="89d83-109">To delete these keys, use either the Regedt32.exe utility or call [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span></span>

 

 
