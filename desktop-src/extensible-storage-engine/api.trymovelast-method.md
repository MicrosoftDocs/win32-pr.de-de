---
description: 'Weitere Informationen finden Sie unter: Api.TryMoveLast-Methode'
title: Api.TryMoveLast-Methode
TOCTitle: 'TryMoveLast method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMoveLast(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymovelast(v=EXCHG.10)
ms:contentKeyID: 55100933
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMoveLast
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMoveLast
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 961a0cb7843f2545c81ea21048a9b68d0507153735708e5baaeca3f68cba5527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947700"
---
# <a name="apitrymovelast-method"></a>Api.TryMoveLast-Methode

Versuchen Sie, zum letzten Datensatz in der Tabelle zu wechseln. Wenn die Tabelle leer ist, wird false zurückgegeben, wenn ein anderer Fehler auftritt, wird eine Ausnahme ausgelöst.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function TryMoveLast ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMoveLast(sesid, _
    tableid)
```

``` csharp
public static bool TryMoveLast(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der zu positionierende Cursor.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Boolean](/dotnet/api/system.boolean)  
True, wenn die Bewegung erfolgreich war.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
