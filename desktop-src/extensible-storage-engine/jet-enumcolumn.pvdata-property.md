---
description: 'Weitere Informationen finden Sie unter: JET_ENUMCOLUMN.pvData-Eigenschaft'
title: JET_ENUMCOLUMN.pvData-Eigenschaft
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
ms.openlocfilehash: df79d838277a849c99ea49af2a8ca12e77cb3667d4750b141f0b9247b46b9232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254693"
---
# <a name="jet_enumcolumnpvdata-property"></a>JET_ENUMCOLUMN.pvData-Eigenschaft

Ruft den Wert ab, der für die Spalte aufzählt wurde. Dieser Member wird nur verwendet, [wenn err](./jet-enumcolumn.err-property.md) gleich [ColumnSingleValue ist.](./jet-wrn-enumeration.md) Dies verweist auf den [Arbeitsspeicher,](./jet-pfnrealloc-delegate.md) der mit dem JET_PFNREALLOC-Zuweisungsrückruf an [JetEnumerateColumns(JET_SESID, JET_TABLEID, \[ \] Int32, , Int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit) zugewiesen](./api.jetenumeratecolumns-method.md)wird. Denken Sie daran, den Arbeitsspeicher frei zu geben, wenn Sie fertig sind.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [System.IntPtr](/dotnet/api/system.intptr)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_ENUMCOLUMN-Klasse](./jet-enumcolumn-class.md)

[JET_ENUMCOLUMN Mitglieder](./jet-enumcolumn-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
