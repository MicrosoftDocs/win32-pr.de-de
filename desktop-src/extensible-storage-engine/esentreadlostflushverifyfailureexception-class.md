---
description: 'Weitere Informationen zu: EsentReadLostFlushVerifyFailureException-Klasse'
title: EsentReadLostFlushVerifyFailureException-Klasse
TOCTitle: EsentReadLostFlushVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentreadlostflushverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102493
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 92e2b4dd0f7d2e27041f801842cf73c353a3ce4f8eba2ce8d8ce7421d342421f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782130"
---
# <a name="esentreadlostflushverifyfailureexception-class"></a>EsentReadLostFlushVerifyFailureException-Klasse

Basisklasse für JET_err. ReadLostFlushVerifyFailure-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentReadLostFlushVerifyFailureException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentReadLostFlushVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentReadLostFlushVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentReadLostFlushVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentReadLostFlushVerifyFailureException-Member](./esentreadlostflushverifyfailureexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
