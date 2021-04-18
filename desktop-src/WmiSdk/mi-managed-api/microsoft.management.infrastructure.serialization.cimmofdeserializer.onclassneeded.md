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
# <a name="cimmofdeserializeronclassneeded-delegate-string-string-string"></a>Cimmufdeserializer. onclassbenögendelegat (Zeichenfolge, Zeichenfolge, Zeichenfolge)

Stellt einen Rückruf zum Abrufen einer CIM-Klasse für den angegebenen Server, Namespace und Klassennamen dar.

**Namespace:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Syntax

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

#### <a name="parameters"></a>Parameter

  - serverName  
    Typ: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Der Name des Servers für die CIM-Klasse.

<!-- end list -->

  - namespaceName  
    Typ: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Der Name des Namespace für die CIM-Klasse.

<!-- end list -->

  - className  
    Typ: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Der Name der Klasse für die CIM-Klasse.

#### <a name="return-value"></a>Rückgabewert

Type: [cimclass-Klasse](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))

Gibt die CIM-Klasse zurück, die den angegebenen Argumenten entspricht, oder **null** , wenn die Klasse nicht gefunden werden kann.

## <a name="see-also"></a>Weitere Informationen

[Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
