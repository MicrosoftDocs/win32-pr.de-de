---
title: CB_GETCUEBANNER Meldung (Winuser. h)
description: Ruft den Hinweis Banner Text ab, der im Bearbeitungs Steuerelement eines Kombinations Felds angezeigt wird. Senden Sie diese Nachricht explizit oder mithilfe des ComboBox \_ getcuebannertext-Makros.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- Windows-Steuerelemente für CB_GETCUEBANNER Meldung
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f51df0083c4cd72c3f34bb3ce045e0f577a24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859019"
---
# <a name="cb_getcuebanner-message"></a><span data-ttu-id="b6aa7-105">CB \_ getcuebanner-Meldung</span><span class="sxs-lookup"><span data-stu-id="b6aa7-105">CB\_GETCUEBANNER message</span></span>

<span data-ttu-id="b6aa7-106">Ruft den Hinweis Banner Text ab, der im Bearbeitungs Steuerelement eines Kombinations Felds angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-106">Gets the cue banner text displayed in the edit control of a combo box.</span></span> <span data-ttu-id="b6aa7-107">Senden Sie diese Nachricht explizit oder mithilfe des [**ComboBox \_ getcuebannertext**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) -Makros.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-107">Send this message explicitly or by using the [**ComboBox\_GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6aa7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6aa7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6aa7-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6aa7-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6aa7-110">Ein Zeiger auf einen Unicode-Zeichen folgen Puffer, der den Hinweis Banner Text empfängt.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-110">A pointer to a Unicode string buffer that receives the cue banner text.</span></span> <span data-ttu-id="b6aa7-111">Die aufrufenden Anwendung ist dafür verantwortlich, den Speicher für den Puffer zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-111">The calling application is responsible for allocating the memory for the buffer.</span></span> <span data-ttu-id="b6aa7-112">Die Puffergröße muss gleich der Länge der Hinweis Banner Zeichenfolge in **WCHARs** Plus 1 für das abschließende Null-  **WCHAR** sein.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-112">The buffer size must be equal to the length of the cue banner string in **WCHARs**, plus 1 for the terminating **NULL** **WCHAR**.</span></span>

</dd> <dt>

<span data-ttu-id="b6aa7-113">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6aa7-113">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6aa7-114">Die Größe des Puffers, auf den von *lpcwtext* in **WCHARs** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-114">The size of the buffer pointed to by *lpcwText* in **WCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6aa7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b6aa7-115">Return value</span></span>

<span data-ttu-id="b6aa7-116">Gibt 1 zurück, wenn erfolgreich, oder andernfalls einen Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-116">Returns 1 if successful, or an error value otherwise.</span></span>

<span data-ttu-id="b6aa7-117">Wenn kein Hinweis Banner Text vorhanden ist, ist der Rückgabewert 0.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-117">If there is no cue banner text to get, the return value is 0.</span></span> <span data-ttu-id="b6aa7-118">Wenn die aufrufende Anwendung keinen Puffer zuweist oder *LPARAM* vor dem Senden dieser Nachricht festgelegt wird, kann es zu einem nicht definierten Verhalten kommen, und der Rückgabewert ist möglicherweise nicht zuverlässig.</span><span class="sxs-lookup"><span data-stu-id="b6aa7-118">If the calling application fails to allocate a buffer, or set *lParam* before sending this message, undefined behavior may result and the return value may not be reliable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6aa7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b6aa7-119">Requirements</span></span>



| <span data-ttu-id="b6aa7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b6aa7-120">Requirement</span></span> | <span data-ttu-id="b6aa7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b6aa7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6aa7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b6aa7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b6aa7-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6aa7-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6aa7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b6aa7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b6aa7-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b6aa7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6aa7-126">Header</span><span class="sxs-lookup"><span data-stu-id="b6aa7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6aa7-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6aa7-127"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6aa7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b6aa7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6aa7-129">Kombinations Feld-Features</span><span class="sxs-lookup"><span data-stu-id="b6aa7-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





