---
description: Weitere Informationen finden Sie unter Instanzklasse.
title: Instanzklasse
TOCTitle: Instance class
ms:assetid: T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance(v=EXCHG.10)
ms:contentKeyID: 55103260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be11bc87b1a7969b1c0ddca6640979be0aadae3715a4c2e825ca470ee7932ed8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731750"
---
# <a name="instance-class"></a>Instanzklasse

Eine Klasse, die eine [Klasse](./jet-instance-structure.md) JET_INSTANCE in einem verwerfbar-Objekt kapselt. Die Instanz muss zuletzt geschlossen werden, und das Schließen der Instanz gibt alle anderen Ressourcen für die Instanz frei.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Runtime.ConstrainedExecution.CriticalFinalizerObject](/dotnet/api/system.runtime.constrainedexecution.criticalfinalizerobject)  
    [System.Runtime.InteropServices.SafeHandle](/dotnet/api/system.runtime.interopservices.safehandle)  
      [Microsoft.Win32.SafeHandles.SafeHandleZeroOrMinusOneIsInvalid](/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid)  
        Microsoft.Isam.Esent.Interop.Instance  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Class Instance _
    Inherits SafeHandleZeroOrMinusOneIsInvalid
'Usage
Dim instance As Instance
```

``` csharp
public class Instance : SafeHandleZeroOrMinusOneIsInvalid
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Instanzmitglieder](./instance-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
