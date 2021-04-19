---
description: Die spfilenotify \_ fileincabinet-Benachrichtigung wird von setupiteratecabinet für jede Datei in der CAB-Datei an eine Rückruf Routine gesendet. Die Rückruf Routine muss einen Wert zurückgeben, der angibt, ob die Datei extrahiert werden soll.
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: SPFILENOTIFY_FILEINCABINET Meldung (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357053"
---
# <a name="spfilenotify_fileincabinet-message"></a><span data-ttu-id="b04bf-104">Spfilenotify \_ fileincabinet-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b04bf-104">SPFILENOTIFY\_FILEINCABINET message</span></span>

<span data-ttu-id="b04bf-105">Die **spfilenotify \_ fileincabinet** -Benachrichtigung wird von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) für jede Datei in der CAB-Datei an eine Rückruf Routine gesendet.</span><span class="sxs-lookup"><span data-stu-id="b04bf-105">The **SPFILENOTIFY\_FILEINCABINET** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) for each file found in the cabinet.</span></span> <span data-ttu-id="b04bf-106">Die Rückruf Routine muss einen Wert zurückgeben, der angibt, ob die Datei extrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b04bf-106">The callback routine must return a value indicating whether to extract the file.</span></span>


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a><span data-ttu-id="b04bf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b04bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b04bf-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="b04bf-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="b04bf-109">Zeiger auf eine [**Datei \_ in \_ \_**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) der CAB-Info-Struktur, die Informationen über die Datei in der CAB-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="b04bf-109">Pointer to a [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure that contains information about the file in the cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="b04bf-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="b04bf-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="b04bf-111">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Dateinamen der CAB-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="b04bf-111">Pointer to a null-terminated string that contains the filename of the cabinet file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b04bf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b04bf-112">Return value</span></span>

<span data-ttu-id="b04bf-113">Die Rückruf Routine sollte eine der folgenden zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b04bf-113">Your callback routine should return one of the following.</span></span>



| <span data-ttu-id="b04bf-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b04bf-114">Return code</span></span>                                                                                 | <span data-ttu-id="b04bf-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b04bf-115">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b04bf-116"><dt>**fileOp-über \_ springen**</dt></span><span class="sxs-lookup"><span data-stu-id="b04bf-116"><dt>**FILEOP\_SKIP**</dt></span></span> </dl> | <span data-ttu-id="b04bf-117">Extrahieren Sie die Datei nicht, und überspringen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="b04bf-117">Do not extract the file, skip it.</span></span><br/> |
| <dl> <span data-ttu-id="b04bf-118"><dt>**fileOp- \_ doit**</dt></span><span class="sxs-lookup"><span data-stu-id="b04bf-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl> | <span data-ttu-id="b04bf-119">Entpacken Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="b04bf-119">Extract the file.</span></span><br/>                 |



 

<span data-ttu-id="b04bf-120">Wenn Ihre Rückruf Routine fileOp \_ doit zurückgibt, sollte der Name, der für die extrahierte Datei verwendet werden soll, im **fulltargetname** -Member der [**Datei in der CAB \_ \_ \_ Info**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) -Struktur angegeben werden, die an die Routine in *param1* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b04bf-120">If your callback routine returns FILEOP\_DOIT, the name to use for the extracted file should be specified in the **FullTargetName** member of the [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure passed to the routine in *Param1*.</span></span>

> [!Note]  
> <span data-ttu-id="b04bf-121">Es ist keine standardmäßige CAB-Rückruf Routine vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b04bf-121">There is no default cabinet callback routine.</span></span> <span data-ttu-id="b04bf-122">Die Setup Anwendung sollte eine Rückruf Routine bereitstellen, um die von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)gesendeten Benachrichtigungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="b04bf-122">The setup application should supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b04bf-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b04bf-123">Requirements</span></span>



| <span data-ttu-id="b04bf-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b04bf-124">Requirement</span></span> | <span data-ttu-id="b04bf-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b04bf-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b04bf-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b04bf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b04bf-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b04bf-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b04bf-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b04bf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b04bf-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b04bf-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b04bf-130">Header</span><span class="sxs-lookup"><span data-stu-id="b04bf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b04bf-131"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b04bf-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b04bf-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b04bf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b04bf-133">Übersicht</span><span class="sxs-lookup"><span data-stu-id="b04bf-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="b04bf-134">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="b04bf-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="b04bf-135">**Datei \_ in CAB- \_ \_ Info**</span><span class="sxs-lookup"><span data-stu-id="b04bf-135">**FILE\_IN\_CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="b04bf-136">**Setupiteratecabinet**</span><span class="sxs-lookup"><span data-stu-id="b04bf-136">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




