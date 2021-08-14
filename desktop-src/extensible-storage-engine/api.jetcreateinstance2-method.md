---
description: 'Weitere Informationen finden Sie unter: Api.JetCreateInstance2-Methode'
title: Api.JetCreateInstance2-Methode
TOCTitle: 'JetCreateInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String,System.String,Microsoft.Isam.Esent.Interop.CreateInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance2(v=EXCHG.10)
ms:contentKeyID: 55100675
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46313c3307db53084b88cd1d8b495a4368abe4412ed9ab99f76430d48435dfed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117719258"
---
# <a name="apijetcreateinstance2-method"></a>Api.JetCreateInstance2-Methode

Zuordnen einer neuen Instanz der Datenbank-Engine zur Verwendung in einem einzelnen Prozess mit einem angegebenen Anzeigenamen.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetCreateInstance2 ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String, _
    displayName As String, _
    grbit As CreateInstanceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As String
Dim displayName As String
Dim grbit As CreateInstanceGrbitApi.JetCreateInstance2(instance, _
    name, displayName, grbit)
```

``` csharp
public static void JetCreateInstance2(
    out JET_INSTANCE instance,
    string name,
    string displayName,
    CreateInstanceGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Gibt die neu erstellte Instanz zurück.

<!-- end list -->

  - name  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Gibt einen eindeutigen Zeichenfolgenbezeichner für die zu erstellende Instanz an. Diese Zeichenfolge muss innerhalb eines bestimmten Prozesses, der die Datenbank-Engine hostet, eindeutig sein.

<!-- end list -->

  - displayName  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Ein Anzeigename für die zu erstellende Instanz. Dies wird in Ereignisprotokolleinträgen verwendet.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.CreateInstanceGrbit](./createinstancegrbit-enumeration.md)  
    
    Erstellungsoptionen,

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
