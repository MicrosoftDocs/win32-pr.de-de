---
description: 'Weitere Informationen finden Sie unter: esentmemoryexception-Klasse'
title: EsentMemoryException-Klasse
TOCTitle: EsentMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a7090fdedee2969e5dd3658b7068fd8739e9365
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103869375"
---
# <a name="esentmemoryexception-class"></a>EsentMemoryException-Klasse

Basisklasse für Speicher Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentoperationexception](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentresourceexception](./esentresourceexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. esentmemoryexception  
              

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentMemoryException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentMemoryException
```

``` csharp
[SerializableAttribute]
public abstract class EsentMemoryException : EsentResourceException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentmemoryexception-Member](./esentmemoryexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Abgeleitete Typen

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentoperationexception](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentresourceexception](./esentresourceexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. esentmemoryexception  
              [Microsoft. ISAM. ESENT. Interop. esentouesf buffersexception](./esentoutofbuffersexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. esentouyscurrsorsexception](./esentoutofcursorsexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. esentouesffilelenker sexception](./esentoutoffilehandlesexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. esentouesf memoryexception](./esentoutofmemoryexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. esentouyfsessionsexception](./esentoutofsessionsexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. esentouesfthreadsexception](./esentoutofthreadsexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. esentesomanymempoolentriesexception](./esenttoomanymempoolentriesexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. esentesomanyopenindexesexception](./esenttoomanyopenindexesexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. esentesomanysortsexception](./esenttoomanysortsexception-class.md)