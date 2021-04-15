---
description: Die spfilenotify \_ targetexists-Benachrichtigung wird an die Rückruf Routine gesendet, wenn die zu kopierende Datei mit dem SP \_ Copy \_ noüberschreibungsflag in die Warteschlange eingereiht wurde und diese Datei bereits im Zielverzeichnis vorhanden ist.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: SPFILENOTIFY_TARGETEXISTS Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393714"
---
# <a name="spfilenotify_targetexists-message"></a><span data-ttu-id="af314-103">Spfilenotify \_ targetexists-Meldung</span><span class="sxs-lookup"><span data-stu-id="af314-103">SPFILENOTIFY\_TARGETEXISTS message</span></span>

<span data-ttu-id="af314-104">Die **spfilenotify \_ targetexists** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn die zu kopierende Datei mit dem SP \_ Copy \_ noüberschreibungsflag in die Warteschlange eingereiht wurde und diese Datei bereits im Zielverzeichnis vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="af314-104">The **SPFILENOTIFY\_TARGETEXISTS** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NOOVERWRITE flag and that file already exists in the target directory.</span></span> <span data-ttu-id="af314-105">Sie kann mithilfe des OR-Operators allein oder mithilfe des-Operators oder mit den [**spfilenotify- \_ Fehlern (spfilenotify**](spfilenotify-langmismatch.md) ) und/oder [**spfilenotify \_ targetneueren**](spfilenotify-targetnewer.md) -Benachrichtigungen an die Rückruf Routine gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="af314-105">It can be sent to the callback routine alone or combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md) notifications.</span></span>


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="af314-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="af314-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af314-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="af314-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="af314-108">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur, die Informationen zu den Pfaden für die Quell-und Zieldateien enthält.</span><span class="sxs-lookup"><span data-stu-id="af314-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="af314-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="af314-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="af314-110">Dieser Parameter wird nicht verwendet, es sei denn, diese Benachrichtigung wird mithilfe des OR-Operators mit der Benachrichtigung [**spfilenotify \_ langmismatch**](spfilenotify-langmismatch.md) kombiniert.</span><span class="sxs-lookup"><span data-stu-id="af314-110">This parameter is not used unless this notification is combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af314-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af314-111">Return value</span></span>

<span data-ttu-id="af314-112">Die Rückruf Routine muss einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="af314-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="af314-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="af314-113">Return code</span></span>                                                                          | <span data-ttu-id="af314-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af314-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="af314-115"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="af314-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="af314-116">Überschreiben Sie die Datei im Zielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="af314-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="af314-117"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="af314-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="af314-118">Überspringt den aktuellen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="af314-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="af314-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af314-119">Requirements</span></span>



| <span data-ttu-id="af314-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af314-120">Requirement</span></span> | <span data-ttu-id="af314-121">Wert</span><span class="sxs-lookup"><span data-stu-id="af314-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af314-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af314-122">Minimum supported client</span></span><br/> | <span data-ttu-id="af314-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af314-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="af314-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af314-124">Minimum supported server</span></span><br/> | <span data-ttu-id="af314-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af314-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af314-126">Header</span><span class="sxs-lookup"><span data-stu-id="af314-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="af314-127"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="af314-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af314-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="af314-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af314-129">Übersicht</span><span class="sxs-lookup"><span data-stu-id="af314-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="af314-130">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="af314-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="af314-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="af314-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="af314-132">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="af314-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="af314-133">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="af314-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="af314-134">**Setupinstallfile**</span><span class="sxs-lookup"><span data-stu-id="af314-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="af314-135">**Setupinstallfileex**</span><span class="sxs-lookup"><span data-stu-id="af314-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="af314-136">**Setupinstallfrominf-Abschnitt**</span><span class="sxs-lookup"><span data-stu-id="af314-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




