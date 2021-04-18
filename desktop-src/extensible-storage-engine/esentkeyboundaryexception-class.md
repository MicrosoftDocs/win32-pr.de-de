---
description: 'Weitere Informationen finden Sie unter: esentkeyboundaryexception-Klasse'
title: Esentkeyboundaryexception-Klasse
TOCTitle: EsentKeyBoundaryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentkeyboundaryexception(v=EXCHG.10)
ms:contentKeyID: 55107283
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentKeyBoundaryException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 959c410f9f2f38b722b7517c5324f8d4f98affa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354861"
---
# <a name="esentkeyboundaryexception-class"></a>Esentkeyboundaryexception-Klasse

Basisklasse für JET_err. Keyboundary-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentapiexception](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentobsoleteexception](./esentobsoleteexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. esentkeyboundaryexception  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentKeyBoundaryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentKeyBoundaryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentKeyBoundaryException : EsentObsoleteException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentkeyboundaryexception-Member](./esentkeyboundaryexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
