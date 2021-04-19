---
description: Die spfilenotify \_ targetneuere-Benachrichtigung wird an die Rückruf Routine gesendet, wenn die zu kopierende Datei in die Warteschlange eingereiht ist, wenn die zu kopierende Datei den SP \_ -Kopiervorgang \_ neuer oder \_ eine neuere \_ \_ Version des SP-Kopiervorgangs enthält
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: SPFILENOTIFY_TARGETNEWER Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362300"
---
# <a name="spfilenotify_targetnewer-message"></a><span data-ttu-id="027cb-103">\_Spfilenotifiktargetneuere Nachricht</span><span class="sxs-lookup"><span data-stu-id="027cb-103">SPFILENOTIFY\_TARGETNEWER message</span></span>

<span data-ttu-id="027cb-104">Die **spfilenotify \_ targetneuere** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn die zu kopierende Datei in die Warteschlange eingereiht ist, wenn die zu kopierende Datei den SP \_ -Kopiervorgang \_ neuer oder \_ eine neuere \_ \_ Version des SP-Kopiervorgangs enthält</span><span class="sxs-lookup"><span data-stu-id="027cb-104">The **SPFILENOTIFY\_TARGETNEWER** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NEWER or SP\_COPY\_FORCE\_NEWER flags specified and a newer version of the file already exists in the target directory.</span></span> <span data-ttu-id="027cb-105">Er kann mit dem [**spfilenotify-Element " \_ langmismatch**](spfilenotify-langmismatch.md) " und/oder " [**spfilenotify \_ targetexists**](spfilenotify-targetexists.md)" allein an die Rückruf Routine oder "ORed" gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="027cb-105">It can be sent to the callback routine alone or ORed together with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md).</span></span>


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="027cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="027cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="027cb-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="027cb-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="027cb-108">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur, die Informationen zu den Pfaden für Quell-und Zieldateien enthält.</span><span class="sxs-lookup"><span data-stu-id="027cb-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="027cb-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="027cb-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="027cb-110">Dieser Parameter wird nicht verwendet, es sei denn, diese Benachrichtigung wird mithilfe des OR-Operators mit [**spfilenotify \_ langmismatch**](spfilenotify-langmismatch.md)kombiniert.</span><span class="sxs-lookup"><span data-stu-id="027cb-110">This parameter is not used unless this notification is combined, by using the OR operator, with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="027cb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="027cb-111">Return value</span></span>

<span data-ttu-id="027cb-112">Die Rückruf Routine muss einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="027cb-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="027cb-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="027cb-113">Return code</span></span>                                                                          | <span data-ttu-id="027cb-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="027cb-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="027cb-115"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="027cb-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="027cb-116">Überschreiben Sie die Datei im Zielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="027cb-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="027cb-117"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="027cb-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="027cb-118">Überspringt den aktuellen Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="027cb-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="027cb-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="027cb-119">Requirements</span></span>



| <span data-ttu-id="027cb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="027cb-120">Requirement</span></span> | <span data-ttu-id="027cb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="027cb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="027cb-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="027cb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="027cb-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="027cb-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="027cb-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="027cb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="027cb-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="027cb-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="027cb-126">Header</span><span class="sxs-lookup"><span data-stu-id="027cb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="027cb-127"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="027cb-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="027cb-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="027cb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="027cb-129">Übersicht</span><span class="sxs-lookup"><span data-stu-id="027cb-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="027cb-130">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="027cb-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="027cb-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="027cb-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="027cb-132">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="027cb-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="027cb-133">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="027cb-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="027cb-134">**Setupinstallfile**</span><span class="sxs-lookup"><span data-stu-id="027cb-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="027cb-135">**Setupinstallfileex**</span><span class="sxs-lookup"><span data-stu-id="027cb-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="027cb-136">**Setupinstallfrominf-Abschnitt**</span><span class="sxs-lookup"><span data-stu-id="027cb-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




