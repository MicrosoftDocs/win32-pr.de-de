---
description: 'Weitere Informationen finden Sie unter: esentcolumndeobigexception-Klasse'
title: Esentcolumndeobigexception-Klasse
TOCTitle: EsentColumnTooBigException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnTooBigException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumntoobigexception(v=EXCHG.10)
ms:contentKeyID: 55101348
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnTooBigException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnTooBigException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a72ef8849dcbb8854786d126899924f0d835dcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354863"
---
# <a name="esentcolumntoobigexception-class"></a>Esentcolumndeobigexception-Klasse

Basisklasse für JET_err. Columnto obig-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentapiexception](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentusageexception](./esentusageexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. esentcolumndeobigexception  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnTooBigException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnTooBigException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnTooBigException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentcolumndeobigexception-Elemente](./esentcolumntoobigexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
