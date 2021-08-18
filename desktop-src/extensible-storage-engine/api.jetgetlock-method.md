---
description: Weitere Informationen finden Sie unter Api.JetGetLock-Methode.
title: Api.JetGetLock-Methode
TOCTitle: 'JetGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetlock(v=EXCHG.10)
ms:contentKeyID: 55100732
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 692d78c274d497c64deff20fc61f2cc6a32e868b6f591e4dd6a32437d007b1b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623560"
---
# <a name="apijetgetlock-method"></a>Api.JetGetLock-Methode

Reservieren Sie explizit die Möglichkeit, eine Zeile zu aktualisieren, eine Schreibsperre zu schreiben oder explizit zu verhindern, dass eine Zeile von einer anderen Sitzung aktualisiert wird. Lesen Sie die Sperre. Normalerweise werden Zeilenschreibsperren implizit als Ergebnis der Aktualisierung von Zeilen eingerichtet. Lesesperren sind aufgrund der Datensatzversionsierung in der Regel nicht erforderlich. In einigen Fällen möchte eine Transaktion jedoch möglicherweise explizit eine Zeile sperren, um die Serialisierung zu erzwingen oder sicherzustellen, dass ein nachfolgender Vorgang erfolgreich ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbitApi.JetGetLock(sesid, tableid, grbit)
```

``` csharp
public static void JetGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der zu verwendende Cursor. Für den aktuellen Datensatz wird eine Sperre eingerichtet.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.GetLockGrbit](./getlockgrbit-enumeration.md)  
    
    Sperrenoptionen: Verwenden Sie diese Option, um anzugeben, welche Art von Sperre sie erhalten soll.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
