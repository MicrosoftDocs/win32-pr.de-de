---
title: Beispiel für Registrierungs Werte
description: Das folgende Beispiel zeigt mögliche Daten für einige der Registrierungs Werte für das Authentifizierungsprotokoll.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104038400"
---
# <a name="registry-values-example"></a><span data-ttu-id="6b485-103">Beispiel für Registrierungs Werte</span><span class="sxs-lookup"><span data-stu-id="6b485-103">Registry Values Example</span></span>

<span data-ttu-id="6b485-104">Das folgende Beispiel zeigt mögliche Daten für einige der Registrierungs Werte für das Authentifizierungsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="6b485-104">The following example shows possible data for some of the authentication protocol registry values.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| <span data-ttu-id="6b485-105">Schlüsselname</span><span class="sxs-lookup"><span data-stu-id="6b485-105">Key Name</span></span>            | <span data-ttu-id="6b485-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6b485-106">Datatype</span></span>        | <span data-ttu-id="6b485-107">Wert</span><span class="sxs-lookup"><span data-stu-id="6b485-107">Value</span></span>                                  |
|---------------------|-----------------|----------------------------------------|
| <span data-ttu-id="6b485-108">Pfad</span><span class="sxs-lookup"><span data-stu-id="6b485-108">Path</span></span>                | <span data-ttu-id="6b485-109">REG \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="6b485-109">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="6b485-110">% Systemroot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="6b485-110">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="6b485-111">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b485-111">FriendlyName</span></span>        | <span data-ttu-id="6b485-112">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="6b485-112">REG\_SZ</span></span>         | <span data-ttu-id="6b485-113">EAP-Beispiel Protokoll</span><span class="sxs-lookup"><span data-stu-id="6b485-113">Sample EAP Protocol</span></span>                    |
| <span data-ttu-id="6b485-114">Configuipath</span><span class="sxs-lookup"><span data-stu-id="6b485-114">ConfigUIPath</span></span>        | <span data-ttu-id="6b485-115">REG \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="6b485-115">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="6b485-116">% Systemroot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="6b485-116">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="6b485-117">Identitypath</span><span class="sxs-lookup"><span data-stu-id="6b485-117">IdentityPath</span></span>        | <span data-ttu-id="6b485-118">REG \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="6b485-118">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="6b485-119">% Systemroot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="6b485-119">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="6b485-120">Interactiveuipath</span><span class="sxs-lookup"><span data-stu-id="6b485-120">InteractiveUIPath</span></span>   | <span data-ttu-id="6b485-121">REG \_ Expand \_ SZ</span><span class="sxs-lookup"><span data-stu-id="6b485-121">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="6b485-122">% Systemroot% \\ system32 \\sample.dll</span><span class="sxs-lookup"><span data-stu-id="6b485-122">%SystemRoot%\\system32\\sample.dll</span></span>     |
| <span data-ttu-id="6b485-123">Requirements configui</span><span class="sxs-lookup"><span data-stu-id="6b485-123">RequireConfigUI</span></span>     | <span data-ttu-id="6b485-124">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="6b485-124">REG\_DWORD</span></span>      | <span data-ttu-id="6b485-125">1</span><span class="sxs-lookup"><span data-stu-id="6b485-125">1</span></span>                                      |
| <span data-ttu-id="6b485-126">Configclsid</span><span class="sxs-lookup"><span data-stu-id="6b485-126">ConfigCLSID</span></span>         | <span data-ttu-id="6b485-127">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="6b485-127">REG\_SZ</span></span>         | <span data-ttu-id="6b485-128">{0000031a-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="6b485-128">{0000031A-0000-0000-C000-000000000046}</span></span> |
| <span data-ttu-id="6b485-129">Standalonesupportiert</span><span class="sxs-lookup"><span data-stu-id="6b485-129">StandaloneSupported</span></span> | <span data-ttu-id="6b485-130">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="6b485-130">REG\_DWORD</span></span>      | <span data-ttu-id="6b485-131">1</span><span class="sxs-lookup"><span data-stu-id="6b485-131">1</span></span>                                      |



 

 

 




