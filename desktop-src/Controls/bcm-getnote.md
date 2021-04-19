---
title: BCM_GETNOTE Meldung (kommstrg. h)
description: Ruft den Text des Notiz Texts ab, der einer Befehls Link Schaltfläche zugeordnet ist. Sie können diese Nachricht explizit senden oder das Schaltfläche \_ GetNote-Makro verwenden.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- Windows-Steuerelemente für BCM_GETNOTE Meldung
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 758dac90ba4c0f3087a6df90d9acf2c1321b1d73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345297"
---
# <a name="bcm_getnote-message"></a><span data-ttu-id="468ae-105">BCM \_ GetNote-Meldung</span><span class="sxs-lookup"><span data-stu-id="468ae-105">BCM\_GETNOTE message</span></span>

<span data-ttu-id="468ae-106">Ruft den Text des Notiz Texts ab, der einer Befehls Link Schaltfläche zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="468ae-106">Gets the text of the note associated with a command link button.</span></span> <span data-ttu-id="468ae-107">Sie können diese Nachricht explizit senden oder das [**Schaltfläche \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="468ae-107">You can send this message explicitly or use the [**Button\_GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="468ae-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="468ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="468ae-109">*wParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="468ae-109">*wParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="468ae-110">Ein **DWORD** , das die Größe des Puffers angibt, auf den *LPARAM* zeigt, in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="468ae-110">A **DWORD** that specifies the size of the buffer pointed to by *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="468ae-111">*LPARAM* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="468ae-111">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="468ae-112">Der Zeichen folgen Puffer, der den Text empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="468ae-112">The string buffer to receive the text.</span></span> <span data-ttu-id="468ae-113">Der Puffer muss groß genug sein, um das abschließende Null-Zeichen aufnehmen zu können.</span><span class="sxs-lookup"><span data-stu-id="468ae-113">The buffer must be large enough to accommodate the terminating NULL character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="468ae-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="468ae-114">Return value</span></span>

<span data-ttu-id="468ae-115">Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="468ae-115">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="468ae-116">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="468ae-116">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="468ae-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="468ae-117">Remarks</span></span>

<span data-ttu-id="468ae-118">Die **BCM \_ GetNote** -Nachricht funktioniert nur mit Schaltflächen, die den Schaltflächen Stil " [**SB \_ CommandLink**](button-styles.md) " oder " [**b" \_ defcommandlink**](button-styles.md) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="468ae-118">The **BCM\_GETNOTE** message works only with buttons that have the [**BS\_COMMANDLINK**](button-styles.md) or [**BS\_DEFCOMMANDLINK**](button-styles.md) button style.</span></span>

<span data-ttu-id="468ae-119">" [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) " enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="468ae-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will contain:</span></span>

-   <span data-ttu-id="468ae-120">Ein Fehler wird \_ nicht \_ unterstützt, wenn die Schaltfläche nicht den Typ "bin [**\_ defcommandlink**](button-styles.md) " oder " [**SB \_ CommandLink**](button-styles.md) " hat.</span><span class="sxs-lookup"><span data-stu-id="468ae-120">ERROR\_NOT\_SUPPORTED, if the button does not have the [**BS\_DEFCOMMANDLINK**](button-styles.md) or [**BS\_COMMANDLINK**](button-styles.md) style.</span></span>
-   <span data-ttu-id="468ae-121">Fehler \_ unzureichender \_ Puffer, wenn der *LPARAM* -Puffer zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="468ae-121">ERROR\_INSUFFICIENT\_BUFFER, if the *lParam* buffer is too small.</span></span> <span data-ttu-id="468ae-122">Der *wParam* -Parameter enthält die erforderliche Puffergröße in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="468ae-122">The *wParam* parameter will contain the required buffer size, in characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="468ae-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="468ae-123">Requirements</span></span>



| <span data-ttu-id="468ae-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="468ae-124">Requirement</span></span> | <span data-ttu-id="468ae-125">Wert</span><span class="sxs-lookup"><span data-stu-id="468ae-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="468ae-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="468ae-126">Minimum supported client</span></span><br/> | <span data-ttu-id="468ae-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="468ae-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="468ae-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="468ae-128">Minimum supported server</span></span><br/> | <span data-ttu-id="468ae-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="468ae-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="468ae-130">Header</span><span class="sxs-lookup"><span data-stu-id="468ae-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="468ae-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="468ae-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="468ae-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="468ae-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="468ae-133">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="468ae-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="468ae-134">Schaltflächenstile</span><span class="sxs-lookup"><span data-stu-id="468ae-134">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="468ae-135">**Licher**</span><span class="sxs-lookup"><span data-stu-id="468ae-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="468ae-136">Schaltflächentypen</span><span class="sxs-lookup"><span data-stu-id="468ae-136">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

