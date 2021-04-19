---
description: Weitere Informationen finden Sie in der Eigenschaft instanceparameters. maxcursors.
title: Instanceparameters. maxcursors (Eigenschaft)
TOCTitle: 'MaxCursors property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxcursors(v=EXCHG.10)
ms:contentKeyID: 55103565
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxCursors
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxCursors
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 029ff7c41916e668f532be60f018870f30e487ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364248"
---
# <a name="instanceparametersmaxcursors-property"></a>Instanceparameters. maxcursors (Eigenschaft)

Ruft die Anzahl der für diese Instanz reservierten Cursor Ressourcen ab oder legt Sie fest. Eine Cursor Ressource entspricht direkt einer JET_TABLEID.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property MaxCursors As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxCursors

instance.MaxCursors = value
```

``` csharp
public int MaxCursors { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanceparameters-Klasse](./instanceparameters-class.md)

[Instanceparameters-Elemente](./instanceparameters-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
