---
description: 'Weitere Informationen finden Sie unter: API. jetgetcolumninfo-Methode (JET_SESID, JET_DBID, Zeichenfolge, Zeichenfolge, JET_COLUMNLIST)'
title: API. jetgetcolumninfo-Methode (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100703
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f3f0ea95e82217f0d9b44e6a00558d3530a7616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348363"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columnlist"></a>API. jetgetcolumninfo-Methode (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)

Ruft Informationen zu allen Spalten in einer Tabelle ab.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columnlist As JET_COLUMNLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columnlist As JET_COLUMNLISTApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columnlist)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNLIST columnlist
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - dbid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Die Datenbank, die die Tabelle enthält.

<!-- end list -->

  - Tabellenname  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Der Name der Tabelle, die die Spalte enthält.

<!-- end list -->

  - columnName  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Konvertiert die Zeichenfolgendarstellung einer Zahl in einem angegebenen Stil und einem kulturspezifischen Format in die entsprechende 32-Bit-Ganzzahl mit Vorzeichen.

<!-- end list -->

  - ColumnList  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNLIST](./jet-columnlist-class.md)  
    
    Wird mit Informationen über die Spalten in der Tabelle ausgefüllt.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Jetgetcolumninfo-Überladung](./api.jetgetcolumninfo-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
