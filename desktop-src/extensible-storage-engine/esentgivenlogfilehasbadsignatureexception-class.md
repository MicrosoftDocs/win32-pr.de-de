---
description: 'Weitere Informationen finden Sie unter: EsentGivenLogFileHasBadSignatureException-Klasse'
title: EsentGivenLogFileHasBadSignatureException-Klasse
TOCTitle: EsentGivenLogFileHasBadSignatureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentgivenlogfilehasbadsignatureexception(v=EXCHG.10)
ms:contentKeyID: 55101732
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b164e2d8502c1d260152c6cae052f3fb2cf15524130dcf11d2d2a848f2f35edb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065270"
---
# <a name="esentgivenlogfilehasbadsignatureexception-class"></a>EsentGivenLogFileHasBadSignatureException-Klasse

Basisklasse für JET_err. GivenLogFileHasBadSignature-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentGivenLogFileHasBadSignatureException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentGivenLogFileHasBadSignatureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentGivenLogFileHasBadSignatureException : EsentInconsistentException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentGivenLogFileHasBadSignatureException-Member](./esentgivenlogfilehasbadsignatureexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
