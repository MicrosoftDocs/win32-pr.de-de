---
description: 'Weitere Informationen finden Sie hier: JET_OPENTEMPORARYTABLE. cbvarsegmac-Eigenschaft'
title: JET_OPENTEMPORARYTABLE. cbvarsegmac-Eigenschaft (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cbVarSegMac property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbvarsegmac(v=EXCHG.10)
ms:contentKeyID: 55104115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbVarSegMac
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37fe218a9741235410d2452f04f082dc6673eaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363517"
---
# <a name="jet_opentemporarytablecbvarsegmac-property"></a>JET_OPENTEMPORARYTABLE. cbvarsegmac (Eigenschaft)

Ruft die maximale Datenmenge ab oder legt Sie fest, die von einer beliebigen Variablen Längen Spalte verwendet wird, um einen Schlüssel für eine bestimmte Zeile zu erstellen. Dieser Parameter kann verwendet werden, um die Menge des von einer bestimmten Schlüssel Spalte genutzten schlüsselplatzes zu steuern. Dieser Grenzwert ist in Bytes. Wenn dieser Parameter 0 (null) ist oder mit der [cbkeymost](./jet-opentemporarytable.cbkeymost-property.md) -Eigenschaft identisch ist, ist kein Limit wirksam.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbVarSegMac As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbVarSegMac

instance.cbVarSegMac = value
```

``` csharp
public int cbVarSegMac { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_OPENTEMPORARYTABLE-Klasse](./jet-opentemporarytable-class.md)

[Mitglieder JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
