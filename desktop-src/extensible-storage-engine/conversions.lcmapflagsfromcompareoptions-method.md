---
description: 'Weitere Informationen finden Sie unter: Konvertierungen. lcmapflagsfromcompareoptions-Methode'
title: Konvertierungen. lcmapflagsfromcompareoptions-Methode
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350503"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a><span data-ttu-id="66235-103">Konvertierungen. lcmapflagsfromcompareoptions-Methode</span><span class="sxs-lookup"><span data-stu-id="66235-103">Conversions.LCMapFlagsFromCompareOptions method</span></span>

<span data-ttu-id="66235-104">Legen Sie CompareOptions fest, und wandeln Sie Sie aus LCMapString in Flags um.</span><span class="sxs-lookup"><span data-stu-id="66235-104">Give CompareOptions, turn them into flags from LCMapString.</span></span> <span data-ttu-id="66235-105">Unbekannte Optionen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="66235-105">Unknown options are ignored.</span></span>

<span data-ttu-id="66235-106">Diese API ist nicht CLS-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="66235-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="66235-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="66235-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="66235-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="66235-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="66235-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="66235-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a><span data-ttu-id="66235-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="66235-110">Parameters</span></span>

  - <span data-ttu-id="66235-111">compareOptions</span><span class="sxs-lookup"><span data-stu-id="66235-111">compareOptions</span></span>  
    <span data-ttu-id="66235-112">Typ: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="66235-112">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
    
    <span data-ttu-id="66235-113">Die Optionen, die konvertiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="66235-113">The options to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="66235-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66235-114">Return value</span></span>

<span data-ttu-id="66235-115">Typ: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="66235-115">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
<span data-ttu-id="66235-116">Die LCMapString-Flags, die den Vergleichs Optionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="66235-116">The LCMapString flags that match the compare options.</span></span> <span data-ttu-id="66235-117">Nicht unterstützte Optionen werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="66235-117">Unsupported options are ignored.</span></span>  

## <a name="see-also"></a><span data-ttu-id="66235-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66235-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="66235-119">Referenz</span><span class="sxs-lookup"><span data-stu-id="66235-119">Reference</span></span>

[<span data-ttu-id="66235-120">Konvertierungs Klasse</span><span class="sxs-lookup"><span data-stu-id="66235-120">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="66235-121">Konvertierungs Elemente</span><span class="sxs-lookup"><span data-stu-id="66235-121">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="66235-122">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="66235-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
