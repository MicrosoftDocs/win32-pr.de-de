---
description: 'Weitere Informationen finden Sie unter: esentresource-Klasse'
title: Esentresource-Klasse
TOCTitle: EsentResource class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource(v=EXCHG.10)
ms:contentKeyID: 55102575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 607fb59d6f9f89c33e685ed411ae9dc95eaa6818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346990"
---
# <a name="esentresource-class"></a>Esentresource-Klasse

Dies ist die Basisklasse für alle ESENT-Ressourcen Objekte. Unterklassen dieser Klasse können nicht verwaltete Ressourcen zuordnen und freigeben.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  Microsoft. ISAM. ESENT. Interop. esentresource  
    [Microsoft. ISAM. ESENT. Interop. Session](./session-class.md)  
    [Microsoft. ISAM. ESENT. Interop. Table](./table-class.md)  
    [Microsoft. ISAM. ESENT. Interop. Transaction](./transaction-class.md)  
    [Microsoft. ISAM. ESENT. Interop. Update](./update-class.md)  
    [Microsoft. ISAM. ESENT. Interop. Windows8. durablecommitcallback](./durablecommitcallback-class.md)  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public MustInherit Class EsentResource _
    Implements IDisposable
'Usage
Dim instance As EsentResource
```

``` csharp
public abstract class EsentResource : IDisposable
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentresource-Member](./esentresource-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
