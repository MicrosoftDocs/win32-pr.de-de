---
title: Translatedispatch-Rückruffunktion
description: Wird vom Client der doreadermode-Funktion zum Abfangen und expliziten verarbeiten von Windows-Meldungen verwendet, die für den scrollbereich des Fensters "Lesemodus" bestimmt sind. Dies ist eine Anwendungs definierte Rückruffunktion.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- Windows-Steuerelemente für translatedispatch-Rückruf Funktionen
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1230ed1e65f8d739f9a0a05e4788eb919c45c4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949767"
---
# <a name="translatedispatch-callback-function"></a><span data-ttu-id="257f3-105">Translatedispatch-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="257f3-105">TranslateDispatch callback function</span></span>

<span data-ttu-id="257f3-106">\[*Translatedispatch* ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="257f3-106">\[*TranslateDispatch* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="257f3-107">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="257f3-107">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="257f3-108">Wird vom Client der [**doreadermode**](doreadermode.md) -Funktion zum Abfangen und expliziten verarbeiten von Windows-Meldungen verwendet, die für den scrollbereich des Fensters "Lesemodus" bestimmt sind.</span><span class="sxs-lookup"><span data-stu-id="257f3-108">Used by the client of the [**DoReaderMode**](doreadermode.md) function to intercept and explicitly handle any windows messages targeted for the scrolling area of the reader mode window.</span></span> <span data-ttu-id="257f3-109">Dies ist eine Anwendungs definierte Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="257f3-109">This is an application-defined callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="257f3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="257f3-110">Syntax</span></span>


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a><span data-ttu-id="257f3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="257f3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="257f3-112">*lpmsg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="257f3-112">*lpmsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="257f3-113">Typ: \* Konstante *[**msg**](/windows/win32/api/winuser/ns-winuser-msg) \** _</span><span class="sxs-lookup"><span data-stu-id="257f3-113">Type: \**const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg)\** _</span></span>

<span data-ttu-id="257f3-114">Ein Zeiger auf eine [_ *msg* \*](/windows/win32/api/winuser/ns-winuser-msg) -Struktur, die die abgefangene Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="257f3-114">A pointer to an [_ *MSG*\*](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the intercepted message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="257f3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="257f3-115">Return value</span></span>

<span data-ttu-id="257f3-116">Typ: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="257f3-116">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="257f3-117">**True** , wenn die Meldung von dieser Funktion behandelt wurde. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="257f3-117">**TRUE** if the message was handled by this function; otherwise, **FALSE**.</span></span> <span data-ttu-id="257f3-118">Wenn der Wert **false** ist, wird die Nachricht von der Standard Implementierung des Lesemodus verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="257f3-118">If **FALSE**, the message is handled by the default reader mode implementation.</span></span> <span data-ttu-id="257f3-119">Diese Implementierung behandelt die Mausbewegung und Schaltflächen sowie Tastendruck.</span><span class="sxs-lookup"><span data-stu-id="257f3-119">That implementation handles mouse movement and buttons as well as key presses.</span></span>

## <a name="examples"></a><span data-ttu-id="257f3-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="257f3-120">Examples</span></span>

<span data-ttu-id="257f3-121">Im folgenden Beispiel wird eine Implementierung dieser Funktion beschrieben.</span><span class="sxs-lookup"><span data-stu-id="257f3-121">The following example outlines an implementation of this function.</span></span>


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a><span data-ttu-id="257f3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="257f3-122">Requirements</span></span>



| <span data-ttu-id="257f3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="257f3-123">Requirement</span></span> | <span data-ttu-id="257f3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="257f3-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="257f3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="257f3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="257f3-126">Nur Windows Vista, Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="257f3-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="257f3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="257f3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="257f3-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="257f3-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

