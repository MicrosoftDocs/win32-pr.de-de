---
description: 'Weitere Informationen finden Sie unter: Api.JetIndexRecordCount-Methode'
title: Api.JetIndexRecordCount-Methode
TOCTitle: 'JetIndexRecordCount method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetindexrecordcount(v=EXCHG.10)
ms:contentKeyID: 55100758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3d6d4ba8c06711cefa69ecec651a15bb3d9447efea72be9e0bf46563f1b0972
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978200"
---
# <a name="apijetindexrecordcount-method"></a>Api.JetIndexRecordCount-Methode

Zählt die Anzahl der Einträge im aktuellen Index aus der aktuellen Position vorwärts. Die aktuelle Position ist in der Anzahl enthalten. Die Anzahl kann größer als die Gesamtzahl der Datensätze in der Tabelle sein, wenn sich der aktuelle Index über einer mehrwertigen Spalte befindet und Instanzen der Spalte mehrere Werte aufweisen. Wenn die Tabelle leer ist, wird 0 für die Anzahl zurückgegeben.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetIndexRecordCount ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef numRecords As Integer, _
    maxRecordsToCount As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRecords As Integer
Dim maxRecordsToCount As IntegerApi.JetIndexRecordCount(sesid, _
    tableid, numRecords, maxRecordsToCount)
```

``` csharp
public static void JetIndexRecordCount(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out int numRecords,
    int maxRecordsToCount
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, in dem die Datensätze gezählt werden sollen.

<!-- end list -->

  - numRecords  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Gibt die Anzahl der Datensätze zurück.

<!-- end list -->

  - maxRecordsToCount  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die maximale Anzahl von datensätzen, die gezählt werden sollen. Der Wert 0 gibt an, dass die Anzahl unbegrenzt ist.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
