---
description: Gibt die Knotenadresse (nad) an, die mit der iscardcmd-Schnittstelle verwendet werden soll.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: Iscardcmd::p ut_Nad-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 64ed9c502811db5666e561a1f290cc234e6c81e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863264"
---
# <a name="iscardcmdput_nad-method"></a><span data-ttu-id="9a52e-103">Iscardcmd::p UT \_ nad-Methode</span><span class="sxs-lookup"><span data-stu-id="9a52e-103">ISCardCmd::put\_Nad method</span></span>

<span data-ttu-id="9a52e-104">\[Die **Put \_ nad** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9a52e-104">\[The **put\_Nad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9a52e-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9a52e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9a52e-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9a52e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9a52e-107">Die **Put \_ nad** -Methode gibt die Knotenadresse (nad) an, die mit der [**iscardcmd**](iscardcmd.md) -Schnittstelle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a52e-107">The **put\_Nad** method specifies the node address (Nad) to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="9a52e-108">Dies gilt für die Kommunikation, die nur die [*Protokoll Kommunikation T = 1*](../secgloss/t-gly.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a52e-108">This applies to communications using the [*T=1 protocol*](../secgloss/t-gly.md) communications only.</span></span> <span data-ttu-id="9a52e-109">Standardmäßig verwendet das [**iscardcmd**](iscardcmd.md) -Objekt einen nad-Wert von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9a52e-109">By default, the [**ISCardCmd**](iscardcmd.md) object uses a Nad of zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a52e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a52e-110">Syntax</span></span>


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a><span data-ttu-id="9a52e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a52e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a52e-112">*bnad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a52e-112">*bNad* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a52e-113">Byte, das das zu verwendende nad darstellt.</span><span class="sxs-lookup"><span data-stu-id="9a52e-113">Byte representing the Nad to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a52e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a52e-114">Return value</span></span>

<span data-ttu-id="9a52e-115">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="9a52e-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9a52e-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9a52e-116">Return code</span></span>                                                                                  | <span data-ttu-id="9a52e-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a52e-117">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="9a52e-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a52e-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="9a52e-119">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9a52e-119">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9a52e-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="9a52e-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="9a52e-121">Der *bnad* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9a52e-121">The *bNad* parameter is not valid.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="9a52e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a52e-122">Remarks</span></span>

<span data-ttu-id="9a52e-123">Diese Methode sollte nur aufgerufen werden, wenn es erforderlich ist, einen anderen Wert als 0 (null) für die nad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a52e-123">This method should be called only when it is necessary to use a value other than zero for the Nad.</span></span>

## <a name="examples"></a><span data-ttu-id="9a52e-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a52e-124">Examples</span></span>

<span data-ttu-id="9a52e-125">Im folgenden Beispiel wird gezeigt, wie eine mit der [**iscardcmd**](iscardcmd.md) -Schnittstelle zu verwendende Knotenadresse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9a52e-125">The following example shows how to specify a node address to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="9a52e-126">Im Beispiel wird davon ausgegangen, dass bynadvalue eine Variable vom Typ " **Byte** " ist, der zuvor ein Wert zugewiesen wurde, und dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der **iscardcmd** -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="9a52e-126">The example assumes that byNadValue is a variable of type **BYTE** that was previously assigned a value, and that pISCardCmd is a valid pointer to an instance of the **ISCardCmd** interface.</span></span>


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="9a52e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a52e-127">Requirements</span></span>



| <span data-ttu-id="9a52e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a52e-128">Requirement</span></span> | <span data-ttu-id="9a52e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9a52e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a52e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a52e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9a52e-131">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a52e-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9a52e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a52e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9a52e-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a52e-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9a52e-134">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9a52e-134">End of client support</span></span><br/>    | <span data-ttu-id="9a52e-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9a52e-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9a52e-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9a52e-136">End of server support</span></span><br/>    | <span data-ttu-id="9a52e-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9a52e-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9a52e-138">Header</span><span class="sxs-lookup"><span data-stu-id="9a52e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a52e-139"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9a52e-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a52e-140">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9a52e-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="9a52e-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9a52e-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9a52e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="9a52e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a52e-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a52e-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9a52e-144">IID</span><span class="sxs-lookup"><span data-stu-id="9a52e-144">IID</span></span><br/>                      | <span data-ttu-id="9a52e-145">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="9a52e-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9a52e-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a52e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a52e-147">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="9a52e-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
