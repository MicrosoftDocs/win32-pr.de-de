---
title: Readermodumfo-Struktur
description: Enthält Informationen, die zum Initialisieren der doreadermode-Funktion erforderlich sind.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- Readermodeingefo-Struktur Windows-Steuerelemente
- Preadermodeingefo-Struktur Zeiger-Windows-Steuerelemente
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dacf0fc59ef62447ca12b7a470689e13967d687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477853"
---
# <a name="readermodeinfo-structure"></a><span data-ttu-id="061c1-105">Readermodumfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="061c1-105">READERMODEINFO structure</span></span>

<span data-ttu-id="061c1-106">\[**Readermodeinfo** wird durch Windows XP mit Service Pack 2 (SP2) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="061c1-106">\[**READERMODEINFO** is supported through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="061c1-107">Dies wird in nachfolgenden Versionen möglicherweise nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="061c1-107">It might be unsupported in subsequent versions.\]</span></span>

<span data-ttu-id="061c1-108">Enthält Informationen, die zum Initialisieren der [**doreadermode**](doreadermode.md) -Funktion erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="061c1-108">Contains information required to initialize the [**DoReaderMode**](doreadermode.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="061c1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="061c1-109">Syntax</span></span>


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a><span data-ttu-id="061c1-110">Member</span><span class="sxs-lookup"><span data-stu-id="061c1-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="061c1-111">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="061c1-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="061c1-112">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="061c1-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="061c1-113">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="061c1-113">Required.</span></span> <span data-ttu-id="061c1-114">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="061c1-114">The size of the structure, in bytes.</span></span> <span data-ttu-id="061c1-115">Legen Sie diesen Parameter auf **sizeof (readermode)** fest, bevor Sie " [**doreadermode**](doreadermode.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="061c1-115">Set this parameter to **sizeof(READERMODE)** before you call [**DoReaderMode**](doreadermode.md).</span></span>

</dd> <dt>

<span data-ttu-id="061c1-116">**HWND**</span><span class="sxs-lookup"><span data-stu-id="061c1-116">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="061c1-117">Typ: **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="061c1-117">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="061c1-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="061c1-118">Required.</span></span> <span data-ttu-id="061c1-119">Das Handle des Fensters, das für den Lesemodus verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="061c1-119">The handle of the window to be used for reader mode.</span></span>

</dd> <dt>

<span data-ttu-id="061c1-120">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="061c1-120">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="061c1-121">Typ: **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="061c1-121">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="061c1-122">Flags, mit denen die Funktionalität des Fensters "Lesemodus" angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="061c1-122">Flags customizing the functionality of the reader mode window.</span></span> <span data-ttu-id="061c1-123">Dieser Parameter kann 0 sein. andernfalls ein oder mehrere der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="061c1-123">This parameter can be 0; otherwise, one or more of the following values.</span></span>



| <span data-ttu-id="061c1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="061c1-124">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="061c1-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="061c1-125">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <span data-ttu-id="061c1-126"><dt>**RMF \_ NULL**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="061c1-126"><dt>**RMF\_ZEROCURSOR**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="061c1-127">Legt den Cursor in der Mitte des Bereichs fest, der in der **Volksrepublik China** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="061c1-127">Sets the cursor in the center of the area specified in **prc**.</span></span> <span data-ttu-id="061c1-128">Wenn dieses Flag nicht angegeben wird, bleibt die Cursorposition unverändert.</span><span class="sxs-lookup"><span data-stu-id="061c1-128">If this flag is not specified, the cursor position remains unchanged.</span></span><br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <span data-ttu-id="061c1-129"><dt>**RMF \_ Verticalonly**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="061c1-129"><dt>**RMF\_VERTICALONLY**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="061c1-130">Ermöglicht nur das vertikale Scrollen.</span><span class="sxs-lookup"><span data-stu-id="061c1-130">Allows only vertical scrolling.</span></span><br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <span data-ttu-id="061c1-131"><dt>**RMF \_ Horizontalonly**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="061c1-131"><dt>**RMF\_HORIZONTALONLY**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="061c1-132">Ermöglicht nur horizontales Scrollen.</span><span class="sxs-lookup"><span data-stu-id="061c1-132">Allows only horizontal scrolling.</span></span><br/>                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="061c1-133">**PRC**</span><span class="sxs-lookup"><span data-stu-id="061c1-133">**prc**</span></span>
</dt> <dd>

<span data-ttu-id="061c1-134">Typ: **lprect**</span><span class="sxs-lookup"><span data-stu-id="061c1-134">Type: **LPRECT**</span></span>

</dd> <dd>

<span data-ttu-id="061c1-135">Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die den scrollbereich im Fenster "Lesemodus" angibt.</span><span class="sxs-lookup"><span data-stu-id="061c1-135">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the scrolling area in the reader mode window.</span></span> <span data-ttu-id="061c1-136">Wenn dieser Member **null** ist, wird das gesamte Fenster als scrollbereich verwendet.</span><span class="sxs-lookup"><span data-stu-id="061c1-136">If this member is **NULL**, then the entire window is used as the scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="061c1-137">**pfnscroll**</span><span class="sxs-lookup"><span data-stu-id="061c1-137">**pfnScroll**</span></span>
</dt> <dd>

<span data-ttu-id="061c1-138">Typ: **pfnreaderscroll**</span><span class="sxs-lookup"><span data-stu-id="061c1-138">Type: **PFNREADERSCROLL**</span></span>

</dd> <dd>

<span data-ttu-id="061c1-139">Ein Zeiger auf eine Anwendungs definierte [*readerscroll*](readerscroll.md) -Rückruffunktion, mit der die Anwendung benachrichtigt wird, dass das Fenster in einer bestimmten Richtung gescrollt werden muss.</span><span class="sxs-lookup"><span data-stu-id="061c1-139">A pointer to an application-defined [*ReaderScroll*](readerscroll.md) callback function used to notify the application that the window needs to be scrolled in a particular direction.</span></span>

</dd> <dt>

<span data-ttu-id="061c1-140">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="061c1-140">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="061c1-141">Typ: **pfnreadertranslatedispatch**</span><span class="sxs-lookup"><span data-stu-id="061c1-141">Type: **PFNREADERTRANSLATEDISPATCH**</span></span>

</dd> <dd>

<span data-ttu-id="061c1-142">Ein Zeiger auf eine Anwendungs definierte [*translatedispatch*](translatedispatch.md) -Rückruffunktion, die verwendet wird, um die erste Benachrichtigung über alle an das Fenster des Lesemodus gesendeten Nachrichten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="061c1-142">A pointer to an application-defined [*TranslateDispatch*](translatedispatch.md) callback function used to get first notification of any messages sent to the reader mode window.</span></span>

</dd> <dt>

<span data-ttu-id="061c1-143">**lParam**</span><span class="sxs-lookup"><span data-stu-id="061c1-143">**lParam**</span></span>
</dt> <dd>

<span data-ttu-id="061c1-144">Typ: **[ **LPARAM**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="061c1-144">Type: **[**LPARAM**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="061c1-145">Zusätzliche Informationen, die von der Anwendung benötigt werden, die vom Aufrufer in der [*readerscroll*](readerscroll.md) -Rückruffunktion gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="061c1-145">Additional information as needed by the application, read by the caller in the [*ReaderScroll*](readerscroll.md) callback function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="061c1-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="061c1-146">Remarks</span></span>

<span data-ttu-id="061c1-147">Diese Struktur ist in keinem öffentlichen Header deklariert.</span><span class="sxs-lookup"><span data-stu-id="061c1-147">This structure is not declared in any public header.</span></span> <span data-ttu-id="061c1-148">Um es zu verwenden, müssen Sie die oben gezeigte Deklaration in ihren eigenen Header einschließen.</span><span class="sxs-lookup"><span data-stu-id="061c1-148">To use it, you must include the declaration shown above in your own header.</span></span>

## <a name="requirements"></a><span data-ttu-id="061c1-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="061c1-149">Requirements</span></span>



| <span data-ttu-id="061c1-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="061c1-150">Requirement</span></span> | <span data-ttu-id="061c1-151">Wert</span><span class="sxs-lookup"><span data-stu-id="061c1-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="061c1-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="061c1-152">Minimum supported client</span></span><br/> | <span data-ttu-id="061c1-153">Nur Windows Vista, Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="061c1-153">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="061c1-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="061c1-154">Minimum supported server</span></span><br/> | <span data-ttu-id="061c1-155">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="061c1-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

