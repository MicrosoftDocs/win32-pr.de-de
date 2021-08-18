---
description: Weitere Informationen finden Sie unter Api.JetRollback-Methode.
title: Api.JetRollback-Methode
TOCTitle: 'JetRollback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRollback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrollback(v=EXCHG.10)
ms:contentKeyID: 55100794
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRollback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 099afa55f6b47d014bccf3ab354ed3c3e5e05d0229aa034a13f467062fa808aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983210"
---
# <a name="apijetrollback-method"></a>Api.JetRollback-Methode

Macht die am Zustand der Datenbank vorgenommenen Änderungen rückgängig und kehrt zum letzten Sicherungspunkt zurück. JetRollback schließt auch alle Cursor, die während des Sicherungspunkts geöffnet wurden. Wenn der äußerste Sicherungspunkt rückgängig ist, beendet die Sitzung die Transaktion.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetRollback ( _
    sesid As JET_SESID, _
    grbit As RollbackTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As RollbackTransactionGrbitApi.JetRollback(sesid, grbit)
```

``` csharp
public static void JetRollback(
    JET_SESID sesid,
    RollbackTransactionGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die Sitzung, für die ein Rollback für die Transaktion ausgeführt werden soll.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit](./rollbacktransactiongrbit-enumeration.md)  
    
    Rollbackoptionen.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
