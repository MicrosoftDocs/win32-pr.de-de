---
description: 'Weitere Informationen finden Sie hier: JET_OSSNAPID. Methode "destring" (String, IFormatProvider)'
title: JET_OSSNAPID. Methode "destring" (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.tostring(v=EXCHG.10)
ms:contentKeyID: 39512151
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 95e93fd3a6bbf7f2fa3505fcb9480367b780ecc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363743"
---
# <a name="jet_ossnapidtostring-method-string-iformatprovider"></a><span data-ttu-id="4d729-103">JET_OSSNAPID. Methode "destring" (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="4d729-103">JET_OSSNAPID.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="4d729-104">Formatiert den Wert der aktuellen Instanz mit dem angegebenen Format.</span><span class="sxs-lookup"><span data-stu-id="4d729-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="4d729-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4d729-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4d729-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4d729-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4d729-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d729-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_OSSNAPID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a><span data-ttu-id="4d729-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d729-108">Parameters</span></span>

  - <span data-ttu-id="4d729-109">format</span><span class="sxs-lookup"><span data-stu-id="4d729-109">format</span></span>  
    <span data-ttu-id="4d729-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4d729-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4d729-111">Die [Zeichenfolge](/dotnet/api/system.string) , die das zu verwendende Format angibt.</span><span class="sxs-lookup"><span data-stu-id="4d729-111">The [String](/dotnet/api/system.string) specifying the format to use.</span></span> <span data-ttu-id="4d729-112">-oder-NULL, um das für den Typ der [IFormattable](/dotnet/api/system.iformattable) -Implementierung definierte Standardformat zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4d729-112">-or- null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="4d729-113">Format Provider</span><span class="sxs-lookup"><span data-stu-id="4d729-113">formatProvider</span></span>  
    <span data-ttu-id="4d729-114">Typ: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="4d729-114">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="4d729-115">Der [IFormatProvider](/dotnet/api/system.iformatprovider) , der zum Formatieren des Werts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d729-115">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value.</span></span> <span data-ttu-id="4d729-116">-oder-NULL zum Abrufen der numerischen Formatinformationen aus der aktuellen Gebiets Schema Einstellung des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="4d729-116">-or- null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4d729-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d729-117">Return value</span></span>

<span data-ttu-id="4d729-118">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4d729-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="4d729-119">Eine [Zeichenfolge](/dotnet/api/system.string) , die den Wert der aktuellen Instanz im angegebenen Format enthält.</span><span class="sxs-lookup"><span data-stu-id="4d729-119">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="4d729-120">Implementiert</span><span class="sxs-lookup"><span data-stu-id="4d729-120">Implements</span></span>

[<span data-ttu-id="4d729-121">IFormattable. to String (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="4d729-121">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="4d729-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d729-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4d729-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="4d729-123">Reference</span></span>

[<span data-ttu-id="4d729-124">JET_OSSNAPID Struktur</span><span class="sxs-lookup"><span data-stu-id="4d729-124">JET_OSSNAPID structure</span></span>](./jet-ossnapid-structure.md)

[<span data-ttu-id="4d729-125">Mitglieder JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="4d729-125">JET_OSSNAPID members</span></span>](./jet-ossnapid-members.md)

[<span data-ttu-id="4d729-126">Überladung von ""</span><span class="sxs-lookup"><span data-stu-id="4d729-126">ToString overload</span></span>](./jet-ossnapid.tostring-method.md)

[<span data-ttu-id="4d729-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="4d729-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
