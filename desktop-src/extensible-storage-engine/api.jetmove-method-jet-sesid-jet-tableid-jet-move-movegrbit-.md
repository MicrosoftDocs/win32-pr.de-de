---
description: 'Weitere Informationen finden Sie unter: API. jetmove-Methode (JET_SESID, JET_TABLEID, JET_Move, movegrbit)'
title: API. jetmove-Methode (JET_SESID, JET_TABLEID, JET_Move, movegrbit)
TOCTitle: JetMove method (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmove(v=EXCHG.10)
ms:contentKeyID: 55100766
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5b6eeaf8d728cf63304141614caaf9598bcc6c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759756"
---
# <a name="apijetmove-method-jet_sesid-jet_tableid-jet_move-movegrbit"></a>API. jetmove-Methode (JET_SESID, JET_TABLEID, JET_Move, movegrbit)

Navigieren Sie durch einen Index. Der Cursor kann am Anfang oder Ende des Indexes positioniert und um eine angegebene Anzahl von Indexeinträgen rückwärts und vorwärts verschoben werden. Siehe auch [trymuvefirst (JET_SESID, JET_TABLEID)](./api.trymovefirst-method.md), [trymuvelast (JET_SESID, JET_TABLEID)](./api.trymovelast-method.md), [trymuvenext (JET_SESID, JET_TABLEID)](./api.trymovenext-method.md), [trymuveprevious (JET_SESID, JET_TABLEID)](./api.trymoveprevious-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numRows As JET_Move, _
    grbit As MoveGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRows As JET_Move
Dim grbit As MoveGrbitApi.JetMove(sesid, tableid, numRows, _
    grbit)
```

``` csharp
public static void JetMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move numRows,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die für den-Befehl zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, der positioniert werden soll.

<!-- end list -->

  - numRows  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_Move](./jet-move-enumeration.md)  
    
    Ein Offset, der angibt, wie weit der Cursor verschoben werden soll.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. muvegrbit](./movegrbit-enumeration.md)  
    
    Verschieben von Optionen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Jetmove-Überladung](./api.jetmove-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
