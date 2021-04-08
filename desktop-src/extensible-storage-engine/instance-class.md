---
description: 'Weitere Informationen finden Sie unter: Instanzklasse'
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
ms.openlocfilehash: 7b717286a9d07b7eb17b87354cbe0896cf182f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753313"
---
# <a name="instance-class"></a>Instanzklasse

Eine Klasse, die eine [JET_INSTANCE](./jet-instance-structure.md) in einem verwerfbaren Objekt kapselt. Die Instanz muss zuletzt geschlossen werden, und das Schließen der-Instanz gibt alle anderen Ressourcen für die-Instanz frei.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System. Runtime. einschräninedexecution. CriticalFinalizerObject](/dotnet/api/system.runtime.constrainedexecution.criticalfinalizerobject)  
    [System.Runtime.InteropServices.SafeHandle](/dotnet/api/system.runtime.interopservices.safehandle)  
      [Microsoft. Win32. SafeHandles. SafeHandleZeroOrMinusOneIsInvalid](/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid)  
        Microsoft. ISAM. ESENT. Interop. Instance  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

#### <a name="reference"></a>Referenz

[Instanzmember](./instance-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
