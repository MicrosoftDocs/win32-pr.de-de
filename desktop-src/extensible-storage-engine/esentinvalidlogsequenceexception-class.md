---
description: 'Weitere Informationen finden Sie unter: esentinvalidlogsequenceexception-Klasse'
title: Esentinvalidlogsequenceexception-Klasse
TOCTitle: EsentInvalidLogSequenceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidlogsequenceexception(v=EXCHG.10)
ms:contentKeyID: 55107285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidLogSequenceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8803298a3202ea151bcb42e5490931c0aba2705
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960601"
---
# <a name="esentinvalidlogsequenceexception-class"></a>Esentinvalidlogsequenceexception-Klasse

Basisklasse für JET_err. Invalidlogsequence-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentdataexception](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentverdertionexception](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. esentinvalidlogsequenceexception  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidLogSequenceException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentInvalidLogSequenceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidLogSequenceException : EsentCorruptionException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentinvalidlogsequenceexception-Member](./esentinvalidlogsequenceexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
