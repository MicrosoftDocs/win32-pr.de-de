---
description: Da die Setup-API keine standardmäßige CAB-Rückruf Routine bereitstellt, müssen Sie eine Routine bereitstellen. Die Rückruf Routine, die für die setupiteratecabinet-Funktion erforderlich ist, muss dieselbe Form aufweisen wie die, auf die von filecallback verwiesen wird.
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: Erstellen einer CAB-Rückruf Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216336"
---
# <a name="creating-a-cabinet-callback-routine"></a><span data-ttu-id="49be5-104">Erstellen einer CAB-Rückruf Routine</span><span class="sxs-lookup"><span data-stu-id="49be5-104">Creating a Cabinet Callback Routine</span></span>

<span data-ttu-id="49be5-105">Da die Setup-API keine standardmäßige CAB-Rückruf Routine bereitstellt, müssen Sie eine Routine bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="49be5-105">Because the Setup API does not supply a default cabinet callback routine, you need to supply a routine.</span></span> <span data-ttu-id="49be5-106">Die Rückruf Routine, die für die [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) -Funktion erforderlich ist, muss dieselbe Form aufweisen wie die, auf die von [filecallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="49be5-106">The callback routine that the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function requires must have the same form as those pointed to by [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span>

<span data-ttu-id="49be5-107">Im folgenden finden Sie die Syntax, die [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) verwendet, um eine Benachrichtigung an die Rückruf Routine zu senden.</span><span class="sxs-lookup"><span data-stu-id="49be5-107">Following is the syntax that [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

<span data-ttu-id="49be5-108">Der *Kontext* Parameter ist ein void-Zeiger auf eine Kontext Variable oder-Struktur, die von der Rückruf Routine verwendet werden kann, um Informationen zu speichern, die zwischen nachfolgenden Aufrufen der Rückruf Routine beibehalten werden müssen.</span><span class="sxs-lookup"><span data-stu-id="49be5-108">The *Context* parameter is a void pointer to a context variable or structure that can be used by the callback routine to store information that needs to persist between subsequent calls to the callback routine.</span></span>

<span data-ttu-id="49be5-109">Die Implementierung dieses Kontexts wird durch die Rückruf Routine angegeben und nie von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)referenziert oder geändert.</span><span class="sxs-lookup"><span data-stu-id="49be5-109">This context's implementation is specified by the callback routine, and it is never referenced or altered by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

<span data-ttu-id="49be5-110">Der *Benachrichtigungs* Parameter ist eine Ganzzahl ohne Vorzeichen und hat einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="49be5-110">The *Notification* parameter is an unsigned integer and will be one of the following values.</span></span>



| <span data-ttu-id="49be5-111">Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="49be5-111">Notification</span></span>                                                        | <span data-ttu-id="49be5-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49be5-112">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="49be5-113">**spfilenotifizieren von \_ fileextrahierung**</span><span class="sxs-lookup"><span data-stu-id="49be5-113">**SPFILENOTIFY\_FILEEXTRACTED**</span></span>](spfilenotify-fileextracted.md)   | <span data-ttu-id="49be5-114">Die Datei wurde aus der CAB-Datei extrahiert.</span><span class="sxs-lookup"><span data-stu-id="49be5-114">The file has been extracted from the cabinet.</span></span>      |
| [<span data-ttu-id="49be5-115">**spfilenotify \_ filinput Cabinet**</span><span class="sxs-lookup"><span data-stu-id="49be5-115">**SPFILENOTIFY\_FILEINCABINET**</span></span>](spfilenotify-fileincabinet.md)   | <span data-ttu-id="49be5-116">In der CAB-Datei ist eine Datei aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="49be5-116">A file is encountered in the cabinet.</span></span>              |
| [<span data-ttu-id="49be5-117">**spfilenotify \_ neednewcabinet**</span><span class="sxs-lookup"><span data-stu-id="49be5-117">**SPFILENOTIFY\_NEEDNEWCABINET**</span></span>](spfilenotify-neednewcabinet.md) | <span data-ttu-id="49be5-118">Die aktuelle Datei wird in der nächsten CAB-Datei fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="49be5-118">The current file is continued in the next cabinet.</span></span> |



 

<span data-ttu-id="49be5-119">Die letzten zwei Parameter, *param1* und *Param2*, sind auch ganze Zahlen ohne Vorzeichen und enthalten zusätzliche Informationen, die für die Benachrichtigung relevant sind.</span><span class="sxs-lookup"><span data-stu-id="49be5-119">The final two parameters, *Param1* and *Param2*, are also unsigned integers and contain additional information relevant to the notification.</span></span> <span data-ttu-id="49be5-120">Weitere Informationen zu den von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)gesendeten Benachrichtigungen finden Sie unter CAB- [Datei Benachrichtigungen](cabinet-file-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="49be5-120">For more information about the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), see [Cabinet File Notifications](cabinet-file-notifications.md).</span></span>

