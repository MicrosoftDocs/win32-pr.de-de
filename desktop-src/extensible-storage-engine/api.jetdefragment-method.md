---
description: Weitere Informationen finden Sie in der API. jetdefragment-Methode.
title: API. jetdefragment-Methode
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69428d785bf9d607199cb62bfe02d2e373e7dbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344419"
---
# <a name="apijetdefragment-method"></a>API. jetdefragment-Methode

Startet und beendet datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die für den-Befehl zu verwendende Sitzung.

<!-- end list -->

  - dbid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Die Datenbank, die deaktiviert werden soll.

<!-- end list -->

  - tableName  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Nicht verwendeter Parameter. Die Defragmentierung wird für die gesamte Datenbank ausgeführt, die durch die angegebene Datenbank-ID beschrieben wird.

<!-- end list -->

  - ausweisen  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Wenn eine Online Defragmentierung gestartet wird, wird mit diesem Parameter die maximale Anzahl von defragmentierungsläufen festgelegt. Wenn Sie eine Online Defragmentierung beenden, wird dieser Parameter auf die Anzahl der durchgeführten Durchläufen festgelegt.

<!-- end list -->

  - Sekunden  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Wenn eine Online Defragmentierung gestartet wird, legt dieser Parameter die maximale Zeit für die Defragmentierung fest. Wenn Sie eine Online Defragmentierung beenden, wird dieser Ausgabepuffer auf die für die Defragmentierung verwendete Zeitspanne festgelegt.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. defraggrbit](./defraggrbit-enumeration.md)  
    
    Defragmentierungsoptionen.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein Warnungs Code.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
