---
description: 'Weitere Informationen finden Sie unter: Konvertierungen. compareoptionsfromlcmapflags-Methode'
title: Konvertierungen. compareoptionsfromlcmapflags-Methode
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79e0d6a92aef75f3758adc16e9c82de81b8c6962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214920"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a><span data-ttu-id="a3529-103">Konvertierungen. compareoptionsfromlcmapflags-Methode</span><span class="sxs-lookup"><span data-stu-id="a3529-103">Conversions.CompareOptionsFromLCMapFlags method</span></span>

<span data-ttu-id="a3529-104">Die angegebenen Flags für lcmapflags werden in Vergleichs Optionen umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="a3529-104">Given flags for LCMapFlags, turn them into compare options.</span></span> <span data-ttu-id="a3529-105">Unbekannte Optionen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a3529-105">Unknown options are ignored.</span></span>

<span data-ttu-id="a3529-106">Diese API ist nicht CLS-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a3529-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="a3529-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a3529-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a3529-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a3529-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a3529-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3529-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a><span data-ttu-id="a3529-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3529-110">Parameters</span></span>

  - <span data-ttu-id="a3529-111">lcmapflags</span><span class="sxs-lookup"><span data-stu-id="a3529-111">lcmapFlags</span></span>  
    <span data-ttu-id="a3529-112">Typ: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="a3529-112">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="a3529-113">LCMapString-Flags.</span><span class="sxs-lookup"><span data-stu-id="a3529-113">LCMapString flags.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a3529-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3529-114">Return value</span></span>

<span data-ttu-id="a3529-115">Typ: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="a3529-115">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
<span data-ttu-id="a3529-116">CompareOptions, die die (bekannten) Flags beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a3529-116">CompareOptions describing the (known) flags.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a3529-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3529-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a3529-118">Referenz</span><span class="sxs-lookup"><span data-stu-id="a3529-118">Reference</span></span>

[<span data-ttu-id="a3529-119">Konvertierungs Klasse</span><span class="sxs-lookup"><span data-stu-id="a3529-119">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="a3529-120">Konvertierungs Elemente</span><span class="sxs-lookup"><span data-stu-id="a3529-120">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="a3529-121">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="a3529-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
