---
description: Initialisiert ein-Systemdienst Objekt, um ein ActiveX-Objekt zu installieren, wenn der aktuelle Benutzer nicht über die Berechtigung zum Installieren des-Objekts verfügt.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: Ieaxiservice-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: 34c4743327b2539616dee6b09c34d9f479aa3303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363258"
---
# <a name="ieaxiservice-interface"></a><span data-ttu-id="0eeee-103">Ieaxiservice-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0eeee-103">IeAxiService interface</span></span>

<span data-ttu-id="0eeee-104">Die **iaxiservice** -Schnittstelle initialisiert ein-Systemdienst Objekt, um ein ActiveX-Objekt zu installieren, wenn der aktuelle Benutzer nicht über die Berechtigung zum Installieren des-Objekts verfügt.</span><span class="sxs-lookup"><span data-stu-id="0eeee-104">The **IAxiService** interface initializes a system service object to install an ActiveX object when the current user does not have permission to install the object.</span></span>

<span data-ttu-id="0eeee-105">Diese Schnittstelle wird von der [**cieaxiinstallerservice**](cieaxiinstallerservice.md) -Klasse implementiert.</span><span class="sxs-lookup"><span data-stu-id="0eeee-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="0eeee-106">Diese Schnittstelle ist nicht in einem öffentlichen Header deklariert.</span><span class="sxs-lookup"><span data-stu-id="0eeee-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="0eeee-107">Anwendungen müssen es selbst definieren.</span><span class="sxs-lookup"><span data-stu-id="0eeee-107">Applications must define it themselves.</span></span> <span data-ttu-id="0eeee-108">Das folgende IDL-Fragment (Interface Definition Language) beschreibt diese Schnittstelle, einschließlich ihrer IID.</span><span class="sxs-lookup"><span data-stu-id="0eeee-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a><span data-ttu-id="0eeee-109">Member</span><span class="sxs-lookup"><span data-stu-id="0eeee-109">Members</span></span>

<span data-ttu-id="0eeee-110">Die **ieaxiservice** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0eeee-110">The **IeAxiService** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0eeee-111">**Ieaxiservice** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0eeee-111">**IeAxiService** also has these types of members:</span></span>

-   [<span data-ttu-id="0eeee-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="0eeee-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0eeee-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="0eeee-113">Methods</span></span>

<span data-ttu-id="0eeee-114">Die **ieaxiservice** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0eeee-114">The **IeAxiService** interface has these methods.</span></span>



| <span data-ttu-id="0eeee-115">Methode</span><span class="sxs-lookup"><span data-stu-id="0eeee-115">Method</span></span>                                        | <span data-ttu-id="0eeee-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0eeee-116">Description</span></span>                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="0eeee-117">**Cleanup**</span><span class="sxs-lookup"><span data-stu-id="0eeee-117">**Cleanup**</span></span>](ieaxiservice-cleanup.md)       | <span data-ttu-id="0eeee-118">Gibt die von der **ieaxiservice** -Schnittstelle verwendeten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="0eeee-118">Frees resources used by the **IeAxiService** interface.</span></span><br/> |
| [<span data-ttu-id="0eeee-119">**Initialisieren**</span><span class="sxs-lookup"><span data-stu-id="0eeee-119">**Initialize**</span></span>](ieaxiservice-initialize.md) | <span data-ttu-id="0eeee-120">Hiermit wird ein ActiveX-Objekt überprüft und heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="0eeee-120">Checks and downloads an ActiveX object.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="0eeee-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0eeee-121">Requirements</span></span>



| <span data-ttu-id="0eeee-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0eeee-122">Requirement</span></span> | <span data-ttu-id="0eeee-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0eeee-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eeee-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0eeee-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0eeee-125">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0eeee-125">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0eeee-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0eeee-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0eeee-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0eeee-127">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="0eeee-128">IID</span><span class="sxs-lookup"><span data-stu-id="0eeee-128">IID</span></span><br/>                      | <span data-ttu-id="0eeee-129">IID \_ ieaxiservice ist definiert als E9E92380-9ecd-4982-A0EB-6815a56ccb27</span><span class="sxs-lookup"><span data-stu-id="0eeee-129">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



 

