---
description: 'Weitere Informationen finden Sie hier: JET_OPENTEMPORARYTABLE. prgcolumnid-Eigenschaft'
title: JET_OPENTEMPORARYTABLE. prgcolumnid-Eigenschaft (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'prgcolumnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.prgcolumnid(v=EXCHG.10)
ms:contentKeyID: 55104133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd6516e01d08de32f7962a48d2caca69ddbf0427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960684"
---
# <a name="jet_opentemporarytableprgcolumnid-property"></a>JET_OPENTEMPORARYTABLE. prgcolumnid-Eigenschaft

Ruft den Ausgabepuffer ab, der das Array der Spalten-IDs empfängt, die während der Erstellung der temporären Tabelle generiert wurden, oder legt diesen fest. Die Spalten-IDs in diesem Array entsprechen exakt dem Eingabe Array von Spaltendefinitionen. Folglich muss die Größe dieses Puffers der Größe von [prgcolumndef](./jet-opentemporarytable.prgcolumndef-property.md)entsprechen.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property prgcolumnid As JET_COLUMNID()
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_COLUMNID()

value = instance.prgcolumnid

instance.prgcolumnid = value
```

``` csharp
public JET_COLUMNID[] prgcolumnid { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Sorte \[\]  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_OPENTEMPORARYTABLE-Klasse](./jet-opentemporarytable-class.md)

[Mitglieder JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
