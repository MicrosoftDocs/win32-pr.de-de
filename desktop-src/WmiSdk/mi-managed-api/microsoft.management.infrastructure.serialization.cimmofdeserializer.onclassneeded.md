---
description: 'Weitere Informationen finden Sie unter: cimmufdeserializer. onclasserforderliche Delegat (String, String, String)'
title: CimMofDeserializer.OnClassNeeded-Delegat (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.OnClassNeeded delegate (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
- Microsoft::Management::Infrastructure::Serialization::CimMofDeserializer::OnClassNeeded
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded..ctor
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.BeginInvoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.Invoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.EndInvoke
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 50e107c09eccde03446278516a1f125f4ad86022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357421"
---
# <a name="cimmofdeserializeronclassneeded-delegate-string-string-string"></a><span data-ttu-id="0e1e8-103">Cimmufdeserializer. onclassbenögendelegat (Zeichenfolge, Zeichenfolge, Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="0e1e8-103">CimMofDeserializer.OnClassNeeded delegate (String, String, String)</span></span>

<span data-ttu-id="0e1e8-104">Stellt einen Rückruf zum Abrufen einer CIM-Klasse für den angegebenen Server, Namespace und Klassennamen dar.</span><span class="sxs-lookup"><span data-stu-id="0e1e8-104">Represents a callback to retrieve a CIM class for the specified server, namespace, and class name.</span></span>

<span data-ttu-id="0e1e8-105">**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e1e8-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="0e1e8-106">**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="0e1e8-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="0e1e8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e1e8-107">Syntax</span></span>

``` csharp
public delegate CimClass OnClassNeeded(
    string serverName,
    string namespaceName,
    string className
)
```

``` c++
public delegate CimClass^ OnClassNeeded(
    String^ serverName,
    String^ namespaceName,
    String^ className
)
```

``` fsharp
type OnClassNeeded = 
    delegate of 
        serverName:string *
        namespaceName:string *
        className:string -> CimClass
```

``` vb
Public Delegate Function OnClassNeeded (
    serverName As String,
    namespaceName As String,
    className As String,
) As CimClass
```

#### <a name="parameters"></a><span data-ttu-id="0e1e8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e1e8-108">Parameters</span></span>

  - <span data-ttu-id="0e1e8-109">serverName</span><span class="sxs-lookup"><span data-stu-id="0e1e8-109">serverName</span></span>  
    <span data-ttu-id="0e1e8-110">Typ: [System. String](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="0e1e8-110">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="0e1e8-111">Der Name des Servers für die CIM-Klasse.</span><span class="sxs-lookup"><span data-stu-id="0e1e8-111">The name of the server for the CIM class.</span></span>

<!-- end list -->

  - <span data-ttu-id="0e1e8-112">namespaceName</span><span class="sxs-lookup"><span data-stu-id="0e1e8-112">namespaceName</span></span>  
    <span data-ttu-id="0e1e8-113">Typ: [System. String](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="0e1e8-113">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="0e1e8-114">Der Name des Namespace für die CIM-Klasse.</span><span class="sxs-lookup"><span data-stu-id="0e1e8-114">The name of the namespace for the CIM class.</span></span>

<!-- end list -->

  - <span data-ttu-id="0e1e8-115">className</span><span class="sxs-lookup"><span data-stu-id="0e1e8-115">className</span></span>  
    <span data-ttu-id="0e1e8-116">Typ: [System. String](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="0e1e8-116">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="0e1e8-117">Der Name der Klasse für die CIM-Klasse.</span><span class="sxs-lookup"><span data-stu-id="0e1e8-117">The name of the class for the CIM class.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0e1e8-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e1e8-118">Return Value</span></span>

<span data-ttu-id="0e1e8-119">Type: [cimclass-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e1e8-119">Type: [CimClass class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))</span></span>

<span data-ttu-id="0e1e8-120">Gibt die CIM-Klasse zurück, die den angegebenen Argumenten entspricht, oder **null** , wenn die Klasse nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="0e1e8-120">Returns the CIM class corresponding to the specified arguments, or **null** if the class can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e1e8-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0e1e8-121">See Also</span></span>

<span data-ttu-id="0e1e8-122">[Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0e1e8-122">[Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
