---
description: Die "spfilenotify"- \_ \_ Benachrichtigungs Benachrichtigungs Benachrichtigung wird von setupscanfilequeue für jeden Knoten in der Kopier unter Warteschlange der Datei Warteschlange an eine Rückruf Routine gesendet.
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: SPFILENOTIFY_QUEUESCAN_SIGNERINFO Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960112"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a><span data-ttu-id="5d346-103">Spfilenotifizieren der \_ Warteschlangen \_ Meldung "SignerInfo"</span><span class="sxs-lookup"><span data-stu-id="5d346-103">SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO message</span></span>

<span data-ttu-id="5d346-104">Die " **spfilenotify" \_ - \_** Benachrichtigungs Benachrichtigungs Benachrichtigung wird von [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) für jeden Knoten in der Kopier unter Warteschlange der Datei Warteschlange an eine Rückruf Routine gesendet.</span><span class="sxs-lookup"><span data-stu-id="5d346-104">The **SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="5d346-105">Dies ist nur der Fall, wenn die **setupscanfilequeue** -Funktion aufgerufen wurde, wobei das Flag SPQ \_ Scan \_ \_ Callback \_ SignerInfo verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d346-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK\_SIGNERINFO.</span></span> <span data-ttu-id="5d346-106">Verfügbar ab Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5d346-106">Available starting with Windows XP.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="5d346-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d346-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d346-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="5d346-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="5d346-109">Zeiger auf eine [**FilePath- \_ SignerInfo**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5d346-109">Pointer to a [**FILEPATHS\_SIGNERINFO**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) structure.</span></span> <span data-ttu-id="5d346-110">Das **Zielmember** ist der Dateiname der Zieldatei im System.</span><span class="sxs-lookup"><span data-stu-id="5d346-110">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="5d346-111">Der **Quell** Member ist der erwartete Pfad der Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="5d346-111">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="5d346-112">Der **Win32Error** -Member ist der Signatur Fehler.</span><span class="sxs-lookup"><span data-stu-id="5d346-112">The **Win32Error** member is the signing error.</span></span> <span data-ttu-id="5d346-113">Signatur Informationen werden zurückgegeben, wenn die Rückruf Routine **Win32Error**= = No error zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="5d346-113">Signature information is returned if the callback routine returns **Win32Error**==NO\_ERROR.</span></span> <span data-ttu-id="5d346-114">Der **digitalsigner** -Member ist der digitale Signatur Geber.</span><span class="sxs-lookup"><span data-stu-id="5d346-114">The **DigitalSigner** member is the digital signer.</span></span> <span data-ttu-id="5d346-115">Der **Versions** Member ist die Version.</span><span class="sxs-lookup"><span data-stu-id="5d346-115">The **Version** member is the version.</span></span> <span data-ttu-id="5d346-116">Die **catalogfile** ist die Katalog Datei.</span><span class="sxs-lookup"><span data-stu-id="5d346-116">The **CatalogFile** is the catalog file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d346-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d346-117">Return value</span></span>

<span data-ttu-id="5d346-118">Die Rückruf Routine sollte einen [Systemfehler Code](/windows/desktop/Debug/system-error-codes)zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5d346-118">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="5d346-119">Wenn die Rückruf Routine keinen Fehler zurückgibt \_ , wird die Warteschlangen Überprüfung fortgesetzt, und es wird zurückgegeben, wenn die Routine einen anderen Fehlercode zurückgibt, die Warteschlangen Überprüfung abgebrochen und [**setupscanfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) **false** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5d346-119">If the callback routine returns NO\_ERROR, the queue scan continues, and returns If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="5d346-120">Diese Benachrichtigung wird nicht von der [**setupdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) -Funktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5d346-120">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d346-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d346-121">Requirements</span></span>



| <span data-ttu-id="5d346-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d346-122">Requirement</span></span> | <span data-ttu-id="5d346-123">Wert</span><span class="sxs-lookup"><span data-stu-id="5d346-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d346-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d346-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5d346-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d346-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5d346-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d346-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5d346-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d346-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d346-128">Header</span><span class="sxs-lookup"><span data-stu-id="5d346-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d346-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d346-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d346-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5d346-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d346-131">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5d346-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="5d346-132">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="5d346-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="5d346-133">**Setupscanfilequeue**</span><span class="sxs-lookup"><span data-stu-id="5d346-133">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

