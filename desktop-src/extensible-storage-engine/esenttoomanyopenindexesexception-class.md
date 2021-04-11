---
description: 'Weitere Informationen finden Sie unter: esentesomanyopenindexesexception-Klasse'
title: Esentesomanyopenindexesexception-Klasse
TOCTitle: EsentTooManyOpenIndexesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopenindexesexception(v=EXCHG.10)
ms:contentKeyID: 55103106
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 681f9a8ec67b9b9c82babcc3814833a1a3dbb0d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217879"
---
# <a name="esenttoomanyopenindexesexception-class"></a>Esentesomanyopenindexesexception-Klasse

Basisklasse für JET_err. Ausnahmen für "-openindexes".

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentoperationexception](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentresourceexception](./esentresourceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentmemoryexception](./esentmemoryexception-class.md)  
              Microsoft. ISAM. ESENT. Interop. esentesomanyopenindexesexception  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenIndexesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManyOpenIndexesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenIndexesException : EsentMemoryException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentesomanyopenindexesexception-Member](./esenttoomanyopenindexesexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
