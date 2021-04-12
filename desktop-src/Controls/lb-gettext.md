---
title: LB_GETTEXT Meldung (Winuser. h)
description: Ruft eine Zeichenfolge aus einem Listenfeld ab.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- Windows-Steuerelemente für LB_GETTEXT Meldung
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dd5e2c7a9e6c1c1aa1b847592555a013766134
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478258"
---
# <a name="lb_gettext-message"></a><span data-ttu-id="933da-104">LB- \_ gettext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="933da-104">LB\_GETTEXT message</span></span>

<span data-ttu-id="933da-105">Ruft eine Zeichenfolge aus einem Listenfeld ab.</span><span class="sxs-lookup"><span data-stu-id="933da-105">Gets a string from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="933da-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="933da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="933da-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="933da-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="933da-108">Der null basierte Index der abzurufenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="933da-108">The zero-based index of the string to retrieve.</span></span>

<span data-ttu-id="933da-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt.</span><span class="sxs-lookup"><span data-stu-id="933da-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="933da-110">Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen.</span><span class="sxs-lookup"><span data-stu-id="933da-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="933da-111">Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.</span><span class="sxs-lookup"><span data-stu-id="933da-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="933da-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="933da-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="933da-113">Ein Zeiger auf den Puffer, der die Zeichenfolge empfängt. der Typ ist **LPTSTR** , der anschließend in ein **LPARAM** umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="933da-113">A pointer to the buffer that will receive the string; it is type **LPTSTR** which is subsequently cast to an **LPARAM**.</span></span> <span data-ttu-id="933da-114">Der Puffer muss über ausreichend Speicherplatz für die Zeichenfolge und ein abschließendes NULL-Zeichen verfügen.</span><span class="sxs-lookup"><span data-stu-id="933da-114">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="933da-115">Eine [**lb- \_ gettextlen**](lb-gettextlen.md) -Nachricht kann vor der **lb- \_ gettext** -Nachricht gesendet werden, um die Länge der Zeichenfolge in **TCHAR** s abzurufen.</span><span class="sxs-lookup"><span data-stu-id="933da-115">An [**LB\_GETTEXTLEN**](lb-gettextlen.md) message can be sent before the **LB\_GETTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="933da-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="933da-116">Return value</span></span>

<span data-ttu-id="933da-117">Der Rückgabewert ist die Länge der Zeichenfolge in **TCHAR** s, wobei das abschließende Null-Zeichen ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="933da-117">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="933da-118">Wenn von *wParam* kein gültiger Index angegeben wird, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="933da-118">If *wParam* does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="933da-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="933da-119">Remarks</span></span>

<span data-ttu-id="933da-120">Wenn im Listenfeld ein vom Besitzer gezeichneter Stil, aber nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, erhält der Puffer, auf den der *LPARAM* -Parameter verweist, den Wert, der dem Element zugeordnet ist (die Elementdaten).</span><span class="sxs-lookup"><span data-stu-id="933da-120">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the buffer pointed to by the *lParam* parameter receives the value associated with the item (the item data).</span></span>

## <a name="requirements"></a><span data-ttu-id="933da-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="933da-121">Requirements</span></span>



| <span data-ttu-id="933da-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="933da-122">Requirement</span></span> | <span data-ttu-id="933da-123">Wert</span><span class="sxs-lookup"><span data-stu-id="933da-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="933da-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="933da-124">Minimum supported client</span></span><br/> | <span data-ttu-id="933da-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="933da-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="933da-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="933da-126">Minimum supported server</span></span><br/> | <span data-ttu-id="933da-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="933da-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="933da-128">Header</span><span class="sxs-lookup"><span data-stu-id="933da-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="933da-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="933da-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="933da-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="933da-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="933da-131">**LB- \_ gettextlen**</span><span class="sxs-lookup"><span data-stu-id="933da-131">**LB\_GETTEXTLEN**</span></span>](lb-gettextlen.md)
</dt> </dl>

 

 





