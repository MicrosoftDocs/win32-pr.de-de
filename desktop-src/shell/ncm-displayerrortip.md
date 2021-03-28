---
description: Zeigt eine Fehlermeldung in der Sprechblasen Info an, die dem Netzwerk Adress Steuerelement zugeordnet ist.
title: NCM_DISPLAYERRORTIP Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993775"
---
# <a name="ncm_displayerrortip-message"></a><span data-ttu-id="a5eab-103">NCM- \_ displayerrortip-Meldung</span><span class="sxs-lookup"><span data-stu-id="a5eab-103">NCM\_DISPLAYERRORTIP message</span></span>

<span data-ttu-id="a5eab-104">Zeigt eine Fehlermeldung in der Sprechblasen Info an, die dem Netzwerk Adress Steuerelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a5eab-104">Displays an error message in the balloon tip associated with the network address control.</span></span>


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="a5eab-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5eab-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5eab-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a5eab-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a5eab-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a5eab-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a5eab-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5eab-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a5eab-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="a5eab-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5eab-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5eab-110">Return value</span></span>

<span data-ttu-id="a5eab-111">Wenn diese Nachricht erfolgreich ist, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a5eab-111">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a5eab-112">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a5eab-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5eab-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5eab-113">Remarks</span></span>

<span data-ttu-id="a5eab-114">Senden Sie diese Meldung, um eine Fehlermeldung anzuzeigen, wenn eine Adresse, die in das Steuerelement eingegeben wird, nicht anhand der zulässigen Netzwerk Adresstypen überprüft wird, die mit der [**NCM \_ setallowtype**](ncm-setallowtype.md) -Nachricht festgelegt</span><span class="sxs-lookup"><span data-stu-id="a5eab-114">Send this message to display an error message when an address typed into the control does not validate against the allowed network address types set with the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message.</span></span> <span data-ttu-id="a5eab-115">Verwenden Sie die [**NCM \_ GetAddress**](ncm-getaddress.md) -Nachricht, um die Adresse zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a5eab-115">Use the [**NCM\_GETADDRESS**](ncm-getaddress.md) message to validate the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5eab-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a5eab-116">Requirements</span></span>



| <span data-ttu-id="a5eab-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5eab-117">Requirement</span></span> | <span data-ttu-id="a5eab-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a5eab-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5eab-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5eab-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a5eab-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5eab-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a5eab-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5eab-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a5eab-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5eab-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5eab-123">Header</span><span class="sxs-lookup"><span data-stu-id="a5eab-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5eab-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5eab-124"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5eab-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a5eab-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5eab-126">**NETADDR \_ displayerrortip**</span><span class="sxs-lookup"><span data-stu-id="a5eab-126">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




