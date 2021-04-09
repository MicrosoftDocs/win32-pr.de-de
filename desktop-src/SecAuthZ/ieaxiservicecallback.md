---
description: Wird von der ieaxisysteminstaller-Schnittstelle aufgerufen, um zu überprüfen, ob ein ActiveX-Objekt installiert werden kann.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: Ieaxiservicecallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869024"
---
# <a name="ieaxiservicecallback-interface"></a><span data-ttu-id="1afbf-103">Ieaxiservicecallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1afbf-103">IeAxiServiceCallback interface</span></span>

<span data-ttu-id="1afbf-104">Die **ieaxiservicecallback** -Schnittstelle wird von der [**ieaxisysteminstaller**](ieaxisysteminstaller.md) -Schnittstelle aufgerufen, um zu überprüfen, ob ein ActiveX-Objekt installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1afbf-104">The **IeAxiServiceCallback** interface is called by the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface to verify that an ActiveX object can be installed.</span></span>

<span data-ttu-id="1afbf-105">Diese Schnittstelle wird von der [**cieaxiinstallerservice**](cieaxiinstallerservice.md) -Klasse implementiert.</span><span class="sxs-lookup"><span data-stu-id="1afbf-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="1afbf-106">Diese Schnittstelle ist nicht in einem öffentlichen Header deklariert.</span><span class="sxs-lookup"><span data-stu-id="1afbf-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="1afbf-107">Anwendungen müssen es selbst definieren.</span><span class="sxs-lookup"><span data-stu-id="1afbf-107">Applications must define it themselves.</span></span> <span data-ttu-id="1afbf-108">Das folgende IDL-Fragment (Interface Definition Language) beschreibt diese Schnittstelle, einschließlich ihrer IID.</span><span class="sxs-lookup"><span data-stu-id="1afbf-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a><span data-ttu-id="1afbf-109">Member</span><span class="sxs-lookup"><span data-stu-id="1afbf-109">Members</span></span>

<span data-ttu-id="1afbf-110">Die **ieaxiservicecallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1afbf-110">The **IeAxiServiceCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1afbf-111">**Ieaxiservicecallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1afbf-111">**IeAxiServiceCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="1afbf-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="1afbf-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1afbf-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="1afbf-113">Methods</span></span>

<span data-ttu-id="1afbf-114">Die **ieaxiservicecallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1afbf-114">The **IeAxiServiceCallback** interface has these methods.</span></span>



| <span data-ttu-id="1afbf-115">Methode</span><span class="sxs-lookup"><span data-stu-id="1afbf-115">Method</span></span>                                                | <span data-ttu-id="1afbf-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1afbf-116">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1afbf-117">**Verifyfile**</span><span class="sxs-lookup"><span data-stu-id="1afbf-117">**VerifyFile**</span></span>](ieaxiservicecallback-verifyfile.md) | <span data-ttu-id="1afbf-118">Führt Sicherheitsüberprüfungen für das angegebene ActiveX-Objekt aus und gibt den Speicherort zurück, an dem die entsprechende CAB-Datei heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="1afbf-118">Performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1afbf-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1afbf-119">Requirements</span></span>



| <span data-ttu-id="1afbf-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1afbf-120">Requirement</span></span> | <span data-ttu-id="1afbf-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1afbf-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1afbf-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1afbf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1afbf-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1afbf-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1afbf-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1afbf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1afbf-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1afbf-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="1afbf-126">IID</span><span class="sxs-lookup"><span data-stu-id="1afbf-126">IID</span></span><br/>                      | <span data-ttu-id="1afbf-127">IID \_ ieaxiservicecallback ist als 1823e7ba-ec36-447a-9b2e-b4912e15afe7 definiert.</span><span class="sxs-lookup"><span data-stu-id="1afbf-127">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



 

