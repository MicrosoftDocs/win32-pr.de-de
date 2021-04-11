---
description: Weitere Informationen finden Sie in der JET_ENUMCOLUMNVALUE. err-Eigenschaft.
title: JET_ENUMCOLUMNVALUE. err-Eigenschaft
TOCTitle: 'err property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.err
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue.err(v=EXCHG.10)
ms:contentKeyID: 55103626
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.err
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.get_err
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.err
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE.set_err
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f797d82ad09b75d961be24f2382b0895880427f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217555"
---
# <a name="jet_enumcolumnvalueerr-property"></a>JET_ENUMCOLUMNVALUE. err-Eigenschaft

Ruft den Spalten Statuscode ab, der sich aus der Enumeration des Spaltenwerts ergibt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property err As JET_wrn
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMNVALUE
Dim value As JET_wrn

value = instance.err
```

``` csharp
public JET_wrn err { get; internal set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_ENUMCOLUMNVALUE-Klasse](./jet-enumcolumnvalue-class.md)

[Mitglieder JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

[Columnnull](./jet-wrn-enumeration.md)

[Columnskipped](./jet-wrn-enumeration.md)

[Columntruncated](./jet-wrn-enumeration.md)
