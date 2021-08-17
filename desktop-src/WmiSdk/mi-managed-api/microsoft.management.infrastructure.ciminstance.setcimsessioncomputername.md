---
description: 'Weitere Informationen finden Sie unter: CimInstance.SetCimSessionComputerName-Methode (String)'
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
ms.openlocfilehash: c3f3c3cbe93710f5f9a796463539ad754c1f2e50ce5524c90a5f639021e716bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131112"
---
# <a name="ciminstancesetcimsessioncomputername-method-string"></a>CimInstance.SetCimSessionComputerName-Methode (String)

Legt den Namen des Computers fest, der für die CIM-Sitzung verwendet wird.

**Namespace:**   [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))  
**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Syntax

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

#### <a name="parameters"></a>Parameter

  - computerName  
    Typ: [System.String](/dotnet/api/system.string?view=netframework-4.8)
    
    Der Name des Computers, der für die CIM-Sitzung verwendet wird. **NULL,** wenn die aktuelle Instanz nur clientseitig ist oder wenn die Instanz von localhost abgerufen wurde.

## <a name="see-also"></a>Weitere Informationen

[CimInstance-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336\(v=vs.85\))  
[Microsoft.Management.Infrastructure-Namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))
