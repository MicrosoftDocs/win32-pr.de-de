---
description: 'Weitere Informationen finden Sie unter: Api.JetEnumerateColumns-Methode'
title: Api.JetEnumerateColumns-Methode
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 713b02835aa063e888a2385df9bd8abdff9af1300a2e9885c06e995f2b814bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042708"
---
# <a name="apijetenumeratecolumns-method"></a>Api.JetEnumerateColumns-Methode

Ruft effizient einen Satz von Spalten und deren Werte aus dem aktuellen Datensatz eines Cursors oder dem Kopierpuffer dieses Cursors ab. Die abgerufenen Spalten und Werte können durch eine Liste von Spalten-IDs, ItagSequence-Zahlen und anderen Merkmalen eingeschränkt werden. Diese Spaltenabruf-API ist insofern eindeutig, als sie Informationen im dynamisch zugeordneten Speicher zurückgibt, die mithilfe eines vom Benutzer bereitgestellten reloc-kompatiblen Rückrufs abgerufen werden. Diese neue Flexibilität ermöglicht das effiziente Abrufen von Spaltendaten mit bestimmten Merkmalen (z. B. Größe und Multiplizität), die dem Aufrufer unbekannt sind. Dadurch entfällt die Notwendigkeit, die Ermittlungsmodi von JetRetrieveColumn zu verwenden, um diese Merkmale zu bestimmen, um einen endgültigen Aufruf von JetRetrieveColumn einzurichten, der die gewünschten Daten erfolgreich abruft.

Diese API ist nicht CLS-kompatibel. 

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, aus dem Daten abgerufen werden sollen.

<!-- end list -->

  - numColumnids  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Anzahl der JET_ENUMCOLUMNIDS.

<!-- end list -->

  - columnids  
    Typ: \[\]  
    
    Ein optionales Array von Spalten-IDs, jedes mit einem optionalen Array von itagSequence-Zahlen, die aufzählen sollen.

<!-- end list -->

  - numColumnValues  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Gibt die Anzahl der abgerufenen Spaltenwerte zurück.

<!-- end list -->

  - columnValues  
    Typ: \[\]  
    
    Gibt die Aufzählungsspaltenwerte zurück.

<!-- end list -->

  - allocator  
    Typ: [Microsoft.Isam.Esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)  
    
    Rückruf, der zum Zuordnen von Arbeitsspeicher verwendet wird.

<!-- end list -->

  - allocatorContext  
    Typ: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Kontext für den Zuordnungsrückruf.

<!-- end list -->

  - maxDataSize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Legt eine Obergrenze für die Datenmenge fest, die aus einer langen Textspalte oder langen binären Spalte zurückgegeben werden soll. Dieser Parameter kann verwendet werden, um die Enumeration eines extrem großen Spaltenwerts zu verhindern.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)  
    
    Abrufen von Optionen.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Eine Warnung oder ein Erfolg.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
