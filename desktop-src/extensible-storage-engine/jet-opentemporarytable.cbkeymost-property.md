---
description: 'Weitere Informationen finden Sie hier: JET_OPENTEMPORARYTABLE. cbkeymost-Eigenschaft'
title: JET_OPENTEMPORARYTABLE. cbkeymost-Eigenschaft (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e608d1419cd381c507874bf1f1c334d192ae2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363380"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a>JET_OPENTEMPORARYTABLE. cbkeymost-Eigenschaft

Ruft die maximale Größe für einen Schlüssel ab, der eine angegebene Zeile darstellt, oder legt diese fest. Die maximale Schlüsselgröße kann festgelegt werden, um zu steuern, wie Schlüssel abgeschnitten werden. Das Abschneiden von Schlüsseln ist wichtig, da sich dies auf den Fall auswirkt, dass Zeilen als verschieden betrachtet werden. Wenn dieser Parameter auf 0 oder 255 festgelegt ist, bleiben die maximale Schlüsselgröße und ihre Semantik identisch mit der maximalen Schlüsselgröße, die von Windows Server 2003 unterstützt wird. Dieser Parameter kann auch auf einen größeren Wert als Funktion der Datenbankseiten Größe für die Instanz [databasepagesize](./jet-param-enumeration.md)festgelegt werden. Weitere Informationen finden Sie unter [keymost](./vistaparam.keymost-field.md) .

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_OPENTEMPORARYTABLE-Klasse](./jet-opentemporarytable-class.md)

[Mitglieder JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
