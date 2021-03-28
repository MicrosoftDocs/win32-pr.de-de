---
description: Gibt das Standard Symbol für das Element zurück, das durch die zugehörige smdata-Struktur angegeben wird.
title: SMC_DEFAULTICON Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d5f6789a-f160-4fba-ba64-b1a0c491fdaa
api_name:
- SMC_DEFAULTICON
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 10edab26c87dae4b1c9d2d5f06390fc608ba1edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994854"
---
# <a name="smc_defaulticon-message"></a><span data-ttu-id="eaa64-103">SMC- \_ DefaultIcon-Nachricht</span><span class="sxs-lookup"><span data-stu-id="eaa64-103">SMC\_DEFAULTICON message</span></span>

<span data-ttu-id="eaa64-104">Gibt das Standard Symbol für das Element zurück, das durch die zugehörige [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="eaa64-104">Return the default icon for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEFAULTICON 
    wParam = (WPARAM) (LPWSTR) pwszIcon;
    lParam = (LPARAM) (int) iIcon
            
```



## <a name="parameters"></a><span data-ttu-id="eaa64-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="eaa64-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaa64-106">*pwszicon*</span><span class="sxs-lookup"><span data-stu-id="eaa64-106">*pwszIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="eaa64-107">Ein Zeiger auf eine Zeichenfolge, die den voll qualifizierten Pfad der Datei empfängt, die das Standard Symbol enthält.</span><span class="sxs-lookup"><span data-stu-id="eaa64-107">A pointer to a string that receives the fully qualified path of the file that contains the default icon.</span></span>

</dd> <dt>

<span data-ttu-id="eaa64-108">*Symbols*</span><span class="sxs-lookup"><span data-stu-id="eaa64-108">*iIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="eaa64-109">Ein Zeiger auf eine Ganzzahl, die den Index des Symbols in der durch *pwszicon* angegebenen Datei empfängt.</span><span class="sxs-lookup"><span data-stu-id="eaa64-109">A pointer to an integer that receives the index of the icon in the file specified by *pwszIcon*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaa64-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eaa64-110">Return value</span></span>

<span data-ttu-id="eaa64-111">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="eaa64-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaa64-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaa64-112">Remarks</span></span>

<span data-ttu-id="eaa64-113">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="eaa64-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa64-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="eaa64-114">Requirements</span></span>



| <span data-ttu-id="eaa64-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaa64-115">Requirement</span></span> | <span data-ttu-id="eaa64-116">Wert</span><span class="sxs-lookup"><span data-stu-id="eaa64-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa64-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eaa64-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eaa64-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaa64-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="eaa64-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eaa64-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eaa64-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eaa64-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eaa64-121">Header</span><span class="sxs-lookup"><span data-stu-id="eaa64-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaa64-122"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaa64-122"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="eaa64-123">IDL</span><span class="sxs-lookup"><span data-stu-id="eaa64-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eaa64-124"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eaa64-124"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




