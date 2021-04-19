---
description: 'Weitere Informationen finden Sie hier: API. jetescrowupdate-Methode'
title: API. jetescrowupdate-Methode
TOCTitle: 'JetEscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetescrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100740
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 09e74f964fd6018248a3cfc594621bed96f92e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339767"
---
# <a name="apijetescrowupdate-method"></a>API. jetescrowupdate-Methode

Führt eine atomarische Additions Operation für eine Spalte aus. Diese Funktion ermöglicht es mehreren Sitzungen, denselben Datensatz gleichzeitig zu aktualisieren, ohne dass Konflikte auftreten. Siehe auch [escrowupdate (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetEscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Byte(), _
    deltaSize As Integer, _
    previousValue As Byte(), _
    previousValueLength As Integer, _
    <OutAttribute> ByRef actualPreviousValueLength As Integer, _
    grbit As EscrowUpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Byte()
Dim deltaSize As Integer
Dim previousValue As Byte()
Dim previousValueLength As Integer
Dim actualPreviousValueLength As Integer
Dim grbit As EscrowUpdateGrbitApi.JetEscrowUpdate(sesid, tableid, _
    columnid, delta, deltaSize, previousValue, _
    previousValueLength, actualPreviousValueLength, _
    grbit)
```

``` csharp
public static void JetEscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] delta,
    int deltaSize,
    byte[] previousValue,
    int previousValueLength,
    out int actualPreviousValueLength,
    EscrowUpdateGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung. Die Sitzung muss sich in einer Transaktion befinden.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, der aktualisiert werden soll.

<!-- end list -->

  - columnid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Die zu Aktualisier gende Spalte. Dabei muss es sich um eine aktualisierbare Spalte für die Hinterlegung

<!-- end list -->

  - delta  
    Sorte \[\]  
    
    Der Puffer, der den Addend enthält.

<!-- end list -->

  - Delta size  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Größe des Addend.

<!-- end list -->

  - previousValue  
    Sorte \[\]  
    
    Ein Ausgabepuffer, der den aktuellen Wert der Spalte empfängt. Dieser Puffer kann NULL sein.

<!-- end list -->

  - previousvaluelength  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Größe des previousValue-Puffers.

<!-- end list -->

  - actualpreviousvaluelength  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Gibt die tatsächliche Größe von previousValue zurück.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. escrowupdategrbit](./escrowupdategrbit-enumeration.md)  
    
    Optionen zum Aktualisieren von Optionen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
