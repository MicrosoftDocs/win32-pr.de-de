---
description: 'Weitere Informationen finden Sie unter: esentexception-Konstruktor (Zeichenfolge)'
title: Esentexception-Konstruktor (String) (Microsoft. ISAM. ESENT)
TOCTitle: EsentException constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100720
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22a93625b7becbe083a42fbd6fcc71ad801173ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366278"
---
# <a name="esentexception-constructor-string"></a>Esentexception-Konstruktor (Zeichenfolge)

Initialisiert eine neue Instanz der esentexception-Klasse mit einer angegebenen Fehlermeldung.

**Namespace:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Protected Sub New ( _
    message As String _
)
'Usage
Dim message As String

Dim instance As New EsentException(message)
```

``` csharp
protected EsentException(
    string message
)
```

#### <a name="parameters"></a>Parameter

  - message  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Die Meldung, in der der Fehler beschrieben wird.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentexception-Klasse](./esentexception-class.md)

[Esentexception-Member](./esentexception-members.md)

[Esentexception-Überladung](./esentexception-constructor.md)

[Microsoft. ISAM. ESENT-Namespace](./microsoft.isam.esent-namespace.md)
