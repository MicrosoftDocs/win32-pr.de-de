---
title: IPM_SETADDRESS Meldung (kommstrg. h)
description: Legt die Adress Werte für alle vier Felder im IP-Adress Steuerelement fest.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- Windows-Steuerelemente für IPM_SETADDRESS Meldung
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104463"
---
# <a name="ipm_setaddress-message"></a><span data-ttu-id="f514a-104">IPM- \_ setAddress-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f514a-104">IPM\_SETADDRESS message</span></span>

<span data-ttu-id="f514a-105">Legt die Adress Werte für alle vier Felder im IP-Adress Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="f514a-105">Sets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f514a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f514a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f514a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f514a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f514a-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="f514a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f514a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f514a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f514a-110">Ein **DWORD** -Wert, der die neue Adresse enthält.</span><span class="sxs-lookup"><span data-stu-id="f514a-110">A **DWORD** value that contains the new address.</span></span> <span data-ttu-id="f514a-111">Der Wert von Feld 3 ist in Bits 0 bis 7 enthalten.</span><span class="sxs-lookup"><span data-stu-id="f514a-111">The field 3 value is contained in bits 0 through 7.</span></span> <span data-ttu-id="f514a-112">Der Wert für Feld 2 ist in Bits 8 bis 15 enthalten.</span><span class="sxs-lookup"><span data-stu-id="f514a-112">The field 2 value is contained in bits 8 through 15.</span></span> <span data-ttu-id="f514a-113">Der Wert für Feld 1 ist in Bits 16 bis 23 enthalten.</span><span class="sxs-lookup"><span data-stu-id="f514a-113">The field 1 value is contained in bits 16 through 23.</span></span> <span data-ttu-id="f514a-114">Der Wert Feld 0 ist in Bits 24 bis 31 enthalten.</span><span class="sxs-lookup"><span data-stu-id="f514a-114">The field 0 value is contained in bits 24 through 31.</span></span> <span data-ttu-id="f514a-115">Das [**MakeIPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) -Makro kann auch zum Erstellen der Adressinformationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f514a-115">The [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) macro can also be used to create the address information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f514a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f514a-116">Return value</span></span>

<span data-ttu-id="f514a-117">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f514a-117">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f514a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f514a-118">Remarks</span></span>

<span data-ttu-id="f514a-119">Diese Meldung generiert keine [**IPN \_ FieldChanged**](ipn-fieldchanged.md) -Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="f514a-119">This message does not generate an [**IPN\_FIELDCHANGED**](ipn-fieldchanged.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="f514a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f514a-120">Requirements</span></span>



| <span data-ttu-id="f514a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f514a-121">Requirement</span></span> | <span data-ttu-id="f514a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f514a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f514a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f514a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f514a-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f514a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f514a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f514a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f514a-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f514a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f514a-127">Header</span><span class="sxs-lookup"><span data-stu-id="f514a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f514a-128"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f514a-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





