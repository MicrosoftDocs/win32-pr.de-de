---
description: Die iwbempath-Schnittstelle stellt die folgenden Methoden zur Verfügung.
ms.assetid: 36EC7EF6-5CCA-4D18-AB09-9EE41D1B9524
ms.tgt_platform: multiple
title: Iwbempath-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f1ae802fd7741e5b1317160991a50bd2a535a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215449"
---
# <a name="iwbempath-methods"></a><span data-ttu-id="5271b-103">Iwbempath-Methoden</span><span class="sxs-lookup"><span data-stu-id="5271b-103">IWbemPath Methods</span></span>

<span data-ttu-id="5271b-104">Die [**iwbempath**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbempath) -Schnittstelle stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5271b-104">The [**IWbemPath**](/windows/desktop/api/Wmiutils/nn-wmiutils-iwbempath) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5271b-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5271b-105">In this section</span></span>

-   [<span data-ttu-id="5271b-106">**Methode "kreateclasspart"**</span><span class="sxs-lookup"><span data-stu-id="5271b-106">**CreateClassPart method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-createclasspart)
-   [<span data-ttu-id="5271b-107">**Deleteclasspart-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-107">**DeleteClassPart method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-deleteclasspart)
-   [<span data-ttu-id="5271b-108">**GetClassName-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-108">**GetClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getclassname)
-   [<span data-ttu-id="5271b-109">**GetInfo-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-109">**GetInfo method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getinfo)
-   [<span data-ttu-id="5271b-110">**GetKeyList-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-110">**GetKeyList method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getkeylist)
-   [<span data-ttu-id="5271b-111">**Getnamespaceat-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-111">**GetNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getnamespaceat)
-   [<span data-ttu-id="5271b-112">**Getnamespacecount-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-112">**GetNamespaceCount method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getnamespacecount)
-   [<span data-ttu-id="5271b-113">**GetScope-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-113">**GetScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscope)
-   [<span data-ttu-id="5271b-114">**Getscopeastext-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-114">**GetScopeAsText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscopeastext)
-   [<span data-ttu-id="5271b-115">**Getscopecount-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-115">**GetScopeCount method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getscopecount)
-   [<span data-ttu-id="5271b-116">**GetServer-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-116">**GetServer method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-getserver)
-   [<span data-ttu-id="5271b-117">**GetText-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-117">**GetText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-gettext)
-   [<span data-ttu-id="5271b-118">**IsLocal-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-118">**IsLocal method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-islocal)
-   [<span data-ttu-id="5271b-119">**IsRelative-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-119">**IsRelative method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-isrelative)
-   [<span data-ttu-id="5271b-120">**Isrelativeorchild-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-120">**IsRelativeOrChild method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-isrelativeorchild)
-   [<span data-ttu-id="5271b-121">**Issameclassname-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-121">**IsSameClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-issameclassname)
-   [<span data-ttu-id="5271b-122">**Removeallnamespaces-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-122">**RemoveAllNamespaces method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removeallnamespaces)
-   [<span data-ttu-id="5271b-123">**Removeallscopes-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-123">**RemoveAllScopes method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removeallscopes)
-   [<span data-ttu-id="5271b-124">**Removenamespaceat-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-124">**RemoveNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removenamespaceat)
-   [<span data-ttu-id="5271b-125">**Removescope-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-125">**RemoveScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-removescope)
-   [<span data-ttu-id="5271b-126">**Setclassname-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-126">**SetClassName method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setclassname)
-   [<span data-ttu-id="5271b-127">**Setnamespaceat-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-127">**SetNamespaceAt method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setnamespaceat)
-   [<span data-ttu-id="5271b-128">**SetScope-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-128">**SetScope method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setscope)
-   [<span data-ttu-id="5271b-129">**Setserver-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-129">**SetServer method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-setserver)
-   [<span data-ttu-id="5271b-130">**SetText-Methode**</span><span class="sxs-lookup"><span data-stu-id="5271b-130">**SetText method**</span></span>](/windows/desktop/api/Wmiutils/nf-wmiutils-iwbempath-settext)

 

 



