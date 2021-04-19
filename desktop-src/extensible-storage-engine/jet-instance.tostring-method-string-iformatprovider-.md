---
description: 'Weitere Informationen finden Sie hier: JET_INSTANCE. Methode "destring" (String, IFormatProvider)'
title: JET_INSTANCE. Methode "destring" (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.tostring(v=EXCHG.10)
ms:contentKeyID: 39511283
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4030a86ed867a2463346dca549acb35809264c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360689"
---
# <a name="jet_instancetostring-method-string-iformatprovider"></a><span data-ttu-id="ef636-103">JET_INSTANCE. Methode "destring" (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="ef636-103">JET_INSTANCE.ToString method (String, IFormatProvider)</span></span>

<span data-ttu-id="ef636-104">Formatiert den Wert der aktuellen Instanz mit dem angegebenen Format.</span><span class="sxs-lookup"><span data-stu-id="ef636-104">Formats the value of the current instance using the specified format.</span></span>

<span data-ttu-id="ef636-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ef636-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ef636-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ef636-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ef636-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef636-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_INSTANCE
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

#### <a name="parameters"></a><span data-ttu-id="ef636-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef636-108">Parameters</span></span>

  - <span data-ttu-id="ef636-109">format</span><span class="sxs-lookup"><span data-stu-id="ef636-109">format</span></span>  
    <span data-ttu-id="ef636-110">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ef636-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ef636-111">Die [Zeichenfolge](/dotnet/api/system.string) , die das zu verwendende Format angibt. oder NULL, um das für den Typ der [IFormattable](/dotnet/api/system.iformattable) -Implementierung definierte Standardformat zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef636-111">The [String](/dotnet/api/system.string) specifying the format to use; or, null to use the default format defined for the type of the [IFormattable](/dotnet/api/system.iformattable) implementation.</span></span>

<!-- end list -->

  - <span data-ttu-id="ef636-112">Format Provider</span><span class="sxs-lookup"><span data-stu-id="ef636-112">formatProvider</span></span>  
    <span data-ttu-id="ef636-113">Typ: [System. IFormatProvider](/dotnet/api/system.iformatprovider)</span><span class="sxs-lookup"><span data-stu-id="ef636-113">Type: [System.IFormatProvider](/dotnet/api/system.iformatprovider)</span></span>  
    
    <span data-ttu-id="ef636-114">Der [IFormatProvider](/dotnet/api/system.iformatprovider) , der zum Formatieren des Werts verwendet werden soll. oder NULL, um die numerischen Formatinformationen aus der aktuellen Gebiets Schema Einstellung des Betriebssystems abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ef636-114">The [IFormatProvider](/dotnet/api/system.iformatprovider) to use to format the value; or, null to obtain the numeric format information from the current locale setting of the operating system.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ef636-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef636-115">Return value</span></span>

<span data-ttu-id="ef636-116">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ef636-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="ef636-117">Eine [Zeichenfolge](/dotnet/api/system.string) , die den Wert der aktuellen Instanz im angegebenen Format enthält.</span><span class="sxs-lookup"><span data-stu-id="ef636-117">A [String](/dotnet/api/system.string) containing the value of the current instance in the specified format.</span></span>  

#### <a name="implements"></a><span data-ttu-id="ef636-118">Implementiert</span><span class="sxs-lookup"><span data-stu-id="ef636-118">Implements</span></span>

[<span data-ttu-id="ef636-119">IFormattable. to String (String, IFormatProvider)</span><span class="sxs-lookup"><span data-stu-id="ef636-119">IFormattable.ToString(String, IFormatProvider)</span></span>](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a><span data-ttu-id="ef636-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef636-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ef636-121">Referenz</span><span class="sxs-lookup"><span data-stu-id="ef636-121">Reference</span></span>

[<span data-ttu-id="ef636-122">JET_INSTANCE Struktur</span><span class="sxs-lookup"><span data-stu-id="ef636-122">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="ef636-123">Mitglieder JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="ef636-123">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="ef636-124">Überladung von ""</span><span class="sxs-lookup"><span data-stu-id="ef636-124">ToString overload</span></span>](./jet-instance.tostring-method2.md)

[<span data-ttu-id="ef636-125">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="ef636-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
