---
description: 'Weitere Informationen finden Sie unter: Instance.Init-Methode (JET_RSTINFO, initgrbit)'
title: Instance.Init-Methode (JET_RSTINFO, initgrbit)
TOCTitle: Init method (JET_RSTINFO, InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103274
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1945b0119053a2759b57b8781b86cf682b3a364c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354544"
---
# <a name="instanceinit-method-jet_rstinfo-initgrbit"></a>Instance.Init-Methode (JET_RSTINFO, initgrbit)

Initialisieren Sie die JET_INSTANCE. Diese API erfordert mindestens die Vista-Version von ESENT.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit

instance.Init(recoveryOptions, grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - Wiederherstellungsoptionen  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_RSTINFO](./jet-rstinfo-class.md)  
    
    Zusätzliche Wiederherstellungs Parameter zum erneuten Zuordnen von Datenbanken während der Wiederherstellung, zur Position, an der die Wiederherstellung beendet werden soll, oder zur

<!-- end list -->

  - grbit  
    Type: [Microsoft.Isam.Esent.Interop.Initgrbit](./initgrbit-enumeration.md)  
    
    Initialisierungs Optionen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanzklasse](./instance-class.md)

[Instanzmember](./instance-members.md)

[Init-Überladung](./instance.init-method2.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