<span data-ttu-id="49be5-121">Eine SP- \_ Datei \_ Benachrichtigungs \_ Rückruf-Routine gibt eine ganze Zahl ohne Vorzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="49be5-121">A SP\_FILE\_NOTIFY\_CALLBACK routine returns an unsigned integer.</span></span> <span data-ttu-id="49be5-122">Die CAB-Rückruf Routine sollte abhängig von der Benachrichtigung einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="49be5-122">The cabinet callback routine should return one of the following values depending on the notification.</span></span>

<span data-ttu-id="49be5-123">Für die spfilenotify \_ fileincabinet-Benachrichtigung erwartet [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) , dass einer der folgenden Werte von der Rückruf Routine zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="49be5-123">For the SPFILENOTIFY\_FILEINCABINET notification, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="49be5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="49be5-124">Value</span></span>         | <span data-ttu-id="49be5-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="49be5-125">Meaning</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="49be5-126">fileOp- \_ Abbruch</span><span class="sxs-lookup"><span data-stu-id="49be5-126">FILEOP\_ABORT</span></span> | <span data-ttu-id="49be5-127">Abbrechen der CAB-Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="49be5-127">Abort cabinet processing.</span></span> |
| <span data-ttu-id="49be5-128">fileOp- \_ doit</span><span class="sxs-lookup"><span data-stu-id="49be5-128">FILEOP\_DOIT</span></span>  | <span data-ttu-id="49be5-129">Extrahieren Sie die aktuelle Datei.</span><span class="sxs-lookup"><span data-stu-id="49be5-129">Extract the current file.</span></span> |
| <span data-ttu-id="49be5-130">fileOp-über \_ springen</span><span class="sxs-lookup"><span data-stu-id="49be5-130">FILEOP\_SKIP</span></span>  | <span data-ttu-id="49be5-131">Überspringen Sie die aktuelle Datei.</span><span class="sxs-lookup"><span data-stu-id="49be5-131">Skip the current file.</span></span>    |



 

<span data-ttu-id="49be5-132">Für spfilenotify \_ neednewcab-und spfilenotify- \_ fileextrahierte Benachrichtigungen erwartet **setupiteratecabinet** , dass einer der folgenden Werte von der Rückruf Routine zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="49be5-132">For SPFILENOTIFY\_NEEDNEWCABINET and SPFILENOTIFY\_FILEEXTRACTED notifications, **SetupIterateCabinet** expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="49be5-133">Wert</span><span class="sxs-lookup"><span data-stu-id="49be5-133">Value</span></span>      | <span data-ttu-id="49be5-134">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="49be5-134">Meaning</span></span>                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49be5-135">kein \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="49be5-135">NO\_ERROR</span></span>  | <span data-ttu-id="49be5-136">Es wurde kein Fehler gefunden. setzen Sie die Verarbeitung der CAB-</span><span class="sxs-lookup"><span data-stu-id="49be5-136">No error was encountered, continue processing the cabinet.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="49be5-137">Fehler \_ xxx</span><span class="sxs-lookup"><span data-stu-id="49be5-137">ERROR\_XXX</span></span> | <span data-ttu-id="49be5-138">Ein Fehler des angegebenen Typs ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="49be5-138">An error of the specified type occurred.</span></span> <span data-ttu-id="49be5-139">Die [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) -Funktion gibt " **false**" zurück, und der angegebene Fehlercode wird durch einen get-Befehl von " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="49be5-139">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> |



 

<span data-ttu-id="49be5-140">Wenn die Rückruf Routine fileOp \_ doit zurückgibt, muss die Routine auch einen vollständigen Zielpfad bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="49be5-140">If the callback routine returns FILEOP\_DOIT, the routine must also provide a full target path.</span></span> <span data-ttu-id="49be5-141">Weitere Informationen finden Sie unter [**spfilenotify \_ fileincabinet**](spfilenotify-fileincabinet.md).</span><span class="sxs-lookup"><span data-stu-id="49be5-141">For more information see [**SPFILENOTIFY\_FILEINCABINET**](spfilenotify-fileincabinet.md).</span></span>

 

 
