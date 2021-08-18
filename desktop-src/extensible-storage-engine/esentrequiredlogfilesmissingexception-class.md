---
description: 'Weitere Informationen finden Sie unter: EsentRequiredLogFilesMissingException-Klasse'
title: EsentRequiredLogFilesMissingException-Klasse
TOCTitle: EsentRequiredLogFilesMissingException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrequiredlogfilesmissingexception(v=EXCHG.10)
ms:contentKeyID: 55102617
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a6506704e48a16502599061e1ed0307ebab77c454ef0c4788cf600fcafe9de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115235"
---
# <a name="esentrequiredlogfilesmissingexception-class"></a>EsentRequiredLogFilesMissingException-Klasse

Basisklasse für JET_err. RequiredLogFilesMissing-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRequiredLogFilesMissingException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentRequiredLogFilesMissingException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRequiredLogFilesMissingException : EsentInconsistentException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentRequiredLogFilesMissingException-Member](./esentrequiredlogfilesmissingexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
