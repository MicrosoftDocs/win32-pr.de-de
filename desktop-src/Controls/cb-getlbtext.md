---
title: CB_GETLBTEXT Meldung (Winuser. h)
description: Ruft eine Zeichenfolge aus der Liste eines Kombinations Felds ab.
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- Windows-Steuerelemente für CB_GETLBTEXT Meldung
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040601"
---
# <a name="cb_getlbtext-message"></a><span data-ttu-id="3dd25-104">CB \_ getlbtext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3dd25-104">CB\_GETLBTEXT message</span></span>

<span data-ttu-id="3dd25-105">Ruft eine Zeichenfolge aus der Liste eines Kombinations Felds ab.</span><span class="sxs-lookup"><span data-stu-id="3dd25-105">Gets a string from the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="3dd25-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dd25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dd25-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3dd25-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3dd25-108">Der null basierte Index der abzurufenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3dd25-108">The zero-based index of the string to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="3dd25-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3dd25-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3dd25-110">Ein Zeiger auf den Puffer, der die Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="3dd25-110">A pointer to the buffer that receives the string.</span></span> <span data-ttu-id="3dd25-111">Der Puffer muss über ausreichend Speicherplatz für die Zeichenfolge und ein abschließendes NULL-Zeichen verfügen.</span><span class="sxs-lookup"><span data-stu-id="3dd25-111">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="3dd25-112">Sie können eine [**CB \_ getlbtextlen**](cb-getlbtextlen.md) -Nachricht vor der **CB \_ getlbtext** -Nachricht senden, um die Länge der Zeichenfolge in **TCHAR** s abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3dd25-112">You can send a [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) message prior to the **CB\_GETLBTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span> <span data-ttu-id="3dd25-113">Wenn es sich um eine ANSI-Zeichenfolge handelt, ist dies die Anzahl von Bytes, aber wenn es sich um eine Unicode-Zeichenfolge handelt, ist dies die Anzahl der Zeichen</span><span class="sxs-lookup"><span data-stu-id="3dd25-113">If it is an ANSI string this is the number of bytes, but if it is a Unicode string this is the number of characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dd25-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3dd25-114">Return value</span></span>

<span data-ttu-id="3dd25-115">Der Rückgabewert ist die Länge der Zeichenfolge in **TCHAR** s, wobei das abschließende Null-Zeichen ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="3dd25-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="3dd25-116">Wenn von *wParam* kein gültiger Index angegeben wird, ist der Rückgabewert CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="3dd25-116">If *wParam* does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dd25-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3dd25-117">Remarks</span></span>

<span data-ttu-id="3dd25-118">**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit des Programms beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="3dd25-118">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="3dd25-119">Diese Meldung bietet keine Möglichkeit, die Größe des Puffers zu kennen.</span><span class="sxs-lookup"><span data-stu-id="3dd25-119">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="3dd25-120">Wenn Sie diese Meldung verwenden, rufen Sie zunächst [**CB \_ getlbtextlen**](cb-getlbtextlen.md) auf, um die erforderliche Anzahl von Zeichen abzurufen, und rufen Sie dann die Nachricht zum Abrufen der Zeichenfolge auf.</span><span class="sxs-lookup"><span data-stu-id="3dd25-120">If you use this message, first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="3dd25-121">Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="3dd25-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="3dd25-122">Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, empfängt der Puffer, auf den *LPARAM* verweist, die Daten, die dem Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3dd25-122">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the buffer pointed to by *lParam* receives the data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd25-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3dd25-123">Requirements</span></span>



| <span data-ttu-id="3dd25-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3dd25-124">Requirement</span></span> | <span data-ttu-id="3dd25-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3dd25-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd25-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3dd25-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd25-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dd25-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3dd25-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3dd25-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd25-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dd25-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3dd25-130">Header</span><span class="sxs-lookup"><span data-stu-id="3dd25-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dd25-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="3dd25-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd25-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dd25-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd25-133">**CB \_ getlbtextlen**</span><span class="sxs-lookup"><span data-stu-id="3dd25-133">**CB\_GETLBTEXTLEN**</span></span>](cb-getlbtextlen.md)
</dt> </dl>

 

 





