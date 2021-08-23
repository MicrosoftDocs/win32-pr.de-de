---
description: 'Weitere Informationen finden Sie unter: EsentMissingLogFileException-Klasse'
title: EsentMissingLogFileException-Klasse
TOCTitle: EsentMissingLogFileException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingLogFileException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissinglogfileexception(v=EXCHG.10)
ms:contentKeyID: 55102306
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingLogFileException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingLogFileException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71a0f6d38869b789817aca861f4017ce3576c0505797e5e7e9ac8a225359e5d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722910"
---
# <a name="esentmissinglogfileexception-class"></a>EsentMissingLogFileException-Klasse

Basisklasse für JET_err. MissingLogFile-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMissingLogFileException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingLogFileException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentMissingLogFileException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingLogFileException : EsentCorruptionException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentMissingLogFileException-Member](./esentmissinglogfileexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
