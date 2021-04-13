---
description: Weitere Informationen finden Sie in der JET_ENUMCOLUMN. pvData-Eigenschaft.
title: JET_ENUMCOLUMN. pvData (Eigenschaft)
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103500
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_pvData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7d4c72a45d90fd8004af2011f9f6081a59cfabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484891"
---
# <a name="jet_enumcolumnpvdata-property"></a>JET_ENUMCOLUMN. pvData (Eigenschaft)

Ruft den Wert ab, der für die Spalte aufgelistet wurde. Dieser Member wird nur verwendet, wenn [Err](./jet-enumcolumn.err-property.md) gleich [columnsinglevalue](./jet-wrn-enumeration.md)ist. Dies verweist auf den Arbeitsspeicher, der mit dem an [jetenumeratecolumns (JET_SESID, JET_TABLEID, Int32, \[ \] , Int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, enumeratecolumnsgrbit)](./api.jetenumeratecolumns-method.md)weiter gegebenen [JET_PFNREALLOC](./jet-pfnrealloc-delegate.md) Zuordnungs Rückruf zugeordnet wird. Vergessen Sie nicht, den Arbeitsspeicher zu veröffentlichen

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pvData As IntPtr
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As IntPtr

value = instance.pvData
```

``` csharp
public IntPtr pvData { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. IntPtr](/dotnet/api/system.intptr)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_ENUMCOLUMN-Klasse](./jet-enumcolumn-class.md)

[Mitglieder JET_ENUMCOLUMN](./jet-enumcolumn-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
