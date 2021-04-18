---
title: NPS-Erweiterungsfunktionen
description: NPS-Erweiterungsfunktionen
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338476"
---
# <a name="nps-extensions-functions"></a><span data-ttu-id="63cea-103">NPS-Erweiterungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="63cea-103">NPS Extensions Functions</span></span>

> [!Note]  
> <span data-ttu-id="63cea-104">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="63cea-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="63cea-105">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="63cea-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="63cea-106">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="63cea-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

## <a name="application-defined"></a><span data-ttu-id="63cea-107">Anwendung definiert</span><span class="sxs-lookup"><span data-stu-id="63cea-107">Application Defined</span></span>

<span data-ttu-id="63cea-108">Die Architektur für NPS-Erweiterungs-DLLs unterstützt die folgenden exportierten Funktionen:</span><span class="sxs-lookup"><span data-stu-id="63cea-108">The architecture for NPS Extension DLLs supports the following exported functions:</span></span>

-   [<span data-ttu-id="63cea-109">**Radiusextensionfreattribute**</span><span class="sxs-lookup"><span data-stu-id="63cea-109">**RadiusExtensionFreeAttributes**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [<span data-ttu-id="63cea-110">**Radiusextensioninit**</span><span class="sxs-lookup"><span data-stu-id="63cea-110">**RadiusExtensionInit**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [<span data-ttu-id="63cea-111">**Radiusextensionprocess**</span><span class="sxs-lookup"><span data-stu-id="63cea-111">**RadiusExtensionProcess**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [<span data-ttu-id="63cea-112">**Radiusextensionprocessex**</span><span class="sxs-lookup"><span data-stu-id="63cea-112">**RadiusExtensionProcessEx**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [<span data-ttu-id="63cea-113">**RadiusExtensionProcess2**</span><span class="sxs-lookup"><span data-stu-id="63cea-113">**RadiusExtensionProcess2**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [<span data-ttu-id="63cea-114">**Radiusextensionterm**</span><span class="sxs-lookup"><span data-stu-id="63cea-114">**RadiusExtensionTerm**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

<span data-ttu-id="63cea-115">Die Funktionen [**radiusextensioninit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) und [**radiusextensionterm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) sind optional.</span><span class="sxs-lookup"><span data-stu-id="63cea-115">The [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) and [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) functions are optional.</span></span>

<span data-ttu-id="63cea-116">Die Erweiterungs-DLL kann [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) anstelle von [**radiusextensionprocess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) oder [**radiusextensionprocessex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)exportieren.</span><span class="sxs-lookup"><span data-stu-id="63cea-116">The Extension DLL may export [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) instead of [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) or [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).</span></span>

<span data-ttu-id="63cea-117">Wenn die Erweiterungs-DLL [**radiusextensionprocessex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)exportiert, muss auch [**radiusextensionfretribute**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="63cea-117">If the Extension DLL exports [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), then it must also export [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).</span></span>

## <a name="system-defined"></a><span data-ttu-id="63cea-118">System definiert</span><span class="sxs-lookup"><span data-stu-id="63cea-118">System Defined</span></span>

<span data-ttu-id="63cea-119">Wenn NPS eine Implementierung von [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)aufruft, übergibt NPS der Funktion einen Zeiger auf eine [**RADIUS- \_ Erweiterungs \_ Steuerungs \_ Block**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) Struktur.</span><span class="sxs-lookup"><span data-stu-id="63cea-119">When NPS calls an implementation of [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS passes the function a pointer to a [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure.</span></span>

<span data-ttu-id="63cea-120">Die [**RADIUS- \_ Erweiterungs \_ Steuerungs \_ Block**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) -Struktur enthält Funktionszeiger auf die folgenden Funktionen, die von NPS bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="63cea-120">The [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="63cea-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63cea-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span></span>
-   <span data-ttu-id="63cea-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63cea-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span></span>
-   <span data-ttu-id="63cea-123">[**Der Typ ""**](/previous-versions/ms688462(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63cea-123">[**SetResponseType**](/previous-versions/ms688462(v=vs.85))</span></span>

<span data-ttu-id="63cea-124">Die Funktionen [**GetRequest**](/previous-versions/ms688263(v=vs.85)) und [**GetResponse**](/previous-versions/ms688270(v=vs.85)) geben Zeiger auf eine Struktur vom Typ [**RADIUS- \_ Attribut \_ Array**](/windows/desktop/api/authif/ns-authif-radius_attribute_array)zurück.</span><span class="sxs-lookup"><span data-stu-id="63cea-124">The functions [**GetRequest**](/previous-versions/ms688263(v=vs.85)) and [**GetResponse**](/previous-versions/ms688270(v=vs.85)) return pointers to a structure of type [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).</span></span>

<span data-ttu-id="63cea-125">Die [**Array Struktur des RADIUS- \_ Attributs \_**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) enthält Funktionszeiger auf die folgenden Funktionen, die von NPS bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="63cea-125">The [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="63cea-126">[**Hinzufügen**](/previous-versions/ms688246(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63cea-126">[**Add**](/previous-versions/ms688246(v=vs.85))</span></span>
-   <span data-ttu-id="63cea-127">[**Attributeat**](/previous-versions/ms688253(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63cea-127">[**AttributeAt**](/previous-versions/ms688253(v=vs.85))</span></span>
-   <span data-ttu-id="63cea-128">[**GetSize**](/previous-versions/ms688277(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63cea-128">[**GetSize**](/previous-versions/ms688277(v=vs.85))</span></span>
-   <span data-ttu-id="63cea-129">[**InsertAt**](/previous-versions/ms688296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63cea-129">[**InsertAt**](/previous-versions/ms688296(v=vs.85))</span></span>
-   <span data-ttu-id="63cea-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63cea-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span></span>
-   <span data-ttu-id="63cea-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="63cea-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span></span>

 

 