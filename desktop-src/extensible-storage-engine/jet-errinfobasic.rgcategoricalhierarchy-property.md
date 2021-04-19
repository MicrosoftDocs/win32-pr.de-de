---
description: 'Weitere Informationen finden Sie hier: JET_ERRINFOBASIC. rgcategoricalhierarchy-Eigenschaft'
title: JET_ERRINFOBASIC. rgcategoricalhierarchy-Eigenschaft (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'rgCategoricalHierarchy property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_errinfobasic.rgcategoricalhierarchy(v=EXCHG.10)
ms:contentKeyID: 55104314
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.set_rgCategoricalHierarchy
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.get_rgCategoricalHierarchy
- Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC.rgCategoricalHierarchy
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37034ca35427c9470d69f5e90dd43a4640601574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362273"
---
# <a name="jet_errinfobasicrgcategoricalhierarchy-property"></a>JET_ERRINFOBASIC. rgkategoricalhierarchy (Eigenschaft)

Ruft die Hierarchie von Fehlern ab oder legt Sie fest. Position 0 ist die höchste Ebene in der Hierarchie, und der Rest wird JET_errcatUnknown.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property rgCategoricalHierarchy As JET_ERRCAT()
    Get
    Set
'Usage
Dim instance As JET_ERRINFOBASIC
Dim value As JET_ERRCAT()

value = instance.rgCategoricalHierarchy

instance.rgCategoricalHierarchy = value
```

``` csharp
public JET_ERRCAT[] rgCategoricalHierarchy { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Sorte \[\]  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_ERRINFOBASIC-Klasse](./jet-errinfobasic-class.md)

[Mitglieder JET_ERRINFOBASIC](./jet-errinfobasic-members.md)

[Microsoft. ISAM. ESENT. Interop. Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
