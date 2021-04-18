---
description: Die isvaliddevmode-Funktion überprüft, ob der Inhalt einer DEVMODE-Struktur gültig ist.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: Isvaliddevmode-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352732"
---
# <a name="isvaliddevmode-function"></a><span data-ttu-id="5db35-103">Isvaliddevmode-Funktion</span><span class="sxs-lookup"><span data-stu-id="5db35-103">IsValidDevmode function</span></span>

<span data-ttu-id="5db35-104">Die **isvaliddevmode** -Funktion überprüft, ob der Inhalt einer DEVMODE-Struktur gültig ist.</span><span class="sxs-lookup"><span data-stu-id="5db35-104">The **IsValidDevmode** function verifies that the contents of a DEVMODE structure are valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="5db35-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5db35-105">Syntax</span></span>


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a><span data-ttu-id="5db35-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5db35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5db35-107">*pdevmode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5db35-107">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5db35-108">Ein Zeiger auf den zu validierenden [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="5db35-108">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to validate.</span></span>

</dd> <dt>

<span data-ttu-id="5db35-109">*Devmudesize*</span><span class="sxs-lookup"><span data-stu-id="5db35-109">*DevmodeSize*</span></span> 
</dt> <dd>

<span data-ttu-id="5db35-110">Die Größe des Eingabe Byte Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5db35-110">The size in bytes of the input byte buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5db35-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5db35-111">Return value</span></span>

<span data-ttu-id="5db35-112">**True**, wenn der [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) -Wert strukturell gültig ist.</span><span class="sxs-lookup"><span data-stu-id="5db35-112">**TRUE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is structurally valid.</span></span> <span data-ttu-id="5db35-113">Wenn kleinere Fehler gefunden werden, werden Sie von der Funktion behoben und **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5db35-113">If minor errors are found the function will fix them and return **TRUE**.</span></span>

<span data-ttu-id="5db35-114">**False**, wenn der [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) ein oder mehrere bedeutende strukturellen Probleme aufweist.</span><span class="sxs-lookup"><span data-stu-id="5db35-114">**FALSE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) has one or more significant structural problems.</span></span> <span data-ttu-id="5db35-115">Beispielsweise ist der **dmsize** -Member falsch ausgerichtet oder gibt einen zu kleinen Puffer an.</span><span class="sxs-lookup"><span data-stu-id="5db35-115">For example, its **dmSize** member is misaligned or specifies a buffer that is too small.</span></span> <span data-ttu-id="5db35-116">Außerdem **false** , wenn **pdevmode** **null** ist.</span><span class="sxs-lookup"><span data-stu-id="5db35-116">Also, **FALSE** if **pDevmode** is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5db35-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5db35-117">Remarks</span></span>

<span data-ttu-id="5db35-118">Es werden keine privaten Druckertreiber Felder des [**DEVMODE-Modus**](/windows/win32/api/wingdi/ns-wingdi-devmodea) geprüft, sondern nur die öffentlichen Felder.</span><span class="sxs-lookup"><span data-stu-id="5db35-118">No private printer driver fields of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) are checked, only the public fields.</span></span>

<span data-ttu-id="5db35-119">Aufrufer sollten **dmsize** + **dmdriverextra** für **devmudesize** nur verwenden, wenn Sie sicherstellen können, dass die Eingabepuffergröße mindestens so groß ist.</span><span class="sxs-lookup"><span data-stu-id="5db35-119">Callers should use **dmSize**+**dmDriverExtra** for **DevmodeSize** only if they can guarantee that the input buffer size is at least that big.</span></span> <span data-ttu-id="5db35-120">Da es sich bei [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) im Allgemeinen um nicht vertrauenswürdige Daten handelt, sind die Werte, die im Eingabepuffer in den Offsets **dmsize** und **dmdriverextra** liegen, ebenfalls nicht vertrauenswürdig.</span><span class="sxs-lookup"><span data-stu-id="5db35-120">Since the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is generally untrusted data, the values that are in the input buffer at the **dmSize** and **dmDriverExtra** offsets are also untrusted.</span></span>

<span data-ttu-id="5db35-121">Diese Funktion ist im Lua-Kontext (Least-Privileged User Account) ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="5db35-121">This function is executable in Least-Privileged User Account (LUA) context.</span></span>

## <a name="requirements"></a><span data-ttu-id="5db35-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5db35-122">Requirements</span></span>



| <span data-ttu-id="5db35-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5db35-123">Requirement</span></span> | <span data-ttu-id="5db35-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5db35-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5db35-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5db35-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5db35-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5db35-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5db35-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5db35-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5db35-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5db35-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5db35-129">Header</span><span class="sxs-lookup"><span data-stu-id="5db35-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5db35-130"><dt>Winspool. h</dt></span><span class="sxs-lookup"><span data-stu-id="5db35-130"><dt>Winspool.h</dt></span></span> </dl>   |
| <span data-ttu-id="5db35-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5db35-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="5db35-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5db35-132"><dt>Winspool.lib</dt></span></span> </dl> |
| <span data-ttu-id="5db35-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5db35-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5db35-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="5db35-134"><dt>Winspool.drv</dt></span></span> </dl> |
| <span data-ttu-id="5db35-135">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="5db35-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5db35-136">**Isvaliddevmodew** (Unicode) und **isvaliddevmodea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5db35-136">**IsValidDevmodeW** (Unicode) and **IsValidDevmodeA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="5db35-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5db35-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db35-138">Drucken</span><span class="sxs-lookup"><span data-stu-id="5db35-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="5db35-139">Druckspooler-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="5db35-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="5db35-140">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="5db35-140">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




