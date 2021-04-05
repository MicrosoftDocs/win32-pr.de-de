---
description: Weitere Informationen finden Sie in der JET_SETCOLUMN. pvData-Eigenschaft.
title: JET_SETCOLUMN. pvData (Eigenschaft)
TOCTitle: 'pvData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.pvData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.pvdata(v=EXCHG.10)
ms:contentKeyID: 55103932
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.pvData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_pvData
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_pvData
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.pvData
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c47170dd68749b13f0c6a3bc818f0a2fb775e77b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750496"
---
# <a name="jet_setcolumnpvdata-property"></a>JET_SETCOLUMN. pvData (Eigenschaft)

Ruft einen Zeiger auf die festzulegenden Daten ab oder legt diesen fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pvData As Byte()
    Get
    Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As Byte()

value = instance.pvData

instance.pvData = value
```

``` csharp
public byte[] pvData { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Sorte \[\]  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_SETCOLUMN-Klasse](./jet-setcolumn-class.md)

[Mitglieder JET_SETCOLUMN](./jet-setcolumn-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
