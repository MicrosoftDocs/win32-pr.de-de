---
description: 'Weitere Informationen finden Sie unter: esentfileaccessdeniedexception-Klasse'
title: Esentfileaccessdeniedexception-Klasse
TOCTitle: EsentFileAccessDeniedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileaccessdeniedexception(v=EXCHG.10)
ms:contentKeyID: 55101658
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afb92cc5fad314763ef2d679035b727f38b8305a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347642"
---
# <a name="esentfileaccessdeniedexception-class"></a>Esentfileaccessdeniedexception-Klasse

Basisklasse für JET_err. Fileaccessdenied-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentoperationexception](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentioexception](./esentioexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. esentfileaccessdeniedexception  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileAccessDeniedException _
    Inherits EsentIOException
'Usage
Dim instance As EsentFileAccessDeniedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileAccessDeniedException : EsentIOException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentfileaccessdeniedexception-Elemente](./esentfileaccessdeniedexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
