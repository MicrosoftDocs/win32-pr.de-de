---
title: LB_ADDFILE Meldung (Winuser. h)
description: Fügt den angegebenen Dateinamen zu einem Listenfeld hinzu, das eine Verzeichnisliste enthält.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- Windows-Steuerelemente für LB_ADDFILE Meldung
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b3d66c6a6c8495c67df2078370911ca9cd31df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478261"
---
# <a name="lb_addfile-message"></a><span data-ttu-id="86d4e-104">LB- \_ AddFile-Nachricht</span><span class="sxs-lookup"><span data-stu-id="86d4e-104">LB\_ADDFILE message</span></span>

<span data-ttu-id="86d4e-105">Fügt den angegebenen Dateinamen zu einem Listenfeld hinzu, das eine Verzeichnisliste enthält.</span><span class="sxs-lookup"><span data-stu-id="86d4e-105">Adds the specified filename to a list box that contains a directory listing.</span></span>

## <a name="parameters"></a><span data-ttu-id="86d4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="86d4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86d4e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86d4e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86d4e-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="86d4e-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="86d4e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86d4e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86d4e-110">Ein Zeiger auf einen Puffer, der den Namen der hinzu zufügenden Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="86d4e-110">A pointer to a buffer that specifies the name of the file to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86d4e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86d4e-111">Return value</span></span>

<span data-ttu-id="86d4e-112">Der Rückgabewert ist der null basierte Index der Datei, die hinzugefügt wurde, oder lb- \_ Err, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="86d4e-112">The return value is the zero-based index of the file that was added, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="86d4e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86d4e-113">Remarks</span></span>

<span data-ttu-id="86d4e-114">Das Listenfeld, dem *LPARAM* hinzugefügt wird, muss von der [**dlgdirlist**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) -Funktion ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="86d4e-114">The list box to which *lParam* is added must have been filled by the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function.</span></span>

<span data-ttu-id="86d4e-115">Die " [**lb- \_ InitStorage**](lb-initstorage.md) "-Nachricht beschleunigt die Initialisierung von Listenfeldern, die über eine große Anzahl von Elementen (mehr als 100) verfügen.</span><span class="sxs-lookup"><span data-stu-id="86d4e-115">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="86d4e-116">Sie reserviert die angegebene Menge an Arbeitsspeicher, sodass nachfolgende **lb- \_ AddFile** -Nachrichten die kürzeste Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="86d4e-116">It reserves the specified amount of memory so that subsequent **LB\_ADDFILE** messages take the shortest possible time.</span></span> <span data-ttu-id="86d4e-117">Sie können Schätzwerte für den *wParam* -Parameter und den *LPARAM* -Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="86d4e-117">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="86d4e-118">Wenn Sie den Wert überschätzen, wird der zusätzliche Arbeitsspeicher zugeordnet. Wenn Sie unterschätzen, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.</span><span class="sxs-lookup"><span data-stu-id="86d4e-118">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="86d4e-119">Für eine ANSI-Anwendung konvertiert das System den Text in einem Listenfeld mithilfe von CP ACP in Unicode \_ .</span><span class="sxs-lookup"><span data-stu-id="86d4e-119">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="86d4e-120">Dies kann zu Problemen führen.</span><span class="sxs-lookup"><span data-stu-id="86d4e-120">This can cause problems.</span></span> <span data-ttu-id="86d4e-121">Beispielsweise werden Zeichen mit untergeordneten Zeichen in einem nicht-Unicode-Listenfeld in einem japanischen Fenster gegartet.</span><span class="sxs-lookup"><span data-stu-id="86d4e-121">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="86d4e-122">Um dieses Problem zu beheben, kompilieren Sie die Anwendung entweder als Unicode, oder verwenden Sie ein vom Besitzer gezeichnetes Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="86d4e-122">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="86d4e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86d4e-123">Requirements</span></span>



| <span data-ttu-id="86d4e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86d4e-124">Requirement</span></span> | <span data-ttu-id="86d4e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="86d4e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86d4e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86d4e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="86d4e-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86d4e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="86d4e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86d4e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="86d4e-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86d4e-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="86d4e-130">Header</span><span class="sxs-lookup"><span data-stu-id="86d4e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="86d4e-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="86d4e-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86d4e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86d4e-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="86d4e-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="86d4e-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="86d4e-134">**Dlgdirlist**</span><span class="sxs-lookup"><span data-stu-id="86d4e-134">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[<span data-ttu-id="86d4e-135">**LB- \_ AddString**</span><span class="sxs-lookup"><span data-stu-id="86d4e-135">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> </dl>

 

 





