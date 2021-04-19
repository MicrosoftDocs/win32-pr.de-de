---
description: 'Weitere Informationen finden Sie unter: implizite Sitzungs Konvertierung (Session to JET_SESID)'
title: Implizite Sitzungs Konvertierung (Sitzung zu JET_SESID)
TOCTitle: Implicit conversion (Session to JET_SESID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.op_Implicit(Microsoft.Isam.Esent.Interop.Session)~Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104121
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session.op_Implicit
- Microsoft.Isam.Esent.Interop.Session.Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 512bc457a84ad1d1b170ac9d31cb04e36d8a05d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356547"
---
# <a name="session-implicit-conversion-session-to-jet_sesid"></a>Implizite Sitzungs Konvertierung (Sitzung zu JET_SESID)

Impliziter Konvertierungs Operator von einer Sitzung zu einer JET_SESID. Dadurch kann eine Sitzung mit APIs verwendet werden, die eine JET_SESID erwarten.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    session As Session _
) As JET_SESID
'Usage
Dim input As Session
Dim output As JET_SESID

output = CType(input, JET_SESID)
```

``` csharp
public static implicit operator JET_SESID (
    Session session
)
```

#### <a name="parameters"></a>Parameter

  - session  
    Typ: [Microsoft. ISAM. ESENT. Interop. Session](./session-class.md)  
    
    Die zu konvertierende Sitzung.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
Der JET_SESID der Sitzung.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Sitzungsklasse](./session-class.md)

[Sitzungs Mitglieder](./session-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
