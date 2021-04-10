---
description: Zusätzlich zur Verwendung des Standard Warteschlangen Rückrufs können Sie eine benutzerdefinierte Rückruf Routine schreiben.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Erstellen einer benutzerdefinierten Warteschlangen Rückruf Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119836e994709ff2d0fa21e12489af947394119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866940"
---
# <a name="creating-a-custom-queue-callback-routine"></a><span data-ttu-id="2ceb6-103">Erstellen einer benutzerdefinierten Warteschlangen Rückruf Routine</span><span class="sxs-lookup"><span data-stu-id="2ceb6-103">Creating a Custom Queue Callback Routine</span></span>

<span data-ttu-id="2ceb6-104">Zusätzlich zur Verwendung des Standard Warteschlangen Rückrufs können Sie eine benutzerdefinierte Rückruf Routine schreiben.</span><span class="sxs-lookup"><span data-stu-id="2ceb6-104">In addition to using the default queue callback, you can write a custom callback routine.</span></span> <span data-ttu-id="2ceb6-105">Diese Funktion muss dieselbe Form wie [*File Callback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2ceb6-105">This function must have the same form as [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="2ceb6-106">Dies ist hilfreich, wenn Sie eine Rückruf Routine benötigen, um eine Benachrichtigung auf eine andere Weise als die von der Standard Warteschlangen-Rückruf Routine bereitgestellte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="2ceb6-106">This is useful if you need a callback routine to handle a notification in a manner other than that provided by the default queue callback routine.</span></span>

<span data-ttu-id="2ceb6-107">Wenn nur ein kleiner Teil des Verhaltens der Standard Warteschlangen Rückruf Routine geändert werden muss, können Sie eine benutzerdefinierte Rückruf Routine erstellen, um die Benachrichtigungen zu filtern, und nur diejenigen behandeln, die ein spezielles Verhalten erfordern und [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) für die anderen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2ceb6-107">If only a small portion of the default queue callback routine's behavior needs to be changed, you can create a custom callback routine to filter the notifications, handling only those that require special behavior and calling [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) for the others.</span></span>

<span data-ttu-id="2ceb6-108">Wenn Sie z. b. Datei Lösch Fehler Benutzer definiert behandeln möchten, können Sie eine benutzerdefinierte Rückruffunktion ( *MyCallback*) erstellen.</span><span class="sxs-lookup"><span data-stu-id="2ceb6-108">For example, if you wanted to custom-handle file delete errors, you could create a custom callback function, *MyCallback*.</span></span> <span data-ttu-id="2ceb6-109">Diese Funktion würde [**spfilenotify \_ deleteerror**](spfilenotify-deleteerror.md) -Benachrichtigungen abfangen und verarbeiten und die standardmäßige Warteschlangen Rückruffunktion für alle anderen Benachrichtigungen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2ceb6-109">This function would intercept and process [**SPFILENOTIFY\_DELETEERROR**](spfilenotify-deleteerror.md) notifications, and call the default queue callback function for all other notifications.</span></span> <span data-ttu-id="2ceb6-110">*MyCallback* gibt einen Wert für die Fehler Benachrichtigungen zum Löschen zurück.</span><span class="sxs-lookup"><span data-stu-id="2ceb6-110">*MyCallback* returns a value for the delete error notifications.</span></span> <span data-ttu-id="2ceb6-111">Für alle anderen Benachrichtigungen übergibt *MyCallback* den Wert, der von der Standard Warteschlangen Rückruf-Routine an die Warteschlange zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2ceb6-111">For all other notifications, *MyCallback* passes whatever value the default queue callback routine returned to the queue.</span></span>

<span data-ttu-id="2ceb6-112">Diese Ablauf Steuerung wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2ceb6-112">This flow of control is illustrated in the following diagram.</span></span>

![Pfeile und Felder mit Datenfluss für benutzerdefinierte Rückruffunktion](images/callback.png)

> [!IMPORTANT]
> <span data-ttu-id="2ceb6-114">Wenn die benutzerdefinierte Rückruffunktion die standardmäßige Warteschlangen Rückruf-Routine aufruft, muss Sie den von [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) oder [**setupinitdefaultqueuecallbackex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) zurückgegebenen void-Zeiger an die Standard Rückruf Routine übergeben.</span><span class="sxs-lookup"><span data-stu-id="2ceb6-114">If the custom callback function calls the default queue callback routine, it must pass the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) to the default callback routine.</span></span>

 

 

 
