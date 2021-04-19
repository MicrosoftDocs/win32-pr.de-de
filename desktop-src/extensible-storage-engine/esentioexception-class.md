---
description: 'Weitere Informationen finden Sie unter: esentioexception-Klasse'
title: EsentIOException-Klasse
TOCTitle: EsentIOException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIOException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102033
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIOException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5fbcbf38ae60ae17f74e650c403611a88d89662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366260"
---
# <a name="esentioexception-class"></a>EsentIOException-Klasse

Basisklasse für e/a-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentoperationexception](./esentoperationexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentioexception  
            [Microsoft. ISAM. ESENT. Interop. esentdeletebackupfilefailexception](./esentdeletebackupfilefailexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentdiskioexception](./esentdiskioexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentfileaccessdeniedexception](./esentfileaccessdeniedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogschreitefailexception](./esentlogwritefailexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmakebackupdirectoriyfailexception](./esentmakebackupdirectoryfailexception-class.md)  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentIOException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentIOException
```

``` csharp
[SerializableAttribute]
public abstract class EsentIOException : EsentOperationException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentioexception-Member](./esentioexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
