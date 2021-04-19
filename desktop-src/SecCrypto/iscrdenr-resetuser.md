---
description: Löscht den Benutzernamen aus dem Smartcard-Steuerelement.
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: 'Iscrdenr:: resetuser-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3b00721229890f82b00e7e7a41ccb8796a81b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373301"
---
# <a name="iscrdenrresetuser-method"></a><span data-ttu-id="11c68-103">Iscrdenr:: resetuser-Methode</span><span class="sxs-lookup"><span data-stu-id="11c68-103">ISCrdEnr::resetUser method</span></span>

<span data-ttu-id="11c68-104">Die **resetuser** -Methode löscht den Benutzernamen aus dem Smartcard-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="11c68-104">The **resetUser** method clears the user name from the smart card control.</span></span>

## <a name="syntax"></a><span data-ttu-id="11c68-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11c68-105">Syntax</span></span>


```C++
HRESULT resetUser();
```



## <a name="parameters"></a><span data-ttu-id="11c68-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11c68-106">Parameters</span></span>

<span data-ttu-id="11c68-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="11c68-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="11c68-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11c68-108">Remarks</span></span>

<span data-ttu-id="11c68-109">Mit dieser Methode werden alle vorhandenen Benutzernamen und zuvor registrierten Zertifikate aus dem Arbeitsspeicher gelöscht.</span><span class="sxs-lookup"><span data-stu-id="11c68-109">This method clears any existing user name and previously enrolled certificate from memory.</span></span> <span data-ttu-id="11c68-110">Das zuvor registrierte Zertifikat wird jedoch nicht von der Smartcard entfernt.</span><span class="sxs-lookup"><span data-stu-id="11c68-110">The previously enrolled certificate is not removed from the smart card, however.</span></span>

## <a name="requirements"></a><span data-ttu-id="11c68-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11c68-111">Requirements</span></span>



| <span data-ttu-id="11c68-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11c68-112">Requirement</span></span> | <span data-ttu-id="11c68-113">Wert</span><span class="sxs-lookup"><span data-stu-id="11c68-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11c68-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11c68-114">Minimum supported client</span></span><br/> | <span data-ttu-id="11c68-115">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="11c68-115">None supported</span></span><br/>                                                               |
| <span data-ttu-id="11c68-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11c68-116">Minimum supported server</span></span><br/> | <span data-ttu-id="11c68-117">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11c68-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="11c68-118">DLL</span><span class="sxs-lookup"><span data-stu-id="11c68-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11c68-119"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11c68-119"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="11c68-120">IID</span><span class="sxs-lookup"><span data-stu-id="11c68-120">IID</span></span><br/>                      | <span data-ttu-id="11c68-121">IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="11c68-121">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="11c68-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11c68-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11c68-123">**Iscrdenr**</span><span class="sxs-lookup"><span data-stu-id="11c68-123">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="11c68-124">**Iscrdenr:: GetUserName**</span><span class="sxs-lookup"><span data-stu-id="11c68-124">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="11c68-125">**Iscrdenr:: selectusername**</span><span class="sxs-lookup"><span data-stu-id="11c68-125">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="11c68-126">**Iscrdenr:: setUserName**</span><span class="sxs-lookup"><span data-stu-id="11c68-126">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




