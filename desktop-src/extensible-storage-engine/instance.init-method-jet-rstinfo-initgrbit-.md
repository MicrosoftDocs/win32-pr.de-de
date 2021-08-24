---
description: 'Weitere Informationen zu: Instance.Init-Methode (JET_RSTINFO, InitGrbit)'
title: Instance.Init-Methode (JET_RSTINFO, InitGrbit)
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
ms.openlocfilehash: 0e2a9975c42383c4ba0d58fb1a41dfeb1df07f81cebfd9b028bd54240bfb6b47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834440"
---
# <a name="instanceinit-method-jet_rstinfo-initgrbit"></a>Instance.Init-Methode (JET_RSTINFO, InitGrbit)

Initialisieren Sie die JET_INSTANCE. Diese API erfordert mindestens die Vista-Version von ESENT.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - recoveryOptions  
    Typ: [Microsoft.Isam.Esent.Interop.JET_RSTINFO](./jet-rstinfo-class.md)  
    
    Zusätzliche Wiederherstellungsparameter für die Neuzuordnung von Datenbanken während der Wiederherstellung, Position, an der die Wiederherstellung beendet werden soll, oder Wiederherstellungsstatus.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)  
    
    Initialisierungsoptionen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Instanzklasse](./instance-class.md)

[Instanzmember](./instance-members.md)

[Init-Überladung](./instance.init-method2.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
