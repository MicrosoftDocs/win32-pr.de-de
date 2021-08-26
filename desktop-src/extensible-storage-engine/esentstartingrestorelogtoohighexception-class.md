---
description: 'Weitere Informationen finden Sie unter: EsentStartingRestoreLogTooHighException-Klasse'
title: EsentStartingRestoreLogTooHighException-Klasse
TOCTitle: EsentStartingRestoreLogTooHighException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstartingrestorelogtoohighexception(v=EXCHG.10)
ms:contentKeyID: 55102926
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a886142e5b99546ba01ce941c9a24a116e43adf8011ba938098c4baeca6fac15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018010"
---
# <a name="esentstartingrestorelogtoohighexception-class"></a>EsentStartingRestoreLogTooHighException-Klasse

Basisklasse für JET_err. StartingRestoreLogTooHigh-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentStartingRestoreLogTooHighException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentStartingRestoreLogTooHighException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentStartingRestoreLogTooHighException
```

``` csharp
[SerializableAttribute]
public sealed class EsentStartingRestoreLogTooHighException : EsentInconsistentException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentStartingRestoreLogTooHighException-Member](./esentstartingrestorelogtoohighexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
