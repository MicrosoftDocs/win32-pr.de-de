---
description: 'Weitere Informationen finden Sie hier: Konvertierungen. convertdoublededatetime-Methode'
title: Konvertierungen. convertdoublededatetime-Methode
TOCTitle: 'ConvertDoubleToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime(System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.convertdoubletodatetime(v=EXCHG.10)
ms:contentKeyID: 55101133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1d066780ade3da95f4d4d5500143700f7a7d5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352605"
---
# <a name="conversionsconvertdoubletodatetime-method"></a><span data-ttu-id="1a9d8-103">Konvertierungen. convertdoublededatetime-Methode</span><span class="sxs-lookup"><span data-stu-id="1a9d8-103">Conversions.ConvertDoubleToDateTime method</span></span>

<span data-ttu-id="1a9d8-104">Konvertiert ein Double (OA-Datums-/Uhrzeitformat) in einen DateTime-Wert.</span><span class="sxs-lookup"><span data-stu-id="1a9d8-104">Convert a double (OA date time format) to a DateTime.</span></span> <span data-ttu-id="1a9d8-105">Anders als DateTime. fromuadate löst dies keine Ausnahmen aus.</span><span class="sxs-lookup"><span data-stu-id="1a9d8-105">Unlike DateTime.FromOADate this doesn't throw exceptions.</span></span>

<span data-ttu-id="1a9d8-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1a9d8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1a9d8-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1a9d8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1a9d8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a9d8-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function ConvertDoubleToDateTime ( _
    d As Double _
) As DateTime
'Usage
Dim d As Double
Dim returnValue As DateTime

returnValue = Conversions.ConvertDoubleToDateTime(d)
```

``` csharp
public static DateTime ConvertDoubleToDateTime(
    double d
)
```

#### <a name="parameters"></a><span data-ttu-id="1a9d8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a9d8-109">Parameters</span></span>

  - <span data-ttu-id="1a9d8-110">d</span><span class="sxs-lookup"><span data-stu-id="1a9d8-110">d</span></span>  
    <span data-ttu-id="1a9d8-111">Typ: [System. Double](/dotnet/api/system.double)</span><span class="sxs-lookup"><span data-stu-id="1a9d8-111">Type: [System.Double](/dotnet/api/system.double)</span></span>  
    
    <span data-ttu-id="1a9d8-112">Der Double-Wert.</span><span class="sxs-lookup"><span data-stu-id="1a9d8-112">The double value.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1a9d8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a9d8-113">Return value</span></span>

<span data-ttu-id="1a9d8-114">Typ: [System. DateTime](/dotnet/api/system.datetime)</span><span class="sxs-lookup"><span data-stu-id="1a9d8-114">Type: [System.DateTime](/dotnet/api/system.datetime)</span></span>  
<span data-ttu-id="1a9d8-115">Ein DateTime-Wert.</span><span class="sxs-lookup"><span data-stu-id="1a9d8-115">A DateTime.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1a9d8-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a9d8-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1a9d8-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="1a9d8-117">Reference</span></span>

[<span data-ttu-id="1a9d8-118">Konvertierungs Klasse</span><span class="sxs-lookup"><span data-stu-id="1a9d8-118">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="1a9d8-119">Konvertierungs Elemente</span><span class="sxs-lookup"><span data-stu-id="1a9d8-119">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="1a9d8-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="1a9d8-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
