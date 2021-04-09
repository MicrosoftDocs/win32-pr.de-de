---
title: Name der itssbenvironment-Eigenschaft
description: Ruft einen Wert ab, der den Namen der Umgebung angibt, die den Zielcomputer hostet.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Name-Eigenschaft Remotedesktopdienste
- Name-Eigenschaft Remotedesktopdienste, itssbenvironment-Schnittstelle
- Itssbenvironment-Schnittstelle Remotedesktopdienste, Name-Eigenschaft
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b5ac2fd725ec07102c08e93b2bfb39dabe701ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949620"
---
# <a name="itssbenvironmentname-property"></a><span data-ttu-id="e53a6-106">Itssbenvironment:: Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e53a6-106">ITsSbEnvironment::Name property</span></span>

<span data-ttu-id="e53a6-107">Ruft einen Wert ab, der den Namen der Umgebung angibt, die den Zielcomputer hostet.</span><span class="sxs-lookup"><span data-stu-id="e53a6-107">Retrieves a value that indicates the name of the environment that hosts the target computer.</span></span>

<span data-ttu-id="e53a6-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e53a6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e53a6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e53a6-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="e53a6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e53a6-110">Property value</span></span>

<span data-ttu-id="e53a6-111">Ein Zeiger auf eine **BSTR** -Variable, die den Namen der Umgebung enthält.</span><span class="sxs-lookup"><span data-stu-id="e53a6-111">A pointer to a **BSTR** variable that contains the name of the environment.</span></span>

## <a name="remarks"></a><span data-ttu-id="e53a6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e53a6-112">Remarks</span></span>

<span data-ttu-id="e53a6-113">Diese Methode gibt eine Zeichenfolge zurück, die nicht direkt von Remotedesktopverbindung Broker (RD-Verbindungsbroker) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e53a6-113">This method returns a string that is not directly used by Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="e53a6-114">RD-Verbindungsbroker übergibt diese Zeichenfolge an Ressourcen-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="e53a6-114">RD Connection Broker passes this string to resource plug-ins.</span></span>

## <a name="requirements"></a><span data-ttu-id="e53a6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e53a6-115">Requirements</span></span>



| <span data-ttu-id="e53a6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e53a6-116">Requirement</span></span> | <span data-ttu-id="e53a6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e53a6-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e53a6-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e53a6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e53a6-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e53a6-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="e53a6-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e53a6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e53a6-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e53a6-121">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="e53a6-122">IDL</span><span class="sxs-lookup"><span data-stu-id="e53a6-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e53a6-123"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e53a6-123"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e53a6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e53a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e53a6-125">**Itssbenvironment**</span><span class="sxs-lookup"><span data-stu-id="e53a6-125">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





