---
description: 'Weitere Informationen zu: EsentInvalidCountryException-Klasse'
title: EsentInvalidCountryException-Klasse
TOCTitle: EsentInvalidCountryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidCountryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidcountryexception(v=EXCHG.10)
ms:contentKeyID: 55101935
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidCountryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidCountryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 12ce899d8eedd1b6c0e11aa6a64acca5ee051f5f6d9524317baa0ca5ab04cd49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982430"
---
# <a name="esentinvalidcountryexception-class"></a>EsentInvalidCountryException-Klasse

Basisklasse für JET_err. InvalidCountry-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentInvalidCountryException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidCountryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentInvalidCountryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidCountryException : EsentObsoleteException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentInvalidCountryException-Member](./esentinvalidcountryexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
