---
description: 'Weitere Informationen finden Sie unter: EsentPageNotInitializedException-Klasse'
title: EsentPageNotInitializedException-Klasse
TOCTitle: EsentPageNotInitializedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpagenotinitializedexception(v=EXCHG.10)
ms:contentKeyID: 55107308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a46a72b09ab440bfcfb7170281ac77f63aaeaa27a267076ea29414428af62fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118261307"
---
# <a name="esentpagenotinitializedexception-class"></a>EsentPageNotInitializedException-Klasse

Basisklasse für JET_err. PageNotInitialized-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPageNotInitializedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentPageNotInitializedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPageNotInitializedException : EsentCorruptionException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[EsentPageNotInitializedException-Member](./esentpagenotinitializedexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
