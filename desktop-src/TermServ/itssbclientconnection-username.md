---
title: Benutzername-Eigenschaft von itssbclientconnection
description: Ruft einen Wert ab, der den Namen des Benutzers angibt, der die Verbindung initiiert hat.
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- Username-Eigenschaft Remotedesktopdienste
- Username-Eigenschaft Remotedesktopdienste, itssbclientconnection-Schnittstelle
- Itssbclientconnection-Schnittstelle Remotedesktopdienste, UserName-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94bd3c1e5bb588ffb276b336cd945f32a0c19afd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341147"
---
# <a name="itssbclientconnectionusername-property"></a><span data-ttu-id="d0ccf-106">Itssbclientconnection:: Username-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d0ccf-106">ITsSbClientConnection::UserName property</span></span>

<span data-ttu-id="d0ccf-107">Ruft einen Wert ab, der den Namen des Benutzers angibt, der die Verbindung initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="d0ccf-107">Retrieves a value that indicates the name of the user who initiated the connection.</span></span>

<span data-ttu-id="d0ccf-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d0ccf-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ccf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0ccf-109">Syntax</span></span>


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="d0ccf-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d0ccf-110">Property value</span></span>

<span data-ttu-id="d0ccf-111">Ein Zeiger auf einen Benutzernamen.</span><span class="sxs-lookup"><span data-stu-id="d0ccf-111">A pointer to a user name.</span></span> <span data-ttu-id="d0ccf-112">Wenn Sie die Zeichenfolge nicht mehr verwenden, können Sie Sie durch Aufrufen der [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) -Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="d0ccf-112">When you have finished using the string, free it by calling the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0ccf-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0ccf-113">Requirements</span></span>



| <span data-ttu-id="d0ccf-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0ccf-114">Requirement</span></span> | <span data-ttu-id="d0ccf-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d0ccf-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ccf-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0ccf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d0ccf-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d0ccf-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="d0ccf-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0ccf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d0ccf-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0ccf-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="d0ccf-120">IDL</span><span class="sxs-lookup"><span data-stu-id="d0ccf-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d0ccf-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d0ccf-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0ccf-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0ccf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ccf-123">**Itssbclientconnection**</span><span class="sxs-lookup"><span data-stu-id="d0ccf-123">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

