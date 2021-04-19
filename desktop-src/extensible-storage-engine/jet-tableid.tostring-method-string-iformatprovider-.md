---
description: 'Weitere Informationen finden Sie hier: JET_TABLEID. Methode "destring" (String, IFormatProvider)'
title: JET_TABLEID. Methode "destring" (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.tostring(v=EXCHG.10)
ms:contentKeyID: 39510805
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e8d57d572a44f04c5b76ffb11f5243f7afb2b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353839"
---
# <a name="jet_tableidtostring-method-string-iformatprovider"></a><span data-ttu-id="c11e7-103">JET_TABLEID. Methode "destring" (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="c11e7-103">JET_TABLEID.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="c11e7-104">Formatiert den Wert der aktuellen Instanz mit dem angegebenen Format.</span><span class="sxs-lookup"><span data-stu-id="c11e7-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="c11e7-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c11e7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c11e7-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c11e7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c11e7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c11e7-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_TABLEID
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

#### <a name="parameters"></a><span data-ttu-id="c11e7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c11e7-108">Parameters</span></span>

  - <span data-ttu-id="c11e7-109">format</span><span class="sxs-lookup"><span data-stu-id="c11e7-109">format</span></span>  
    <span data-ttu-id="c11e7-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c11e7-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c11e7-111">Die [Zeichenfolge](/dotnet/api/system.string) , die das zu verwendende Format angibt. oder NULL, um das für den Typ der [IFormattable](/dotnet/api/system.iformattable) -Implementierung definierte Standardformat zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c11e7-111">The [String](/dotnet/api/system.string) specifying the format to use; or, null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="c11e7-112">Format Provider</span><span class="sxs-lookup"><span data-stu-id="c11e7-112">formatProvider</span></span>  
    <span data-ttu-id="c11e7-113">Typ: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="c11e7-113">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="c11e7-114">Der [IFormatProvider](/dotnet/api/system.iformatprovider) , der zum Formatieren des Werts verwendet werden soll. oder NULL, um die numerischen Formatinformationen aus der aktuellen Gebiets Schema Einstellung des Betriebssystems abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c11e7-114">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value; or, null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c11e7-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c11e7-115">Return value</span></span>

<span data-ttu-id="c11e7-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c11e7-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="c11e7-117">Eine [Zeichenfolge](/dotnet/api/system.string) , die den Wert der aktuellen Instanz im angegebenen Format enthält.</span><span class="sxs-lookup"><span data-stu-id="c11e7-117">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="c11e7-118">Implementiert</span><span class="sxs-lookup"><span data-stu-id="c11e7-118">Implements</span></span>

[<span data-ttu-id="c11e7-119">IFormattable. to String (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="c11e7-119">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="c11e7-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c11e7-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c11e7-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="c11e7-121">Reference</span></span>

[<span data-ttu-id="c11e7-122">JET_TABLEID Struktur</span><span class="sxs-lookup"><span data-stu-id="c11e7-122">JET_TABLEID structure</span></span>](./jet-tableid-structure.md)

[<span data-ttu-id="c11e7-123">Mitglieder JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c11e7-123">JET_TABLEID members</span></span>](./jet-tableid-members.md)

[<span data-ttu-id="c11e7-124">Überladung von ""</span><span class="sxs-lookup"><span data-stu-id="c11e7-124">ToString overload</span></span>](./jet-tableid.tostring-method.md)

[<span data-ttu-id="c11e7-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c11e7-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
