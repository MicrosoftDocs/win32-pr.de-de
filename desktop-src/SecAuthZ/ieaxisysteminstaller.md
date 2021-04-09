---
description: Installiert ein ActiveX-Objekt.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: Ieaxisysteminstaller-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 391088a70aa845cd685511f10e4eb6e809dc7fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050383"
---
# <a name="ieaxisysteminstaller-interface"></a><span data-ttu-id="ceb6f-103">Ieaxisysteminstaller-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ceb6f-103">IeAxiSystemInstaller interface</span></span>

<span data-ttu-id="ceb6f-104">Die **ieaxisysteminstaller** -Schnittstelle installiert ein ActiveX-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ceb6f-104">The **IeAxiSystemInstaller** interface installs an ActiveX object.</span></span>

<span data-ttu-id="ceb6f-105">Diese Schnittstelle ist nicht in einem öffentlichen Header deklariert.</span><span class="sxs-lookup"><span data-stu-id="ceb6f-105">This interface is not declared in a public header.</span></span> <span data-ttu-id="ceb6f-106">Anwendungen müssen es selbst definieren.</span><span class="sxs-lookup"><span data-stu-id="ceb6f-106">Applications must define it themselves.</span></span> <span data-ttu-id="ceb6f-107">Das folgende IDL-Fragment (Interface Definition Language) beschreibt diese Schnittstelle, einschließlich ihrer IID.</span><span class="sxs-lookup"><span data-stu-id="ceb6f-107">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a><span data-ttu-id="ceb6f-108">Member</span><span class="sxs-lookup"><span data-stu-id="ceb6f-108">Members</span></span>

<span data-ttu-id="ceb6f-109">Die **ieaxisysteminstaller** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ceb6f-109">The **IeAxiSystemInstaller** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ceb6f-110">**Ieaxisysteminstaller** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ceb6f-110">**IeAxiSystemInstaller** also has these types of members:</span></span>

-   [<span data-ttu-id="ceb6f-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="ceb6f-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ceb6f-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="ceb6f-112">Methods</span></span>

<span data-ttu-id="ceb6f-113">Die **ieaxisysteminstaller** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="ceb6f-113">The **IeAxiSystemInstaller** interface has these methods.</span></span>



| <span data-ttu-id="ceb6f-114">Methode</span><span class="sxs-lookup"><span data-stu-id="ceb6f-114">Method</span></span>                                                                              | <span data-ttu-id="ceb6f-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ceb6f-115">Description</span></span>                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="ceb6f-116">**Initializesysteminstaller**</span><span class="sxs-lookup"><span data-stu-id="ceb6f-116">**InitializeSystemInstaller**</span></span>](ieaxisysteminstaller-initializesysteminstaller.md) | <span data-ttu-id="ceb6f-117">Installiert das angegebene ActiveX-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ceb6f-117">Installs the specified ActiveX object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ceb6f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ceb6f-118">Requirements</span></span>



| <span data-ttu-id="ceb6f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ceb6f-119">Requirement</span></span> | <span data-ttu-id="ceb6f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ceb6f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb6f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ceb6f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ceb6f-122">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ceb6f-122">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ceb6f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ceb6f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ceb6f-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ceb6f-124">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="ceb6f-125">IID</span><span class="sxs-lookup"><span data-stu-id="ceb6f-125">IID</span></span><br/>                      | <span data-ttu-id="ceb6f-126">IID \_ ieaxisysteminstaller ist als a50ea6f8-4764-4299-b309-022b2a8b4d8d definiert.</span><span class="sxs-lookup"><span data-stu-id="ceb6f-126">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



 

