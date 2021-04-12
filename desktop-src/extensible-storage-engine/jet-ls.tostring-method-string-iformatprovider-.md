---
description: 'Weitere Informationen finden Sie hier: JET_LS. Methode "destring" (String, IFormatProvider)'
title: JET_LS. Methode "destring" (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.tostring(v=EXCHG.10)
ms:contentKeyID: 39512228
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9979a10ea3afe41a995661f1af8eac8cba80cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217064"
---
# <a name="jet_lstostring-method-string-iformatprovider"></a><span data-ttu-id="042d1-103">JET_LS. Methode "destring" (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="042d1-103">JET_LS.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="042d1-104">Formatiert den Wert der aktuellen Instanz mit dem angegebenen Format.</span><span class="sxs-lookup"><span data-stu-id="042d1-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="042d1-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="042d1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="042d1-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="042d1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="042d1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="042d1-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_LS
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

#### <a name="parameters"></a><span data-ttu-id="042d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="042d1-108">Parameters</span></span>

  - <span data-ttu-id="042d1-109">format</span><span class="sxs-lookup"><span data-stu-id="042d1-109">format</span></span>  
    <span data-ttu-id="042d1-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="042d1-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="042d1-111">Die [Zeichenfolge](/dotnet/api/system.string) , die das zu verwendende Format angibt.</span><span class="sxs-lookup"><span data-stu-id="042d1-111">The [String](/dotnet/api/system.string) specifying the format to use.</span></span> <span data-ttu-id="042d1-112">-oder-NULL, um das für den Typ der [IFormattable](/dotnet/api/system.iformattable) -Implementierung definierte Standardformat zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="042d1-112">-or- null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="042d1-113">Format Provider</span><span class="sxs-lookup"><span data-stu-id="042d1-113">formatProvider</span></span>  
    <span data-ttu-id="042d1-114">Typ: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="042d1-114">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="042d1-115">Der [IFormatProvider](/dotnet/api/system.iformatprovider) , der zum Formatieren des Werts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="042d1-115">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value.</span></span> <span data-ttu-id="042d1-116">-oder-NULL zum Abrufen der numerischen Formatinformationen aus der aktuellen Gebiets Schema Einstellung des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="042d1-116">-or- null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="042d1-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="042d1-117">Return value</span></span>

<span data-ttu-id="042d1-118">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="042d1-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="042d1-119">Eine [Zeichenfolge](/dotnet/api/system.string) , die den Wert der aktuellen Instanz im angegebenen Format enthält.</span><span class="sxs-lookup"><span data-stu-id="042d1-119">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="042d1-120">Implementiert</span><span class="sxs-lookup"><span data-stu-id="042d1-120">Implements</span></span>

[<span data-ttu-id="042d1-121">IFormattable. to String (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="042d1-121">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="042d1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="042d1-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="042d1-123">Referenz</span><span class="sxs-lookup"><span data-stu-id="042d1-123">Reference</span></span>

[<span data-ttu-id="042d1-124">JET_LS Struktur</span><span class="sxs-lookup"><span data-stu-id="042d1-124">JET_LS structure</span></span>](./jet-ls-structure.md)

[<span data-ttu-id="042d1-125">Mitglieder JET_LS</span><span class="sxs-lookup"><span data-stu-id="042d1-125">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="042d1-126">Überladung von ""</span><span class="sxs-lookup"><span data-stu-id="042d1-126">ToString overload</span></span>](./jet-ls.tostring-method2.md)

[<span data-ttu-id="042d1-127">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="042d1-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
