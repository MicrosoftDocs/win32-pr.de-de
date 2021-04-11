---
description: 'Weitere Informationen finden Sie unter: esentesomanyopentablesexception-Klasse'
title: Esentesomanyopentablesexception-Klasse
TOCTitle: EsentTooManyOpenTablesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopentablesexception(v=EXCHG.10)
ms:contentKeyID: 55107362
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 066191af07aab606731f98a16369b2500d24cda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130569"
---
# <a name="esenttoomanyopentablesexception-class"></a>Esentesomanyopentablesexception-Klasse

Basisklasse für JET_err. "Zu"-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentoperationexception](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentresourceexception](./esentresourceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentquotaexception](./esentquotaexception-class.md)  
              Microsoft. ISAM. ESENT. Interop. esentesomanyopentablesexception  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenTablesException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentTooManyOpenTablesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenTablesException : EsentQuotaException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentesomanyopentablesexception-Elemente](./esenttoomanyopentablesexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
