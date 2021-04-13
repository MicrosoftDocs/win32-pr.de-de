---
title: WSMAN. getErrorMessage-Methode (WSManDisp. h)
description: Gibt eine formatierte Zeichenfolge zurück, die den Text einer Fehlernummer enthält.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- GetErrorMessage-Methode Windows-Remoteverwaltung
- GetErrorMessage-Methode Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, getErrorMessage-Methode
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340697"
---
# <a name="wsmangeterrormessage-method"></a><span data-ttu-id="4447f-106">WSMAN. getErrorMessage-Methode</span><span class="sxs-lookup"><span data-stu-id="4447f-106">WSMan.GetErrorMessage method</span></span>

<span data-ttu-id="4447f-107">Gibt eine formatierte Zeichenfolge zurück, die den Text einer Fehlernummer enthält.</span><span class="sxs-lookup"><span data-stu-id="4447f-107">Returns a formatted string that contains the text of an error number.</span></span> <span data-ttu-id="4447f-108">Diese Methode führt denselben Vorgang aus wie die **WinRM** -Befehlszeile **WinRM helpmsg** *Decimal oder hexadezimale Fehlernummer*.</span><span class="sxs-lookup"><span data-stu-id="4447f-108">This method performs the same operation as the **Winrm** command-line **winrm helpmsg** *decimal or hexadecimal error number*.</span></span>

## <a name="syntax"></a><span data-ttu-id="4447f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4447f-109">Syntax</span></span>


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="4447f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4447f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4447f-111">*errornumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4447f-111">*errorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4447f-112">Eine Fehlermeldungs Nummer in Dezimal-oder hexadezimal aus WinRM-, WinHTTP-oder anderen Betriebssystemkomponenten.</span><span class="sxs-lookup"><span data-stu-id="4447f-112">An error message number in decimal or hexadecimal from WinRM, WinHTTP, or other operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="4447f-113">*ErrorMessage* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4447f-113">*errorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4447f-114">Eine Fehlermeldungs Zeichenfolge, die wie vom **WinRM** -Befehl zurückgegebene Meldungen formatiert</span><span class="sxs-lookup"><span data-stu-id="4447f-114">An error message string formatted like messages returned from the **Winrm** command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4447f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4447f-115">Remarks</span></span>

<span data-ttu-id="4447f-116">Die entsprechende C++-Methode ist " [**iwsmanex:: getErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage)".</span><span class="sxs-lookup"><span data-stu-id="4447f-116">The corresponding C++ method is [**IWSManEx::GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="4447f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4447f-117">Requirements</span></span>



| <span data-ttu-id="4447f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4447f-118">Requirement</span></span> | <span data-ttu-id="4447f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="4447f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4447f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4447f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4447f-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4447f-121">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="4447f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4447f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4447f-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4447f-123">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4447f-124">Header</span><span class="sxs-lookup"><span data-stu-id="4447f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4447f-125"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4447f-125"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4447f-126">IDL</span><span class="sxs-lookup"><span data-stu-id="4447f-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4447f-127"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4447f-127"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="4447f-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4447f-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="4447f-129"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4447f-129"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4447f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4447f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4447f-131"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4447f-131"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4447f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4447f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4447f-133">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="4447f-133">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





