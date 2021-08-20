---
description: Weitere Informationen finden Sie unter Api.TryOpenTable-Methode.
title: Api.TryOpenTable-Methode
TOCTitle: 'TryOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryopentable(v=EXCHG.10)
ms:contentKeyID: 55100889
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3624e32543d671f9c31334608a91b4528b4966ee70de2a0014dc3e96fd6c57b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117717206"
---
# <a name="apitryopentable-method"></a>Api.TryOpenTable-Methode

Versuchen Sie, eine Tabelle zu öffnen.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function TryOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryOpenTable(sesid, _
    dbid, tablename, grbit, tableid)
```

``` csharp
public static bool TryOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - dbid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Die Datenbank, in der nach der Tabelle gesucht werden soll.

<!-- end list -->

  - Tabellenname  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Der Name der Tabelle.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)  
    
    Optionen zum Öffnen von Tabellen.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Gibt die geöffnete tableid zurück.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
True, wenn die Tabelle geöffnet wurde, FALSE, wenn die Tabelle nicht vorhanden ist.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
