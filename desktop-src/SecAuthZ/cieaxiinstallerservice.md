---
description: Implementiert die Schnittstellen iaxiservice und ieaxiservicecallback.
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: Cieaxiinstallerservice-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: b5ae7ec2a2c904a523f3388fa08a3bf2e44fec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959007"
---
# <a name="cieaxiinstallerservice-object"></a><span data-ttu-id="e977a-103">Cieaxiinstallerservice-Objekt</span><span class="sxs-lookup"><span data-stu-id="e977a-103">CIeAxiInstallerService object</span></span>

<span data-ttu-id="e977a-104">Das **cieaxiinstallerservice** -Objekt implementiert die [**iaxiservice**](ieaxiservice.md) -und [**ieaxiservicecallback**](ieaxiservicecallback.md) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="e977a-104">The **CIeAxiInstallerService** object implements the [**IAxiService**](ieaxiservice.md) and [**IeAxiServiceCallback**](ieaxiservicecallback.md) interfaces.</span></span>

<span data-ttu-id="e977a-105">Dieses Objekt ist nicht in einem öffentlichen Header deklariert.</span><span class="sxs-lookup"><span data-stu-id="e977a-105">This object is not declared in a public header.</span></span> <span data-ttu-id="e977a-106">Anwendungen müssen es selbst definieren.</span><span class="sxs-lookup"><span data-stu-id="e977a-106">Applications must define it themselves.</span></span> <span data-ttu-id="e977a-107">Das folgende IDL-Fragment (Interface Definition Language) beschreibt dieses Objekt, einschließlich seiner CLSID.</span><span class="sxs-lookup"><span data-stu-id="e977a-107">The following Interface Definition Language (IDL) fragment describes this object, including its CLSID.</span></span>

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a><span data-ttu-id="e977a-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e977a-108">Requirements</span></span>



| <span data-ttu-id="e977a-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e977a-109">Requirement</span></span> | <span data-ttu-id="e977a-110">Wert</span><span class="sxs-lookup"><span data-stu-id="e977a-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e977a-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e977a-111">Minimum supported client</span></span><br/> | <span data-ttu-id="e977a-112">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e977a-112">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e977a-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e977a-113">Minimum supported server</span></span><br/> | <span data-ttu-id="e977a-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e977a-114">None supported</span></span><br/>                                                                                 |



## <a name="see-also"></a><span data-ttu-id="e977a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e977a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e977a-116">**Iaxiservice**</span><span class="sxs-lookup"><span data-stu-id="e977a-116">**IAxiService**</span></span>](ieaxiservice.md)
</dt> <dt>

[<span data-ttu-id="e977a-117">**Ieaxiservicecallback**</span><span class="sxs-lookup"><span data-stu-id="e977a-117">**IeAxiServiceCallback**</span></span>](ieaxiservicecallback.md)
</dt> </dl>

 

 




