---
description: 'Weitere Informationen finden Sie hier: JET_CALLBACK-Delegaten'
title: JET_CALLBACK Delegat
TOCTitle: JET_CALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_callback(v=EXCHG.10)
ms:contentKeyID: 39515752
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_CALLBACK..ctor
- Microsoft.Isam.Esent.Interop.JET_CALLBACK.Invoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 617cbefba047f822b338627a782be7e016c2a16f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373287"
---
# <a name="jet_callback-delegate"></a>JET_CALLBACK Delegat

Eine multizweck-Rückruffunktion, die von der Datenbank-Engine verwendet wird, um die Anwendung über ein Ereignis mit Online Defragmentierung und Cursor Zustands Benachrichtigungen zu informieren.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Delegate Function JET_CALLBACK ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    arg1 As Object, _
    arg2 As Object, _
    context As IntPtr, _
    unused As IntPtr _
) As JET_err
'Usage
Dim instance As New JET_CALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_CALLBACK(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    Object arg1,
    Object arg2,
    IntPtr context,
    IntPtr unused
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die Sitzung, für die der Rückruf erstellt wird.

<!-- end list -->

  - dbid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Die Datenbank, für die der Rückruf erstellt wird.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, für den der Rückruf erstellt wird.

<!-- end list -->

  - cbyp  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)  
    
    Der Vorgang, für den der Rückruf durchgeführt wird.

<!-- end list -->

  - arg1  
    Type: [System. Object](/dotnet/api/system.object)  
    
    Das erste Rückruf spezifische Argument.

<!-- end list -->

  - arg2  
    Type: [System. Object](/dotnet/api/system.object)  
    
    Zweites Rückruf spezifisches Argument.

<!-- end list -->

  - context  
    Typ: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Rückruf Kontext.

<!-- end list -->

  - unused  
    Typ: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Dieser Parameter wird nicht verwendet.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
