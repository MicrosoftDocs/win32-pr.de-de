---
title: IPM_GETADDRESS Meldung (kommstrg. h)
description: Ruft die Adress Werte für alle vier Felder im IP-Adress Steuerelement ab.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- Windows-Steuerelemente für IPM_GETADDRESS Meldung
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 426e9c76712701b2f4e108679133be23eb700687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956724"
---
# <a name="ipm_getaddress-message"></a><span data-ttu-id="c80be-104">IPM- \_ GetAddress-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c80be-104">IPM\_GETADDRESS message</span></span>

<span data-ttu-id="c80be-105">Ruft die Adress Werte für alle vier Felder im IP-Adress Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="c80be-105">Gets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c80be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c80be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c80be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c80be-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c80be-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c80be-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c80be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c80be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c80be-110">Ein Zeiger auf einen **DWORD** -Wert, der die Adresse empfängt.</span><span class="sxs-lookup"><span data-stu-id="c80be-110">A pointer to a **DWORD** value that receives the address.</span></span> <span data-ttu-id="c80be-111">Der Wert für Feld 3 ist in Bits 0 bis 7 enthalten.</span><span class="sxs-lookup"><span data-stu-id="c80be-111">The field 3 value will be contained in bits 0 through 7.</span></span> <span data-ttu-id="c80be-112">Der Wert für Feld 2 ist in Bits 8 bis 15 enthalten.</span><span class="sxs-lookup"><span data-stu-id="c80be-112">The field 2 value will be contained in bits 8 through 15.</span></span> <span data-ttu-id="c80be-113">Der Wert für Feld 1 ist in Bits 16 bis 23 enthalten.</span><span class="sxs-lookup"><span data-stu-id="c80be-113">The field 1 value will be contained in bits 16 through 23.</span></span> <span data-ttu-id="c80be-114">Der Wert Feld 0 ist in Bits 24 bis 31 enthalten.</span><span class="sxs-lookup"><span data-stu-id="c80be-114">The field 0 value will be contained in bits 24 through 31.</span></span> <span data-ttu-id="c80be-115">Die [**erste \_ IP-Adresse**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), die [**zweite \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress)-, [**dritte \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)-und [**vierte \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) -Makros können auch zum Extrahieren der Adressinformationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c80be-115">The [**FIRST\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), [**SECOND\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**THIRD\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress), and [**FOURTH\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) macros can also be used to extract the address information.</span></span> <span data-ttu-id="c80be-116">NULL wird als Adresse für alle leeren Felder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c80be-116">Zero will be returned as the address for any blank fields.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c80be-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c80be-117">Return value</span></span>

<span data-ttu-id="c80be-118">Gibt die Anzahl der nicht leeren Felder zurück.</span><span class="sxs-lookup"><span data-stu-id="c80be-118">Returns the number of nonblank fields.</span></span>

## <a name="requirements"></a><span data-ttu-id="c80be-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c80be-119">Requirements</span></span>



| <span data-ttu-id="c80be-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c80be-120">Requirement</span></span> | <span data-ttu-id="c80be-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c80be-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c80be-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c80be-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c80be-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c80be-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c80be-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c80be-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c80be-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c80be-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c80be-126">Header</span><span class="sxs-lookup"><span data-stu-id="c80be-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c80be-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c80be-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





