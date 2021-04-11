---
description: Die spfilenotify \_ neednewcab-Benachrichtigung wird von setupiteratecabinet gesendet, um anzugeben, dass die aktuelle Datei in einer anderen CAB-Datei fortgesetzt wird.
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: SPFILENOTIFY_NEEDNEWCABINET Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218175"
---
# <a name="spfilenotify_neednewcabinet-message"></a><span data-ttu-id="5ab78-103">Spfilenotify \_ neednewcab-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5ab78-103">SPFILENOTIFY\_NEEDNEWCABINET message</span></span>

<span data-ttu-id="5ab78-104">Die **spfilenotify \_ neednewcab** -Benachrichtigung wird von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) gesendet, um anzugeben, dass die aktuelle Datei in einer anderen CAB-Datei fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="5ab78-104">The **SPFILENOTIFY\_NEEDNEWCABINET** notification is sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate that the current file continues in another cabinet.</span></span> <span data-ttu-id="5ab78-105">Die Rückruf Routine kann dann [**setuppromptfordisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)aufrufen oder ein eigenes Dialogfeld erstellen, in dem der Benutzer aufgefordert wird, den nächsten Datenträger einzufügen.</span><span class="sxs-lookup"><span data-stu-id="5ab78-105">Your callback routine can then call [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), or create its own dialog box to prompt the user to insert the next disk.</span></span>


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a><span data-ttu-id="5ab78-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ab78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ab78-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="5ab78-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="5ab78-108">Ein Zeiger auf eine CAB [**-Informationsstruktur \_**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) , die Informationen über die CAB-Datei und die zu extrahierende Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="5ab78-108">Pointer to a [**CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) structure that contains information about the cabinet and the file to be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="5ab78-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="5ab78-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="5ab78-110">Wenn der Rückruf keinen Fehler zurückgibt \_ , ist dieser Parameter ein Zeiger auf eine NULL-terminierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5ab78-110">If the callback returns NO\_ERROR, this parameter is a pointer to a null-terminated string.</span></span> <span data-ttu-id="5ab78-111">Wenn die Zeichenfolge nicht leer ist, wird ein neuer Pfad zur CAB-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="5ab78-111">If the string is not empty, it specifies a new path to the cabinet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ab78-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ab78-112">Return value</span></span>

<span data-ttu-id="5ab78-113">Die Routine sollte einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5ab78-113">Your routine should return one of the following values.</span></span>



| <span data-ttu-id="5ab78-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5ab78-114">Return code</span></span>                                                                                 | <span data-ttu-id="5ab78-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ab78-115">Description</span></span>                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ab78-116"><dt>**kein \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="5ab78-116"><dt>**NO\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="5ab78-117">Es wurde kein Fehler gefunden. setzen Sie die Verarbeitung der CAB-</span><span class="sxs-lookup"><span data-stu-id="5ab78-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="5ab78-118"><dt>\**Fehler \_* XXX \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="5ab78-118"><dt>\**ERROR\_* XXX\*\*\*</dt></span></span> </dl> | <span data-ttu-id="5ab78-119">Ein Fehler des angegebenen Typs ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="5ab78-119">An error of the specified type occurred.</span></span> <span data-ttu-id="5ab78-120">Die [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) -Funktion gibt " **false**" zurück, und der angegebene Fehlercode wird durch einen get-Befehl von " [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ab78-120">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="5ab78-121">Es ist keine standardmäßige CAB-Rückruf Routine vorhanden. Daher müssen Sie eine Rückruf Routine bereitstellen, um die von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)gesendeten Benachrichtigungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5ab78-121">There is no default cabinet callback routine; thus, you must supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="remarks"></a><span data-ttu-id="5ab78-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ab78-122">Remarks</span></span>

<span data-ttu-id="5ab78-123">Wenn die Rückruf Routine keinen Fehler zurückgibt \_ , prüft [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) den Puffer, auf den von *Param2* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5ab78-123">If the callback routine returns NO\_ERROR, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) checks the buffer pointed to by *Param2*.</span></span> <span data-ttu-id="5ab78-124">Wenn der Puffer nicht leer ist, enthält er einen neuen Quellpfad.</span><span class="sxs-lookup"><span data-stu-id="5ab78-124">If the buffer is not empty, then it contains a new source path.</span></span> <span data-ttu-id="5ab78-125">Wenn der Puffer leer ist, wird davon ausgegangen, dass der Quellpfad unverändert ist.</span><span class="sxs-lookup"><span data-stu-id="5ab78-125">If the buffer is empty, the source path is assumed to be unchanged.</span></span>

<span data-ttu-id="5ab78-126">Die Rückruffunktion sollte sicherstellen, dass auf die CAB-Datei zugegriffen werden kann, bevor Sie zurückkehrt, und die Funktion [**setuppromptfordisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) aufrufen, wenn neue Medien eingefügt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5ab78-126">Your callback function should ensure that the cabinet is accessible before it returns, calling the [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) function, if new media needs to be inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ab78-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ab78-127">Requirements</span></span>



| <span data-ttu-id="5ab78-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ab78-128">Requirement</span></span> | <span data-ttu-id="5ab78-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5ab78-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab78-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ab78-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5ab78-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ab78-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5ab78-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ab78-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5ab78-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ab78-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5ab78-134">Header</span><span class="sxs-lookup"><span data-stu-id="5ab78-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ab78-135"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ab78-135"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ab78-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5ab78-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab78-137">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5ab78-137">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="5ab78-138">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="5ab78-138">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="5ab78-139">**CAB- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="5ab78-139">**CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="5ab78-140">**Setupiteratecabinet**</span><span class="sxs-lookup"><span data-stu-id="5ab78-140">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

