---
description: Ruft die Netzwerk Adresstypen ab, die von einem angegebenen Netzwerk Adress Steuerelement akzeptiert werden.
title: NCM_GETALLOWTYPE Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d93cb3cff575c18764e352da54a717d7c557001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041845"
---
# <a name="ncm_getallowtype-message"></a><span data-ttu-id="1c329-103">NCM- \_ getallowtype-Nachricht</span><span class="sxs-lookup"><span data-stu-id="1c329-103">NCM\_GETALLOWTYPE message</span></span>

<span data-ttu-id="1c329-104">Ruft die Netzwerk Adresstypen ab, die von einem angegebenen Netzwerk Adress Steuerelement akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c329-104">Retrieves the network address types that a specified network address control accepts.</span></span>


```C++
NCM_GETALLOWTYPE

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="1c329-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c329-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c329-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1c329-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1c329-107">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1c329-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1c329-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1c329-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1c329-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1c329-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c329-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c329-110">Return value</span></span>

<span data-ttu-id="1c329-111">Gibt die zulässigen Netzwerk Adresstypen als eine oder mehrere der [**net \_ String**](net-string.md) -Konstanten zurück.</span><span class="sxs-lookup"><span data-stu-id="1c329-111">Returns the allowed network address types as one or more of the [**NET\_STRING**](net-string.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c329-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c329-112">Remarks</span></span>

<span data-ttu-id="1c329-113">Die zurückgegebene Maske ist das Kriterium, das verwendet wird, um eine Netzwerkadresse in der [**NCM \_ GetAddress**](ncm-getaddress.md) -Nachricht zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1c329-113">The returned mask is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="1c329-114">Verwenden Sie diese Meldung nur für ein Netzwerk Adress Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="1c329-114">Use this message for a network address control only.</span></span> <span data-ttu-id="1c329-115">Verwenden Sie zum Instanziieren die in shellapi. h definierte Klasse **msctls- \_ netaddress** .</span><span class="sxs-lookup"><span data-stu-id="1c329-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="1c329-116">Ruft vor dem Senden dieser Nachricht [**initnetworkaddresscontrol**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) zur Laufzeit auf.</span><span class="sxs-lookup"><span data-stu-id="1c329-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="1c329-117">Dadurch wird die Bibliothek der allgemeinen Steuerelemente initialisiert, die das Netzwerk Adress Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="1c329-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c329-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1c329-118">Requirements</span></span>



| <span data-ttu-id="1c329-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c329-119">Requirement</span></span> | <span data-ttu-id="1c329-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1c329-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c329-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c329-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1c329-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c329-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1c329-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c329-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1c329-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c329-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c329-125">Header</span><span class="sxs-lookup"><span data-stu-id="1c329-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c329-126"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c329-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c329-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1c329-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c329-128">**NCM- \_ Typ "Typ"**</span><span class="sxs-lookup"><span data-stu-id="1c329-128">**NCM\_SETALLOWTYPE**</span></span>](ncm-setallowtype.md)
</dt> <dt>

[<span data-ttu-id="1c329-129">**NETADDR- \_ getallowtype**</span><span class="sxs-lookup"><span data-stu-id="1c329-129">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




