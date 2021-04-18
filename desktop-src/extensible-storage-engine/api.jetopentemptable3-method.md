---
description: Weitere Informationen finden Sie in der API. JetOpenTempTable3-Methode.
title: Api.JetOpenTempTable3-Methode
TOCTitle: 'JetOpenTempTable3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable3(v=EXCHG.10)
ms:contentKeyID: 55100774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e88b5413492c0ae00ed41e569afb49ca6c18e51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352736"
---
# <a name="apijetopentemptable3-method"></a>Api.JetOpenTempTable3-Methode

Erstellt eine temporäre Tabelle mit einem einzelnen Index. Eine temporäre Tabelle speichert und ruft Datensätze wie eine gewöhnliche Tabelle ab, die mithilfe von jetkreatetablecolumnindex erstellt wurde. Temporäre Tabellen sind aufgrund ihrer flüchtigen Natur jedoch viel schneller als normale Tabellen. Sie können auch verwendet werden, um das Entfernen von Duplikaten für Daten Satz Gruppen sehr schnell zu sortieren und auszuführen, wenn auf eine rein sequenzielle Weise zugegriffen wird. Siehe auch [jetopentemptable (JET_SESID, \[ \] , Int32, temptablegrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [jetopentemporarytable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetOpenTempTable3 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    unicodeindex As JET_UNICODEINDEX, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim unicodeindex As JET_UNICODEINDEX
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable3(sesid, columns, _
    numColumns, unicodeindex, grbit, _
    tableid, columnids)
```

``` csharp
public static void JetOpenTempTable3(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    JET_UNICODEINDEX unicodeindex,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - Spalten  
    Sorte \[\]  
    
    Spaltendefinitionen für die Spalten, die in der temporären Tabelle erstellt werden.

<!-- end list -->

  - NumColumns  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Anzahl der Spaltendefinitionen.

<!-- end list -->

  - unicodeindex  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)  
    
    Die Gebiets Schema-ID und die normalisierungs Flags, die verwendet werden, um alle Unicode-Schlüssel Spaltendaten in der temporären Tabelle zu vergleichen. Wenn dies nicht der Fall ist, werden die Standardoptionen verwendet.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. temptablegrbit](./temptablegrbit-enumeration.md)  
    
    Tabellen Erstellungs Optionen.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Gibt die TableID der temporären Tabelle zurück. Wenn Sie diese TableID mit [jetclosetable (JET_SESID JET_TABLEID) schließen, werden](./api.jetclosetable-method.md) die der temporären Tabelle zugeordneten Ressourcen freigegeben.

<!-- end list -->

  - columnIds  
    Sorte \[\]  
    
    Der Ausgabepuffer, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden. Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen. Folglich muss die Größe dieses Puffers der Größe des Eingabe Arrays entsprechen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
