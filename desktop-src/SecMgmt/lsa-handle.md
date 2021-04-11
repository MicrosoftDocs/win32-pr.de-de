---
description: Handle für das lokale Richtlinien Objekt.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (ntabcapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042315"
---
# <a name="lsa_handle"></a><span data-ttu-id="4c016-103">LSA- \_ handle</span><span class="sxs-lookup"><span data-stu-id="4c016-103">LSA\_HANDLE</span></span>

<span data-ttu-id="4c016-104">Der **LSA- \_ handle** -Datentyp ist ein Handle für das lokale [**Richtlinien**](policy-object.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="4c016-104">The **LSA\_HANDLE** data type is a handle to the local [**Policy**](policy-object.md) object.</span></span>


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="4c016-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c016-105">Remarks</span></span>

<span data-ttu-id="4c016-106">Bevor Sie die lokale Richtlinien-API verwenden können, muss Ihre Anwendung ein Handle für ein [**Richtlinien**](policy-object.md) Objekt öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c016-106">Before you can use the local policy API your application must open a handle to a [**Policy**](policy-object.md) object.</span></span> <span data-ttu-id="4c016-107">Nennen Sie hierzu [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span><span class="sxs-lookup"><span data-stu-id="4c016-107">To do this, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span></span> <span data-ttu-id="4c016-108">Diese Funktion gibt ein Handle zurück, das von der Anwendung in nachfolgenden LSA-Richtlinien Funktionsaufrufen angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="4c016-108">This function returns a handle that your application can then specify in subsequent LSA policy function calls.</span></span>

<span data-ttu-id="4c016-109">Jedes Handle verfügt über einen zugeordneten Berechtigungs Satz, mit dem die Vorgänge bestimmt werden, die Ihre Anwendung mit dem Handle für das [**Richtlinien**](policy-object.md) Objekt ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="4c016-109">Each handle has an associated set of permissions that determine the operations your application can perform on the [**Policy**](policy-object.md) object by using the handle.</span></span> <span data-ttu-id="4c016-110">Die Anwendung kann jeweils mehr als ein Handle für das **Richtlinien** Objekt öffnen.</span><span class="sxs-lookup"><span data-stu-id="4c016-110">Your application can open more than one handle to the **Policy** object at a time.</span></span> <span data-ttu-id="4c016-111">Wenn ein Handle nicht mehr benötigt wird, sollte die Anwendung es durch Aufrufen von [**lsaclose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)schließen.</span><span class="sxs-lookup"><span data-stu-id="4c016-111">When a handle is no longer required, your application should close it by calling [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c016-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c016-112">Requirements</span></span>



| <span data-ttu-id="4c016-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c016-113">Requirement</span></span> | <span data-ttu-id="4c016-114">Wert</span><span class="sxs-lookup"><span data-stu-id="4c016-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c016-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4c016-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4c016-116">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c016-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4c016-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4c016-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4c016-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4c016-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c016-119">Header</span><span class="sxs-lookup"><span data-stu-id="4c016-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c016-120"><dt>Ntabcapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c016-120"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c016-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c016-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c016-122">**Lsaclose**</span><span class="sxs-lookup"><span data-stu-id="4c016-122">**LsaClose**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[<span data-ttu-id="4c016-123">**LsaOpenPolicy**</span><span class="sxs-lookup"><span data-stu-id="4c016-123">**LsaOpenPolicy**</span></span>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

