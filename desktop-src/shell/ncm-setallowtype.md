---
description: Legt die Netzwerk Adresstypen fest, die von einem angegebenen Netzwerk Adress Steuerelement akzeptiert werden.
title: NCM_SETALLOWTYPE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d9cc822e07022a01439fbe7e41243bd1b78e636b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753056"
---
# <a name="ncm_setallowtype-message"></a><span data-ttu-id="fc195-103">NCM- \_ Nachricht vom Typ "logatlowtype"</span><span class="sxs-lookup"><span data-stu-id="fc195-103">NCM\_SETALLOWTYPE message</span></span>

<span data-ttu-id="fc195-104">Legt die Netzwerk Adresstypen fest, die von einem angegebenen Netzwerk Adress Steuerelement akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="fc195-104">Sets the network address types that a specified network address control accepts.</span></span>


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="fc195-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc195-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc195-106">*addrmask* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc195-106">*addrMask* \[in\]</span></span>
</dt> <dd><span data-ttu-id="fc195-107">Gibt die Netzwerk Adresstypen als eine oder mehrere der <a href="net-string.md">**net \_ String**</a> -Konstanten an.</span><span class="sxs-lookup"><span data-stu-id="fc195-107">Specifies the network address types as one or more of the <a href="net-string.md">**NET\_STRING**</a> constants.</span></span></dd> <dt>

<span data-ttu-id="fc195-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc195-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fc195-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="fc195-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc195-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc195-110">Return value</span></span>

<span data-ttu-id="fc195-111">Gibt \_ bei Erfolg S OK oder andernfalls einen Fehlerwert zurück.</span><span class="sxs-lookup"><span data-stu-id="fc195-111">Returns S\_OK if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc195-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc195-112">Remarks</span></span>

<span data-ttu-id="fc195-113">Der Masken Satz ist das Kriterium, das verwendet wird, um eine Netzwerkadresse in der [**NCM- \_ GetAddress**](ncm-getaddress.md) -Nachricht zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="fc195-113">The mask set is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="fc195-114">Verwenden Sie diese Meldung nur für ein Netzwerk Adress Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="fc195-114">Use this message for a network address control only.</span></span> <span data-ttu-id="fc195-115">Verwenden Sie zum Instanziieren die in shellapi. h definierte Klasse **msctls- \_ netaddress** .</span><span class="sxs-lookup"><span data-stu-id="fc195-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="fc195-116">Ruft vor dem Senden dieser Nachricht [**initnetworkaddresscontrol**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) zur Laufzeit auf.</span><span class="sxs-lookup"><span data-stu-id="fc195-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="fc195-117">Dadurch wird die Bibliothek der allgemeinen Steuerelemente initialisiert, die das Netzwerk Adress Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="fc195-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc195-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fc195-118">Requirements</span></span>



| <span data-ttu-id="fc195-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc195-119">Requirement</span></span> | <span data-ttu-id="fc195-120">Wert</span><span class="sxs-lookup"><span data-stu-id="fc195-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc195-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc195-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fc195-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc195-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc195-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc195-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fc195-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc195-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc195-125">Header</span><span class="sxs-lookup"><span data-stu-id="fc195-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc195-126"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc195-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc195-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fc195-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc195-128">**NCM- \_ getallowtype**</span><span class="sxs-lookup"><span data-stu-id="fc195-128">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="fc195-129">**NETADDR- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="fc195-129">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




