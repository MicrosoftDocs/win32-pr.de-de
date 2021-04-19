---
description: Die Authority-Eigenschaft des "errbemubjectpath"-Objekts enthält eine Zeichenfolge, die die Autoritäts Komponente des Objekt Pfads definiert.
ms.assetid: f00e5759-03b4-4333-b89e-5f54db73c3b7
ms.tgt_platform: multiple
title: Errbemubjectpath. Authority-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Authority
- ISWbemObjectPath.Authority
- ISWbemObjectPath.get_Authority
- ISWbemObjectPath.put_Authority
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2b452f37f9f8d36b33596e032a82441a3507d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357045"
---
# <a name="swbemobjectpathauthority-property"></a><span data-ttu-id="70445-103">Errbemubjectpath. Authority (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="70445-103">SWbemObjectPath.Authority property</span></span>

<span data-ttu-id="70445-104">Die **Authority** -Eigenschaft des " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts enthält eine Zeichenfolge, die die Autoritäts Komponente des Objekt Pfads definiert.</span><span class="sxs-lookup"><span data-stu-id="70445-104">The **Authority** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains a string that defines the Authority component of the object path.</span></span> <span data-ttu-id="70445-105">Weitere Informationen finden Sie unter dem Parameter " *stranauthority* " der Methode " [**Swap. ConnectServer**](swbemlocator-connectserver.md) " und [Festlegen der Sicherheit für IWbemServices und andere](setting-the-security-on-iwbemservices-and-other-proxies.md)Proxys.</span><span class="sxs-lookup"><span data-stu-id="70445-105">For more information, see the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method and [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="70445-106">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="70445-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="70445-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="70445-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="70445-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="70445-108">Syntax</span></span>


```VB
SWbemObjectPath.Authority As String
```



## <a name="property-value"></a><span data-ttu-id="70445-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="70445-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="70445-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70445-110">Requirements</span></span>



| <span data-ttu-id="70445-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70445-111">Requirement</span></span> | <span data-ttu-id="70445-112">Wert</span><span class="sxs-lookup"><span data-stu-id="70445-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70445-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70445-113">Minimum supported client</span></span><br/> | <span data-ttu-id="70445-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70445-114">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="70445-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70445-115">Minimum supported server</span></span><br/> | <span data-ttu-id="70445-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70445-116">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="70445-117">Header</span><span class="sxs-lookup"><span data-stu-id="70445-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="70445-118"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="70445-118"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="70445-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="70445-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="70445-120"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="70445-120"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="70445-121">DLL</span><span class="sxs-lookup"><span data-stu-id="70445-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70445-122"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70445-122"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="70445-123">CLSID</span><span class="sxs-lookup"><span data-stu-id="70445-123">CLSID</span></span><br/>                    | <span data-ttu-id="70445-124">CLSID- \_ Swap-Austausch Pfad</span><span class="sxs-lookup"><span data-stu-id="70445-124">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="70445-125">IID</span><span class="sxs-lookup"><span data-stu-id="70445-125">IID</span></span><br/>                      | <span data-ttu-id="70445-126">IID \_ iswbemubjectpath</span><span class="sxs-lookup"><span data-stu-id="70445-126">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




