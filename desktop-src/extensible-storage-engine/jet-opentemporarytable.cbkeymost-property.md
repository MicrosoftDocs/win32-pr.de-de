---
description: 'Weitere Informationen zu: JET_OPENTEMPORARYTABLE.cbKeyMost-Eigenschaft'
title: JET_OPENTEMPORARYTABLE.cbKeyMost-Eigenschaft (Microsoft.Isam.Esent.Interop.Vista)
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
ms.openlocfilehash: 225c801770bb41337ee9f3ae248092c60441cd2e9a059f64897ad19053bfe30b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107699"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a>JET_OPENTEMPORARYTABLE.cbKeyMost-Eigenschaft

Ruft die maximale Größe für einen Schlüssel ab, der eine angegebene Zeile darstellt, oder legt diese fest. Die maximale Schlüsselgröße kann festgelegt werden, um zu steuern, wie Schlüssel abgeschnitten werden. Das Abschneiden von Schlüsseln ist wichtig, da sie sich darauf auswirken kann, wenn Zeilen als unterschiedlich betrachtet werden. Wenn dieser Parameter auf 0 oder 255 festgelegt ist, bleibt die maximale Schlüsselgröße und ihre Semantik mit der maximalen Schlüsselgröße identisch, die von Windows Server 2003 unterstützt wird. Dieser Parameter kann auch auf einen größeren Wert als Funktion der Datenbankseitengröße für die [DatabasePageSize-Instanz](./jet-param-enumeration.md)festgelegt werden. Weitere Informationen finden Sie unter [KeyMost.](./vistaparam.keymost-field.md)

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_OPENTEMPORARYTABLE-Klasse](./jet-opentemporarytable-class.md)

[JET_OPENTEMPORARYTABLE-Member](./jet-opentemporarytable-members.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
