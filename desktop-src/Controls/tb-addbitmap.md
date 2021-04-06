---
title: TB_ADDBITMAP Meldung (kommstrg. h)
description: Fügt der Liste der für eine Symbolleiste verfügbaren Schaltflächen Bilder mindestens ein Bild hinzu.
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- Windows-Steuerelemente für TB_ADDBITMAP Meldung
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743969"
---
# <a name="tb_addbitmap-message"></a><span data-ttu-id="c1e85-104">TB \_ AddBitmap-Meldung</span><span class="sxs-lookup"><span data-stu-id="c1e85-104">TB\_ADDBITMAP message</span></span>

<span data-ttu-id="c1e85-105">Fügt der Liste der für eine Symbolleiste verfügbaren Schaltflächen Bilder mindestens ein Bild hinzu.</span><span class="sxs-lookup"><span data-stu-id="c1e85-105">Adds one or more images to the list of button images available for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1e85-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1e85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e85-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1e85-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1e85-108">Anzahl von Schaltflächen Bildern in der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="c1e85-108">Number of button images in the bitmap.</span></span> <span data-ttu-id="c1e85-109">Wenn *LPARAM* eine System definierte Bitmap angibt, wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c1e85-109">If *lParam* specifies a system-defined bitmap, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c1e85-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1e85-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1e85-111">Zeiger auf eine [**tbaddbitmap**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) -Struktur, die den Bezeichner einer Bitmapressource enthält, und das Handle für die Modul Instanz mit der ausführbaren Datei, die die Bitmap-Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="c1e85-111">Pointer to a [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) structure that contains the identifier of a bitmap resource and the handle to the module instance with the executable file that contains the bitmap resource.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e85-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1e85-112">Return value</span></span>

<span data-ttu-id="c1e85-113">Gibt den Index des ersten neuen Bilds zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="c1e85-113">Returns the index of the first new image if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1e85-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1e85-114">Remarks</span></span>

<span data-ttu-id="c1e85-115">Wenn die Symbolleiste mit [**der Funktion "**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) -Funktion" erstellt wurde, müssen Sie vor dem Senden von **TB \_ AddBitmap** die [**TB- \_ buttonstructsize**](tb-buttonstructsize.md) -Nachricht an die Symbolleiste senden.</span><span class="sxs-lookup"><span data-stu-id="c1e85-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBITMAP**.</span></span>

## <a name="examples"></a><span data-ttu-id="c1e85-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1e85-116">Examples</span></span>

<span data-ttu-id="c1e85-117">Im folgenden Beispiel wird eine Bitmap aus einer Ressource (IDB \_ bitmap1) erstellt, wobei die Hintergrundfarbe (in diesem Fall schwarz) der Vordergrundfarbe der System Schaltfläche zugeordnet und der Symbolleiste hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c1e85-117">The following example creates a bitmap from a resource (IDB\_BITMAP1), maps the background color (black in this case) to the system button face color, and adds it to the toolbar.</span></span>


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a><span data-ttu-id="c1e85-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1e85-118">Requirements</span></span>



| <span data-ttu-id="c1e85-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1e85-119">Requirement</span></span> | <span data-ttu-id="c1e85-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c1e85-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e85-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1e85-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c1e85-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1e85-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1e85-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1e85-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c1e85-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1e85-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1e85-125">Header</span><span class="sxs-lookup"><span data-stu-id="c1e85-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1e85-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1e85-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

