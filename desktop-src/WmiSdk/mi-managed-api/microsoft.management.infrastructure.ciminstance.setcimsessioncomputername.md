---
description: 'Weitere Informationen finden Sie unter: ciminstance. setcimsessioncomputername-Methode (String)'
title: CimInstance.SetCimSessionComputerName-Methode (Microsoft.Management.Infrastructure)
TOCTitle: CimInstance.SetCimSessionComputerName method (Microsoft.Management.Infrastructure)
ms:assetid: M:Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName(System.String)
ms.date: 11/12/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName
- Microsoft::Management::Infrastructure::CimInstance::SetCimSessionComputerName
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: b9f4cd9d308617a2369eaa542705e4ad7f854fa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346498"
---
# <a name="ciminstancesetcimsessioncomputername-method-string"></a><span data-ttu-id="e4364-103">Ciminstance. setcimsessioncomputername-Methode (String)</span><span class="sxs-lookup"><span data-stu-id="e4364-103">CimInstance.SetCimSessionComputerName method (String)</span></span>

<span data-ttu-id="e4364-104">Legt den Namen des Computers fest, der für die CIM-Sitzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4364-104">Sets the name of the computer used for the CIM session.</span></span>

<span data-ttu-id="e4364-105">**Namespace:**   [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="e4364-105">**Namespace:**   [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))</span></span>  
<span data-ttu-id="e4364-106">**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="e4364-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="e4364-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4364-107">Syntax</span></span>

``` csharp
public void SetCimSessionComputerName(
    string computerName
)
```

``` c++
public:
void SetCimSessionComputerName(
    String^ computerName
)
```

``` fsharp
member SetCimSessionComputerName : 
        computerName:string -> unit
```

``` vb
Public Sub SetCimSessionComputerName (
    computerName As String
)
```

#### <a name="parameters"></a><span data-ttu-id="e4364-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4364-108">Parameters</span></span>

  - <span data-ttu-id="e4364-109">computerName</span><span class="sxs-lookup"><span data-stu-id="e4364-109">computerName</span></span>  
    <span data-ttu-id="e4364-110">Typ: [System. String](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="e4364-110">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="e4364-111">Der Name des Computers, der für die CIM-Sitzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4364-111">The name of the computer used for the CIM session.</span></span> <span data-ttu-id="e4364-112">**null** , wenn die aktuelle Instanz nur Client seitig ist, oder, wenn die Instanz von localhost abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e4364-112">**null** if the current instance is client-side only, or if the instance was retrieved from localhost.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4364-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4364-113">See also</span></span>

<span data-ttu-id="e4364-114">[Ciminstance-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="e4364-114">[CimInstance Class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336\(v=vs.85\))</span></span>  
<span data-ttu-id="e4364-115">[Microsoft. Management. Infrastructure-Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="e4364-115">[Microsoft.Management.Infrastructure namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))</span></span>
