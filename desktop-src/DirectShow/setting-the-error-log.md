---
description: Festlegen des Fehler Protokolls
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: Festlegen des Fehler Protokolls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac96fb90570408ca41be06656f7cf1704e9f48dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342931"
---
# <a name="setting-the-error-log"></a><span data-ttu-id="099cf-103">Festlegen des Fehler Protokolls</span><span class="sxs-lookup"><span data-stu-id="099cf-103">Setting the Error Log</span></span>

<span data-ttu-id="099cf-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="099cf-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="099cf-105">Nachdem Sie die Fehler Protokollierungs Klasse implementiert haben, erstellen Sie eine neue Instanz der-Klasse.</span><span class="sxs-lookup"><span data-stu-id="099cf-105">After you implement the error logging class, create a new instance of the class.</span></span> <span data-ttu-id="099cf-106">Weisen Sie dann [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) einen Zeiger darauf zu, indem Sie die Methode [**iamseterrorlog::p UT \_ ErrorLog**](iamseterrorlog-put-errorlog.md) auf der Zeitachse aufrufen.</span><span class="sxs-lookup"><span data-stu-id="099cf-106">Then, give [DirectShow Editing Services](directshow-editing-services.md) a pointer to it by calling the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span> <span data-ttu-id="099cf-107">Fragen Sie die Zeitachse für die **iamset terrorlog** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="099cf-107">Query the timeline for the **IAMSetErrorLog** interface.</span></span> <span data-ttu-id="099cf-108">Um sicherzustellen, dass alle Fehler protokolliert werden, sollten Sie diese Methode vor dem Laden, speichern oder Rendering der Zeitachse abrufen.</span><span class="sxs-lookup"><span data-stu-id="099cf-108">To ensure that all errors are logged, you should call this method before you load, save, or render the timeline.</span></span>


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



<span data-ttu-id="099cf-109">Die Fehler Protokollierung hat keine Auswirkung auf die Rückgabewerte, die Sie erhalten, wenn Sie Methoden in der Anwendung aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="099cf-109">Error logging has no effect on the return values that you receive when you call methods in your application.</span></span> <span data-ttu-id="099cf-110">Die Fehler Protokollierung wird ergänzt, aber die üblichen Fehler Behandlungstechniken werden nicht ersetzt.</span><span class="sxs-lookup"><span data-stu-id="099cf-110">Error logging complements but does not replace the usual error handling techniques.</span></span> <span data-ttu-id="099cf-111">Überprüfen Sie immer HRESULT-Werte, um eine robuste Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="099cf-111">To create a robust application, always check HRESULT values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="099cf-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="099cf-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="099cf-113">Protokollierungs Fehler</span><span class="sxs-lookup"><span data-stu-id="099cf-113">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



