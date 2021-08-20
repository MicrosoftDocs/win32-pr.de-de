---
description: 'Weitere Informationen finden Sie unter: EsentSQLLinkNotSupportedException-Klasse'
title: EsentSQLLinkNotSupportedException-Klasse
TOCTitle: EsentSQLLinkNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSQLLinkNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsqllinknotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55102922
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSQLLinkNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSQLLinkNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c9e314b32b9d56c8bba73eedad69c386cba4a6983be3cb0cf5f72c30022cdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118078324"
---
# <a name="esentsqllinknotsupportedexception-class"></a>EsentSQLLinkNotSupportedException-Klasse

Basisklasse für JET_err. SQLLinkNotSupported-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentSQLLinkNotSupportedException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSQLLinkNotSupportedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentSQLLinkNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSQLLinkNotSupportedException : EsentObsoleteException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentSQLLinkNotSupportedException-Member](./esentsqllinknotsupportedexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
