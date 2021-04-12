---
description: 'Weitere Informationen: Instanzkonstruktor (Zeichenfolge, Zeichenfolge)'
title: Instanzkonstruktor (Zeichenfolge, Zeichenfolge)
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02cb629cdfaba17ce9a137b52eb1a6d6fdbaa56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344229"
---
# <a name="instance-constructor-string-string"></a>Instanzkonstruktor (Zeichenfolge, Zeichenfolge)

Initialisiert eine neue Instanz der Instanzklasse. Die zugrunde liegende JET_INSTANCE ist zugeordnet, aber nicht initialisiert.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
)
```

#### <a name="parameters"></a>Parameter

  - name  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Der Name der Instanz. Diese Zeichenfolge muss innerhalb eines bestimmten Prozesses, der die Datenbank-Engine gehostet, eindeutig sein.

<!-- end list -->

  - displayName  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Ein Anzeige Name für die-Instanz. Diese wird in EventLog-Einträgen verwendet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanzklasse](./instance-class.md)

[Instanzmember](./instance-members.md)

[Instanzüberladung](./instance-constructor.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
