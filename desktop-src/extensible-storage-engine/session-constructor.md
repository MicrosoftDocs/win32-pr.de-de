---
description: 'Weitere Informationen: Sitzungskonstruktor'
title: Sitzungskonstruktor
TOCTitle: 'Session constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.session(v=EXCHG.10)
ms:contentKeyID: 55107728
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Session
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73d19d5ae1ba422969cd5b11f5b59ceb2811a89d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216285"
---
# <a name="session-constructor"></a>Sitzungskonstruktor

Initialisiert eine neue Instanz der Session-Klasse. Eine neue JET_SESSION wird von der angegebenen-Instanz zugeordnet.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCE

Dim instance As New Session(instance)
```

``` csharp
public Session(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die-Instanz, in der die Sitzung gestartet werden soll.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Sitzungsklasse](./session-class.md)

[Sitzungs Mitglieder](./session-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
