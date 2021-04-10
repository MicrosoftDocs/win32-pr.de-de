---
description: 'Weitere Informationen finden Sie unter: esentcolumnnochunkexception-Klasse'
title: Esentcolumnnochunkexception-Klasse
TOCTitle: EsentColumnNoChunkException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnNoChunkException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumnnochunkexception(v=EXCHG.10)
ms:contentKeyID: 55101234
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnNoChunkException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnNoChunkException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57ff408b4d45debc3af98aabc70be2d56ad712ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042525"
---
# <a name="esentcolumnnochunkexception-class"></a>Esentcolumnnochunkexception-Klasse

Basisklasse für JET_err. Columnnochunk-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentapiexception](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentusageexception](./esentusageexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. esentcolumnnochunkexception  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnNoChunkException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnNoChunkException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnNoChunkException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentcolumnnochunkexception-Member](./esentcolumnnochunkexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
