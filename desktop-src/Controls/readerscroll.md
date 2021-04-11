---
title: Readerscroll-Rückruffunktion
description: Eine von der Anwendung definierte Rückruffunktion, die verwendet wird, wenn der Mauszeiger in den Teil des lesemodusfensters verschoben wird, der als aktiver scrollbereich deklariert wurde.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- Windows-Steuerelemente für readerscroll-Rückruf Funktionen
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949815"
---
# <a name="readerscroll-callback-function"></a><span data-ttu-id="afc6d-104">Readerscroll-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="afc6d-104">ReaderScroll callback function</span></span>

<span data-ttu-id="afc6d-105">\[*Readerscroll* ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="afc6d-105">\[*ReaderScroll* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="afc6d-106">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="afc6d-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="afc6d-107">Eine von der Anwendung definierte Rückruffunktion, die verwendet wird, wenn der Mauszeiger in den Teil des lesemodusfensters verschoben wird, der als aktiver scrollbereich deklariert wurde.</span><span class="sxs-lookup"><span data-stu-id="afc6d-107">An application-defined callback function used when the mouse pointer is moved within the portion of the reader mode window that has been declared as the active scrolling area.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc6d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="afc6d-108">Syntax</span></span>


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a><span data-ttu-id="afc6d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="afc6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc6d-110">*prmi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afc6d-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc6d-111">Typ: **preadermodeinfo**</span><span class="sxs-lookup"><span data-stu-id="afc6d-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="afc6d-112">Ein Zeiger auf die [**readermodumfo**](readermodeinfo.md) -Struktur, die an die [**doreadermode**](doreadermode.md) -Funktion weitergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="afc6d-112">A pointer to the [**READERMODEINFO**](readermodeinfo.md) structure that was passed to the [**DoReaderMode**](doreadermode.md) function.</span></span> <span data-ttu-id="afc6d-113">Diese Struktur definiert das Fenster Lesemodus und den aktiven scrollbereich.</span><span class="sxs-lookup"><span data-stu-id="afc6d-113">This structure defines the reader mode window and the active scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="afc6d-114">*DX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afc6d-114">*dx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc6d-115">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="afc6d-115">Type: **int**</span></span>

<span data-ttu-id="afc6d-116">Der Abstand, der horizontal durchlaufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="afc6d-116">The distance to scroll horizontally.</span></span> <span data-ttu-id="afc6d-117">Wenn das RMF \_ verticalonly-Flag in der [**readermodeinfo**](readermodeinfo.md) -Struktur festgelegt ist, ist dieser Wert immer 0.</span><span class="sxs-lookup"><span data-stu-id="afc6d-117">If the RMF\_VERTICALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> <dt>

<span data-ttu-id="afc6d-118">*dy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afc6d-118">*dy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc6d-119">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="afc6d-119">Type: **int**</span></span>

<span data-ttu-id="afc6d-120">Der Abstand, der vertikal durchlaufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="afc6d-120">The distance to scroll vertically.</span></span> <span data-ttu-id="afc6d-121">Wenn das RMF- \_ Flag horizontalonly in der [**readermodeinfo**](readermodeinfo.md) -Struktur festgelegt ist, ist dieser Wert immer 0.</span><span class="sxs-lookup"><span data-stu-id="afc6d-121">If the RMF\_HORIZONTALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afc6d-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afc6d-122">Return value</span></span>

<span data-ttu-id="afc6d-123">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="afc6d-123">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="afc6d-124">Diese Funktion sollte immer **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="afc6d-124">This function should always return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="afc6d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afc6d-125">Remarks</span></span>

<span data-ttu-id="afc6d-126">Wenn die Anwendung eine Benachrichtigung von dieser Funktion empfängt, ist die Anwendung dafür verantwortlich, das Fenster des Lesemodus in der durch die *DX* -und *dy* -Parameter angegebenen Richtung zu scrollen.</span><span class="sxs-lookup"><span data-stu-id="afc6d-126">When the application receives notification from this function, the application is responsible for scrolling the reader mode window in the direction specified by the *dx* and *dy* parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="afc6d-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afc6d-127">Examples</span></span>

<span data-ttu-id="afc6d-128">Im folgenden Beispiel wird eine Implementierung dieser Funktion mithilfe einer benutzerdefinierten Funktion für den Bildlauf dargestellt.</span><span class="sxs-lookup"><span data-stu-id="afc6d-128">The following example outlines an implementation of this function using a custom function to accomplish the scrolling.</span></span>


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a><span data-ttu-id="afc6d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afc6d-129">Requirements</span></span>



| <span data-ttu-id="afc6d-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afc6d-130">Requirement</span></span> | <span data-ttu-id="afc6d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="afc6d-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="afc6d-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afc6d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="afc6d-133">Nur Windows Vista, Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc6d-133">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="afc6d-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afc6d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="afc6d-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc6d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

