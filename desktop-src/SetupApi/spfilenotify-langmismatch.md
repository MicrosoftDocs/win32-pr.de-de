---
description: Die spfilenotify \_ langmismatch-Benachrichtigung wird an die Rückruf Routine gesendet, wenn die Sprache der zu kopierenden Datei nicht mit der Sprache einer vorhandenen Zieldatei übereinstimmt.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: SPFILENOTIFY_LANGMISMATCH Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359540"
---
# <a name="spfilenotify_langmismatch-message"></a><span data-ttu-id="a2b97-103">Spfilenotify \_ langmismatch-Meldung</span><span class="sxs-lookup"><span data-stu-id="a2b97-103">SPFILENOTIFY\_LANGMISMATCH message</span></span>

<span data-ttu-id="a2b97-104">Die **spfilenotify \_ langmismatch** -Benachrichtigung wird an die Rückruf Routine gesendet, wenn die Sprache der zu kopierenden Datei nicht mit der Sprache einer vorhandenen Zieldatei übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a2b97-104">The **SPFILENOTIFY\_LANGMISMATCH** notification is sent to the callback routine if the language of the file to be copied does not match the language of an existing target file.</span></span> <span data-ttu-id="a2b97-105">Sie kann mithilfe des OR-Operators, mit [**spfilenotify \_ targetexists**](spfilenotify-targetexists.md) und/oder [**spfilenotify \_ targetneueren**](spfilenotify-targetnewer.md), einzeln oder in Kombination mit der Rückruf Routine gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="a2b97-105">It can be sent to the callback routine alone or combined, by using the OR operator, with [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md).</span></span>


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="a2b97-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2b97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2b97-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="a2b97-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="a2b97-108">Zeiger auf eine [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) -Struktur, die Informationen zu den Pfaden der Quell-und Zieldateien enthält.</span><span class="sxs-lookup"><span data-stu-id="a2b97-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths of the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="a2b97-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="a2b97-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="a2b97-110">Identifiziert die nicht übereinstimmenden Sprachen.</span><span class="sxs-lookup"><span data-stu-id="a2b97-110">Identifies the mismatched languages.</span></span> <span data-ttu-id="a2b97-111">Dieser Member hat den sprach Bezeichner der Quelldatei im niedrigen Wort und den sprach Bezeichner der vorhandenen Zieldatei im hohen Wort.</span><span class="sxs-lookup"><span data-stu-id="a2b97-111">This member has the language identifier of the source file in the low word, and the language identifier of the existing target file in the high word.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2b97-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2b97-112">Return value</span></span>

<span data-ttu-id="a2b97-113">Die Rückruf Routine muss einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a2b97-113">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="a2b97-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a2b97-114">Return code</span></span>                                                                          | <span data-ttu-id="a2b97-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2b97-115">Description</span></span>                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a2b97-116"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="a2b97-116"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="a2b97-117">Kopieren Sie die Datei, und überschreiben Sie die vorhandene Datei.</span><span class="sxs-lookup"><span data-stu-id="a2b97-117">Copy the file and overwrite the existing file.</span></span><br/>               |
| <dl> <span data-ttu-id="a2b97-118"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="a2b97-118"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="a2b97-119">Überspringen Sie den Kopiervorgang.</span><span class="sxs-lookup"><span data-stu-id="a2b97-119">Skip the copy operation.</span></span> <span data-ttu-id="a2b97-120">Überschreiben Sie die vorhandene Datei nicht.</span><span class="sxs-lookup"><span data-stu-id="a2b97-120">Do not overwrite the existing file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a2b97-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2b97-121">Requirements</span></span>



| <span data-ttu-id="a2b97-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2b97-122">Requirement</span></span> | <span data-ttu-id="a2b97-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a2b97-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b97-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2b97-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a2b97-125">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2b97-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a2b97-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2b97-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a2b97-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a2b97-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2b97-128">Header</span><span class="sxs-lookup"><span data-stu-id="a2b97-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2b97-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2b97-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2b97-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a2b97-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2b97-131">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a2b97-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="a2b97-132">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="a2b97-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="a2b97-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="a2b97-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="a2b97-134">**Setupcommitfilequeue**</span><span class="sxs-lookup"><span data-stu-id="a2b97-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="a2b97-135">**Setupdefaultqueuecallback**</span><span class="sxs-lookup"><span data-stu-id="a2b97-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="a2b97-136">**Setupinstallfile**</span><span class="sxs-lookup"><span data-stu-id="a2b97-136">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="a2b97-137">**Setupinstallfileex**</span><span class="sxs-lookup"><span data-stu-id="a2b97-137">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="a2b97-138">**Setupinstallfrominf-Abschnitt**</span><span class="sxs-lookup"><span data-stu-id="a2b97-138">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




