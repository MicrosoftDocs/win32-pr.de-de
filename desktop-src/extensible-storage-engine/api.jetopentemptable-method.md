---
description: 'Weitere Informationen finden Sie unter: Api.JetOpenTempTable-Methode'
title: Api.JetOpenTempTable-Methode
TOCTitle: 'JetOpenTempTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable(v=EXCHG.10)
ms:contentKeyID: 55100773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: efaf0c6656414ec5e4cf0da96dd7f95dd8a91024d1f0297d8bce8453c08e9865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117718698"
---
# <a name="apijetopentemptable-method"></a>Api.JetOpenTempTable-Methode

Erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert und ruft Datensätze genau wie eine normale Tabelle ab, die mit JetCreateTableColumnIndex erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um sehr schnell zu sortieren und doppelte Entfernungen für Datensatzgruppen durchzuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird. Siehe [auch JetOpenTempTable3(JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md). [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetOpenTempTable ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable(sesid, columns, _
    numColumns, grbit, tableid, columnids)
```

``` csharp
public static void JetOpenTempTable(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - Spalten  
    Typ: \[\]  
    
    Spaltendefinitionen für die in der temporären Tabelle erstellten Spalten.

<!-- end list -->

  - numColumns  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Anzahl der Spaltendefinitionen.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)  
    
    Optionen für die Tabellenerstellung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Gibt die tableid der temporären Tabelle zurück. Wenn Sie diese tableid mit [JetCloseTable(JET_SESID, JET_TABLEID) schließen,](./api.jetclosetable-method.md) werden die der temporären Tabelle zugeordneten Ressourcen frei.

<!-- end list -->

  - columnids  
    Typ: \[\]  
    
    Der Ausgabepuffer, der das Array von Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden. Die Spalten-IDs in diesem Array entsprechen genau dem Eingabearray von Spaltendefinitionen. Daher muss die Größe dieses Puffers der Größe des Eingabearrays entsprechen.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
