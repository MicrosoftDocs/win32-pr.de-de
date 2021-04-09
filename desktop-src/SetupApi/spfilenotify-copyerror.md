---
description: Die spfilenotify- \_ copyError-Benachrichtigung wird an die Rückruf Routine gesendet, wenn während eines Datei Kopiervorgangs ein Fehler auftritt.
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: SPFILENOTIFY_COPYERROR Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd44daabd6a4aed5e61a716bab3df44f35fc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865715"
---
# <a name="spfilenotify_copyerror-message"></a><span data-ttu-id="5296d-103">Spfilenotify- \_ copyError-Meldung</span><span class="sxs-lookup"><span data-stu-id="5296d-103">SPFILENOTIFY\_COPYERROR message</span></span>

<span data-ttu-id="5296d-104">Die **spfilenotify- \_ copyError** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn während eines Datei Kopiervorgangs ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="5296d-104">The **SPFILENOTIFY\_COPYERROR** notification is sent to the callback routine if an error occurs during a file copy operation.</span></span>


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a><span data-ttu-id="5296d-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="5296d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5296d-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="5296d-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="5296d-107">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5296d-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5296d-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="5296d-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="5296d-109">Zeiger auf einen Puffer mit einer Größe von Max. \_ Pfad Zeichen, der neue Pfadinformationen speichert, die vom Benutzer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5296d-109">Pointer to a buffer, of size MAX\_PATH characters, that stores new path information specified by the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5296d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5296d-110">Return value</span></span>

<span data-ttu-id="5296d-111">Der Rückruf muss einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5296d-111">The callback should return one of the following values.</span></span>



| <span data-ttu-id="5296d-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5296d-112">Return code</span></span>                                                                                    | <span data-ttu-id="5296d-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5296d-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5296d-114"><dt>**fileOp- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="5296d-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="5296d-115">Die Warteschlangen Verarbeitung sollte abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="5296d-115">Queue processing should be canceled.</span></span> <span data-ttu-id="5296d-116">[**Setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) gibt 0 (null) zurück, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt erweiterte Fehlerinformationen zurück, wie z. b. \_ den Fehler abgebrochen (wenn der Benutzer abgebrochen hat) oder einen Fehler \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="5296d-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="5296d-117"><dt>**fileOp \_ NewPath**</dt></span><span class="sxs-lookup"><span data-stu-id="5296d-117"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="5296d-118">Wiederholen Sie den Kopiervorgang mit dem Pfad der Rückruffunktion, die im Puffer platziert wurde, auf den der *Param2* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="5296d-118">Retry the copy operation using the path the callback function placed in the buffer pointed to by the *Param2* parameter.</span></span> <span data-ttu-id="5296d-119">Die Rückruf Routine sollte sicherstellen, dass der Pfad die Puffergröße eines TCHAR-Arrays von Max- \_ Pfad Elementen nicht überflutet.</span><span class="sxs-lookup"><span data-stu-id="5296d-119">The callback routine should ensure that the path does not overflow the buffer size of a TCHAR array of MAX\_PATH elements.</span></span><br/>                |
| <dl> <span data-ttu-id="5296d-120"><dt>**fileOp- \_ Wiederholung**</dt></span><span class="sxs-lookup"><span data-stu-id="5296d-120"><dt>**FILEOP\_RETRY**</dt></span></span> </dl>   | <span data-ttu-id="5296d-121">Der Benutzer versucht erneut, den Kopiervorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5296d-121">The user is attempting the copy operation again.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="5296d-122"><dt>**fileOp-über \_ springen**</dt></span><span class="sxs-lookup"><span data-stu-id="5296d-122"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="5296d-123">Der Benutzer wird den Datei Kopiervorgang übersprungen.</span><span class="sxs-lookup"><span data-stu-id="5296d-123">The user is skipping the file copy operation.</span></span><br/>                                                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="5296d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5296d-124">Requirements</span></span>



| <span data-ttu-id="5296d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5296d-125">Requirement</span></span> | <span data-ttu-id="5296d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5296d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5296d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5296d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5296d-128">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5296d-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5296d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5296d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5296d-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5296d-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5296d-131">Header</span><span class="sxs-lookup"><span data-stu-id="5296d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5296d-132"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5296d-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5296d-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5296d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5296d-134">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5296d-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="5296d-135">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="5296d-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="5296d-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="5296d-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="5296d-137">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="5296d-137">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="5296d-138">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="5296d-138">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

