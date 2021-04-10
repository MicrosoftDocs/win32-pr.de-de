---
description: Weitere Informationen finden Sie in der API. jetenreeratecolumschlag-Methode.
title: API. jetenreeratecolumschlag-Methode
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
ms.openlocfilehash: c9a9848d4470d54cc2a146098343b664c9bd3419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041662"
---
# <a name="apijetenumeratecolumns-method"></a>API. jetenreeratecolumschlag-Methode

Ruft effizient eine Gruppe von Spalten und deren Werten aus dem aktuellen Datensatz eines Cursors oder dem Kopier Puffer dieses Cursors ab. Die abgerufenen Spalten und Werte können durch eine Liste von Spalten-IDs, itagsequence-Nummern und anderen Merkmalen eingeschränkt werden. Diese Spalten Abruf-API ist eindeutig, da Sie Informationen in dynamisch zugewiesener Speicher zurückgibt, die mit einem vom Benutzer bereitgestellten rezuordnungskompatiblen Rückruf abgerufen werden. Diese neue Flexibilität ermöglicht das effiziente Abrufen von Spaltendaten mit bestimmten Merkmalen (z. b. Größe und Multiplizität), die dem Aufrufer unbekannt sind. Dadurch ist es nicht mehr erforderlich, die Ermittlungs Modi jetretrievecolumgen zu verwenden, um die Eigenschaften zu bestimmen, um einen letzten Rückruf für jetretrievecolumschlag einzurichten, mit dem die gewünschten Daten erfolgreich abgerufen werden.

Diese API ist nicht CLS-kompatibel. 

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, von dem Daten abgerufen werden sollen.

<!-- end list -->

  - numcolumnids  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Anzahl der JET_ENUMCOLUMNIDS.

<!-- end list -->

  - columnIds  
    Sorte \[\]  
    
    Ein optionales Array von Spalten-IDs, von denen jedes ein optionales Array von itagsequence-Zahlen auflistet.

<!-- end list -->

  - numcolumnvalues  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Gibt die Anzahl der abgerufenen Spaltenwerte zurück.

<!-- end list -->

  - columnvalues  
    Sorte \[\]  
    
    Gibt die aufgelisteten Spaltenwerte zurück.

<!-- end list -->

  - allocator  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)  
    
    Rückruf, der zum Zuordnen von Speicher verwendet wird.

<!-- end list -->

  - ' Zuweisung '  
    Typ: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Der Kontext für den Zuordnungs Rückruf.

<!-- end list -->

  - maxdatasize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Legt eine Obergrenze für die Menge der Daten fest, die von einer Long-Text-oder Long Binary-Spalte zurückgegeben wird. Dieser Parameter kann verwendet werden, um die Enumeration eines extrem großen Spaltenwerts zu verhindern.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. enumeratecolumnsgrbit](./enumeratecolumnsgrbit-enumeration.md)  
    
    Abrufen von Optionen.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Eine Warnung oder ein Erfolg.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
