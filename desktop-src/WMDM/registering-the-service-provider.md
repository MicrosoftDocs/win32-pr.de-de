---
title: Registrieren des Dienstanbieters
description: Registrieren des Dienstanbieters
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Media Device Manager, Registrieren von Dienstanbietern
- Device Manager, Registrieren von Dienstanbietern
- Programmier Handbuch, Registrieren von Dienstanbietern
- Dienstanbieter, Registrieren von Dienstanbietern
- Erstellen von Dienstanbietern, Registrieren von Dienstanbietern
- Registrieren von Dienstanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1226b724b06990fc1e000a522e3a61672789cf3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036500"
---
# <a name="registering-the-service-provider"></a><span data-ttu-id="7e6fa-109">Registrieren des Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="7e6fa-109">Registering the Service Provider</span></span>

<span data-ttu-id="7e6fa-110">Ein Dienstanbieter muss nicht nur als COM-Objekt registriert werden, sondern muss als Plug-in für Windows Media Device Manager registriert werden.</span><span class="sxs-lookup"><span data-stu-id="7e6fa-110">In addition to being registered as a COM object, a service provider must be registered as a plug-in to Windows Media Device Manager.</span></span> <span data-ttu-id="7e6fa-111">Ein Dienstanbieter muss den folgenden Registrierungsschlüssel erstellen, um sich zu registrieren:</span><span class="sxs-lookup"><span data-stu-id="7e6fa-111">To register, a service provider must create the following registry key:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

<span data-ttu-id="7e6fa-112">In diesem Schlüssel < der *Name Ihres Dienstanbieters* > der Name der dll ist. beispielsweise verwendet der Beispiel Dienstanbieter mshdsp.</span><span class="sxs-lookup"><span data-stu-id="7e6fa-112">In this key, < *your service provider name* > is the name of your DLL; for example, the sample service provider uses MsHDSP.</span></span> <span data-ttu-id="7e6fa-113">Der ProgID-Schlüssel sollte über einen Zeichen folgen Wert verfügen, der der CLSID Ihres Dienstanbieters entspricht.</span><span class="sxs-lookup"><span data-stu-id="7e6fa-113">The ProgID key should have a string value that corresponds to the CLSID of your service provider.</span></span> <span data-ttu-id="7e6fa-114">Der Beispiel Dienstanbieter hat beispielsweise den Wert "mdserviceproviderhd. mdserviceproviderhd".</span><span class="sxs-lookup"><span data-stu-id="7e6fa-114">For instance, the sample service provider has the value "MDServiceProviderHD.MDServiceProviderHD".</span></span>

<span data-ttu-id="7e6fa-115">Die Implementierung von DllRegisterServer durch den Beispiel Dienstanbieter in mdsp. cpp fügt diesen Registrierungsschlüssel hinzu, wenn Sie die Beispiel-Dienstanbieter-dll registrieren.</span><span class="sxs-lookup"><span data-stu-id="7e6fa-115">The sample service provider's implementation of DLLRegisterServer in Mdsp.cpp adds this registry key when you register the sample service provider DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e6fa-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7e6fa-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e6fa-117">**Erstellen eines Dienstanbieters**</span><span class="sxs-lookup"><span data-stu-id="7e6fa-117">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




