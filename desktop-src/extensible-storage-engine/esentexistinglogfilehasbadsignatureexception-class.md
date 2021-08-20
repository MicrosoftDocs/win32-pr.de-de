---
description: 'Weitere Informationen finden Sie unter: EsentExistingLogFileHasBadSignatureException-Klasse'
title: EsentExistingLogFileHasBadSignatureException-Klasse
TOCTitle: EsentExistingLogFileHasBadSignatureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentExistingLogFileHasBadSignatureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentexistinglogfilehasbadsignatureexception(v=EXCHG.10)
ms:contentKeyID: 55101651
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentExistingLogFileHasBadSignatureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentExistingLogFileHasBadSignatureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ac84eaef60c5cc30e7bdf4422c0c3b081f56e9bd0eeeb8a43b30aa34bfd3c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118082074"
---
# <a name="esentexistinglogfilehasbadsignatureexception-class"></a>EsentExistingLogFileHasBadSignatureException-Klasse

Basisklasse für JET_err. ExistingLogFileHasBadSignature-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentExistingLogFileHasBadSignatureException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentExistingLogFileHasBadSignatureException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentExistingLogFileHasBadSignatureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentExistingLogFileHasBadSignatureException : EsentInconsistentException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentExistingLogFileHasBadSignatureException-Member](./esentexistinglogfilehasbadsignatureexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
