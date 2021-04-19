---
description: Weitere Informationen finden Sie in der JET_SETCOLUMN. itagsequence-Eigenschaft.
title: JET_SETCOLUMN. itagsequence (Eigenschaft)
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103935
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_itagSequence
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_itagSequence
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7870f6e29cf8f6810c6aa41049868fbceb370dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345023"
---
# <a name="jet_setcolumnitagsequence-property"></a>JET_SETCOLUMN. itagsequence (Eigenschaft)

Ruft die Sequenznummer des Werts in einer mehrwertigen Spalte ab, die festgelegt werden soll, oder legt Sie fest. Das Array von Werten ist 1-basiert. Der erste Wert ist Sequenz 1, nicht 0 (null). Wenn die Daten Satz Spalte nur über einen Wert verfügt, sollte 1 als itagsequence übergeben werden, wenn dieser Wert ersetzt wird. Der Wert 0 (null) bedeutet, dass am Ende der Sequenz der Spaltenwerte eine neue Spaltenwert Instanz hinzugefügt wird.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_SETCOLUMN-Klasse](./jet-setcolumn-class.md)

[Mitglieder JET_SETCOLUMN](./jet-setcolumn-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
