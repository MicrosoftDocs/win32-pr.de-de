---
title: MCIWNDM_SENDSTRING Meldung (VFW. h)
description: Die mciwndm \_ sendstring-Nachricht sendet einen MCI-Befehl in Form einer Zeichenfolge an das Gerät, das dem mciwnd-Fenster zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des mciwndsendstring-Makros senden.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- MCIWNDM_SENDSTRING-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742488"
---
# <a name="mciwndm_sendstring-message"></a><span data-ttu-id="5a010-105">Mciwndm \_ sendstring-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5a010-105">MCIWNDM\_SENDSTRING message</span></span>

<span data-ttu-id="5a010-106">Die **mciwndm \_ sendstring** -Nachricht sendet einen MCI-Befehl in Form einer Zeichenfolge an das Gerät, das dem mciwnd-Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5a010-106">The **MCIWNDM\_SENDSTRING** message sends an MCI command in string form to the device associated with the MCIWnd window.</span></span> <span data-ttu-id="5a010-107">Sie können diese Nachricht explizit oder mithilfe des [**mciwndsendstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="5a010-107">You can send this message explicitly or by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro.</span></span>


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a><span data-ttu-id="5a010-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a010-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a010-109"><span id="sz"></span><span id="SZ"></span>*RT*</span><span class="sxs-lookup"><span data-stu-id="5a010-109"><span id="sz"></span><span id="SZ"></span>*sz*</span></span>
</dt> <dd>

<span data-ttu-id="5a010-110">Zeichen folgen Befehl, der an das MCI-Gerät gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5a010-110">String command to send to the MCI device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a010-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a010-111">Return Value</span></span>

<span data-ttu-id="5a010-112">Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="5a010-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a010-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a010-113">Remarks</span></span>

<span data-ttu-id="5a010-114">Der Nachrichten Handler für **mciwndm \_ sendstring** fügt einen Gerätealias an den MCI-Befehl an, den Sie an das Gerät senden.</span><span class="sxs-lookup"><span data-stu-id="5a010-114">The message handler for **MCIWNDM\_SENDSTRING** appends a device alias to the MCI command you send to the device.</span></span> <span data-ttu-id="5a010-115">Daher sollten Sie in einem MCI-Befehl, den Sie mit **mciwndm \_ sendstring** ausgeben, keinen Alias verwenden.</span><span class="sxs-lookup"><span data-stu-id="5a010-115">Therefore, you should not use any alias in an MCI command that you issue with **MCIWNDM\_SENDSTRING**.</span></span>

<span data-ttu-id="5a010-116">Um die Rückgabe Zeichenfolge, die das Ergebnis des Befehls enthält, zu erhalten, senden Sie die [**mciwndm-Nachricht " \_ returnstring**](mciwndm-returnstring.md) ".</span><span class="sxs-lookup"><span data-stu-id="5a010-116">To get the return string, which contains the result of the command, send the [**MCIWNDM\_RETURNSTRING**](mciwndm-returnstring.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a010-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a010-117">Requirements</span></span>



| <span data-ttu-id="5a010-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a010-118">Requirement</span></span> | <span data-ttu-id="5a010-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5a010-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5a010-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5a010-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5a010-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a010-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5a010-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5a010-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5a010-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5a010-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5a010-124">Header</span><span class="sxs-lookup"><span data-stu-id="5a010-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a010-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a010-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a010-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a010-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a010-127">**Mciwndsendstring**</span><span class="sxs-lookup"><span data-stu-id="5a010-127">**MCIWndSendString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[<span data-ttu-id="5a010-128">Multimediaregister</span><span class="sxs-lookup"><span data-stu-id="5a010-128">Multimedia Command Strings</span></span>](multimedia-command-strings.md)
</dt> </dl>

 

 





