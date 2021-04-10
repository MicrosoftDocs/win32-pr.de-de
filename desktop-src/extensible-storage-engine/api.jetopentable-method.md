---
description: Weitere Informationen finden Sie in der API. jetopentable-Methode.
title: API. jetopentable-Methode
TOCTitle: 'JetOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentable(v=EXCHG.10)
ms:contentKeyID: 55100776
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5764138d4ea387b68c94805c6966f7ce0e817c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960727"
---
# <a name="apijetopentable-method"></a>API. jetopentable-Methode

Öffnet einen Cursor für eine zuvor erstellte Tabelle.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    parameters As Byte(), _
    parametersSize As Integer, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim parameters As Byte()
Dim parametersSize As Integer
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As JET_wrn

returnValue = Api.JetOpenTable(sesid, _
    dbid, tablename, parameters, parametersSize, _
    grbit, tableid)
```

``` csharp
public static JET_wrn JetOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    byte[] parameters,
    int parametersSize,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Daten banksitzung.

<!-- end list -->

  - dbid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Die Datenbank, in der die Tabelle geöffnet werden soll.

<!-- end list -->

  - Tabellenname  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Der Name der zu öffnenden Tabelle.

<!-- end list -->

  - parameters  
    Sorte \[\]  
    
    Der-Parameter wird nicht verwendet.

<!-- end list -->

  - parameterssize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Der-Parameter wird nicht verwendet.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. opentablegrbit](./opentablegrbit-enumeration.md)  
    
    Tabellen Öffnungs Optionen.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Gibt die geöffnete Tabelle zurück.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Eine ESENT-Warnung.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
