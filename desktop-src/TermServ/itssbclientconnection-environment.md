---
title: Itssbclientconnection-Umgebungs Eigenschaft
description: Ruft ein Objekt ab, das Informationen über die Umgebung enthält, die den Zielcomputer hostet.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- Umgebungs Eigenschaften Remotedesktopdienste
- Umgebungs Eigenschaft Remotedesktopdienste, itssbclientconnection-Schnittstelle
- Itssbclientconnection-Schnittstelle Remotedesktopdienste, Umgebungs Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18018c8f8fc5e7d017809cf5fe109db7c52712c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477724"
---
# <a name="itssbclientconnectionenvironment-property"></a><span data-ttu-id="cc678-106">Itssbclientconnection:: Environment-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cc678-106">ITsSbClientConnection::Environment property</span></span>

<span data-ttu-id="cc678-107">Ruft ein Objekt ab, das Informationen über die Umgebung enthält, die den Zielcomputer hostet.</span><span class="sxs-lookup"><span data-stu-id="cc678-107">Retrieves an object that contains information about the environment that hosts the target computer.</span></span> <span data-ttu-id="cc678-108">In einem Szenario mit virtuellen Desktops würde dieses Objekt z. b. Informationen über den Computer enthalten, der die virtuelle Maschine hostet.</span><span class="sxs-lookup"><span data-stu-id="cc678-108">For example, in a virtual desktop scenario, this object would contain information about the computer that hosts the virtual machine.</span></span>

<span data-ttu-id="cc678-109">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cc678-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc678-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc678-110">Syntax</span></span>


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a><span data-ttu-id="cc678-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cc678-111">Property value</span></span>

<span data-ttu-id="cc678-112">Ein Zeiger auf einen Zeiger auf ein [**itssbenvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) -Umgebungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc678-112">A pointer to a pointer to an [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) environment object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cc678-113">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="cc678-113">Error codes</span></span>

<span data-ttu-id="cc678-114">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="cc678-114">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc678-115">Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="cc678-115">Otherwise, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="cc678-116">Mögliche Werte sind u. a. die in der folgenden Liste aufgeführten Werte:</span><span class="sxs-lookup"><span data-stu-id="cc678-116">Possible values include, but are not limited to, those in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="cc678-117">E- \_ Zeiger</span><span class="sxs-lookup"><span data-stu-id="cc678-117">E\_POINTER</span></span>
</dt> <dd>

<span data-ttu-id="cc678-118">Die Umgebung wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="cc678-118">The environment was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc678-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc678-119">Remarks</span></span>

<span data-ttu-id="cc678-120">Ein Orchestrierungs-Plug-in kann diese Methode aufrufen, um Umgebungs Informationen zu einem virtuellen Zielcomputer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cc678-120">An orchestration plug-in can call this method to retrieve environment information about a target virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc678-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc678-121">Requirements</span></span>



| <span data-ttu-id="cc678-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc678-122">Requirement</span></span> | <span data-ttu-id="cc678-123">Wert</span><span class="sxs-lookup"><span data-stu-id="cc678-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cc678-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc678-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cc678-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cc678-125">None supported</span></span><br/>                                                            |
| <span data-ttu-id="cc678-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc678-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cc678-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc678-127">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="cc678-128">IDL</span><span class="sxs-lookup"><span data-stu-id="cc678-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cc678-129"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cc678-129"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc678-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc678-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc678-131">**Itssbclientconnection**</span><span class="sxs-lookup"><span data-stu-id="cc678-131">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





