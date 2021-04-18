---
description: Wird von einem Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) verwendet, um das Fenster Handle abzurufen, das der CSP als übergeordnetes Element oder Besitzer einer beliebigen angezeigten Benutzeroberfläche verwenden soll.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: CRYPT_RETURN_HWND Funktionszeiger (cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352305"
---
# <a name="crypt_return_hwnd-function-pointer"></a><span data-ttu-id="f9382-103">Crypt \_ Return- \_ HWND-Funktionszeiger</span><span class="sxs-lookup"><span data-stu-id="f9382-103">CRYPT\_RETURN\_HWND function pointer</span></span>

<span data-ttu-id="f9382-104">Die Funktion " **funkreturnhwnd** Callback" wird von einem [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) verwendet, um das Fenster Handle abzurufen, das der CSP als übergeordnetes Element oder als Besitzer einer beliebigen angezeigten Benutzeroberfläche verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="f9382-104">The **FuncReturnhWnd** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to obtain the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9382-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9382-105">Syntax</span></span>


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a><span data-ttu-id="f9382-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9382-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9382-107">*phwnd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f9382-107">*phWnd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9382-108">Die Adresse einer **HWND** -Variablen, die das übergeordnete Fenster Handle empfängt.</span><span class="sxs-lookup"><span data-stu-id="f9382-108">The address of an **HWND** variable that receives the parent window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9382-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9382-109">Return value</span></span>

<span data-ttu-id="f9382-110">Dieser Funktionszeiger gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f9382-110">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9382-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9382-111">Requirements</span></span>



| <span data-ttu-id="f9382-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9382-112">Requirement</span></span> | <span data-ttu-id="f9382-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f9382-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9382-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9382-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f9382-115">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9382-115">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9382-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9382-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f9382-117">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9382-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f9382-118">Header</span><span class="sxs-lookup"><span data-stu-id="f9382-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9382-119"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9382-119"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9382-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9382-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9382-121">**Cpacquirecontext**</span><span class="sxs-lookup"><span data-stu-id="f9382-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="f9382-122">**Vtableprovstruc**</span><span class="sxs-lookup"><span data-stu-id="f9382-122">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
