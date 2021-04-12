---
title: TBN_GETBUTTONINFO Benachrichtigungs Code (kommctrl. h)
description: Ruft Informationen zur Symbolleisten Anpassung ab und benachrichtigt das übergeordnete Fenster der Symbolleiste über alle Änderungen, die an der Symbolleiste vorgenommen werden. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- Windows-Steuerelemente für TBN_GETBUTTONINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956873"
---
# <a name="tbn_getbuttoninfo-notification-code"></a><span data-ttu-id="f6472-105">TBN- \_ getbuttoninfo-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="f6472-105">TBN\_GETBUTTONINFO notification code</span></span>

<span data-ttu-id="f6472-106">Ruft Informationen zur Symbolleisten Anpassung ab und benachrichtigt das übergeordnete Fenster der Symbolleiste über alle Änderungen, die an der Symbolleiste vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="f6472-106">Retrieves toolbar customization information and notifies the toolbar's parent window of any changes being made to the toolbar.</span></span> <span data-ttu-id="f6472-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="f6472-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="f6472-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6472-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6472-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6472-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6472-110">Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f6472-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="f6472-111">Das **iItem-Element** gibt einen NULL basierten Index an, der die Anzahl der Schaltflächen bereitstellt. das Dialogfeld Symbolleiste anpassen wird sowohl als verfügbar als auch auf der Symbolleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f6472-111">The **iItem** member specifies a zero-based index that provides a count of the buttons the Customize Toolbar dialog box displays as both available and present on the toolbar.</span></span> <span data-ttu-id="f6472-112">Der **pszText** -Member gibt die Adresse des aktuellen Schaltflächen Texts an, und **cchtext** gibt seine Länge in Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="f6472-112">The **pszText** member specifies the address of the current button text, and **cchText** specifies its length in characters.</span></span> <span data-ttu-id="f6472-113">Die Anwendung sollte die Struktur mit Informationen über die Schaltfläche Auffüllen.</span><span class="sxs-lookup"><span data-stu-id="f6472-113">The application should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6472-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6472-114">Return value</span></span>

<span data-ttu-id="f6472-115">Gibt **true** zurück, wenn Schaltflächen Informationen in die angegebene-Struktur kopiert wurden, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="f6472-115">Returns **TRUE** if button information was copied to the specified structure, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6472-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6472-116">Remarks</span></span>

<span data-ttu-id="f6472-117">Das Symbolleisten-Steuerelement ordnet einen Puffer zu, und der Empfänger (übergeordnetes Fenster) muss den Text in diesen Puffer kopieren.</span><span class="sxs-lookup"><span data-stu-id="f6472-117">The toolbar control allocates a buffer, and the receiver (parent window) must copy the text into that buffer.</span></span> <span data-ttu-id="f6472-118">Der **cchtext** -Member enthält die Länge des Puffers, der von der Symbolleiste zugewiesen wird, wenn TBN \_ getbuttoninfo an das übergeordnete Fenster gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="f6472-118">The **cchText** member contains the length of the buffer allocated by the toolbar when TBN\_GETBUTTONINFO is sent to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6472-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6472-119">Requirements</span></span>



| <span data-ttu-id="f6472-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6472-120">Requirement</span></span> | <span data-ttu-id="f6472-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f6472-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6472-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6472-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f6472-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6472-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6472-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6472-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f6472-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6472-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6472-126">Header</span><span class="sxs-lookup"><span data-stu-id="f6472-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6472-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6472-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f6472-128">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="f6472-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f6472-129">**TBN \_ Getbuttoninfow** (Unicode) und **TBN \_ getbuttoninfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f6472-129">**TBN\_GETBUTTONINFOW** (Unicode) and **TBN\_GETBUTTONINFOA** (ANSI)</span></span><br/>       |



 

 





