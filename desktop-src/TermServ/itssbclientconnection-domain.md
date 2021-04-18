---
title: Itssbclientconnection-Domänen Eigenschaft
description: Ruft einen Wert ab, der den Domänen Namen des-Remotedesktopverbindung (RDC)-Clients angibt.
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- Domänen Eigenschaft Remotedesktopdienste
- Domänen Eigenschaft Remotedesktopdienste, itssbclientconnection-Schnittstelle
- Itssbclientconnection-Schnittstelle Remotedesktopdienste, Domänen Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 678d6fc6838b615faeec9fa36b736b3105b64453
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344097"
---
# <a name="itssbclientconnectiondomain-property"></a><span data-ttu-id="5f2e7-106">Itssbclientconnection::D omain-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5f2e7-106">ITsSbClientConnection::Domain property</span></span>

<span data-ttu-id="5f2e7-107">Ruft einen Wert ab, der den Domänen Namen des-Remotedesktopverbindung (RDC)-Clients angibt.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-107">Retrieves a value that indicates the domain name of the Remote Desktop Connection (RDC) client.</span></span>

<span data-ttu-id="5f2e7-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f2e7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f2e7-109">Syntax</span></span>


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="5f2e7-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5f2e7-110">Property value</span></span>

<span data-ttu-id="5f2e7-111">Ein Zeiger auf eine **BSTR** -Variable, die den Domänen Namen des RDC-Clients enthält.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-111">A pointer to a **BSTR** variable that contains the domain name of the RDC client.</span></span> <span data-ttu-id="5f2e7-112">Wenn Sie die Zeichenfolge nicht mehr verwenden, können Sie Sie durch Aufrufen der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="5f2e7-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f2e7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f2e7-113">Requirements</span></span>



| <span data-ttu-id="5f2e7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f2e7-114">Requirement</span></span> | <span data-ttu-id="5f2e7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5f2e7-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5f2e7-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f2e7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5f2e7-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5f2e7-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="5f2e7-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f2e7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5f2e7-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5f2e7-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="5f2e7-120">IDL</span><span class="sxs-lookup"><span data-stu-id="5f2e7-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f2e7-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f2e7-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f2e7-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f2e7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f2e7-123">**Itssbclientconnection**</span><span class="sxs-lookup"><span data-stu-id="5f2e7-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

