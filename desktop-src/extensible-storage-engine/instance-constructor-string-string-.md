---
description: 'Weitere Informationen zu: Instanzkonstruktor (Zeichenfolge, Zeichenfolge)'
title: Instanzkonstruktor (String, String)
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
ms.openlocfilehash: 2d93a5799a646a90688261bdd55bc9dfe929ef6bd074a51e15cabdcee768ffa2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116440"
---
# <a name="instance-constructor-string-string"></a>Instanzkonstruktor (String, String)

Initialisiert eine neue Instanz der Instanzklasse. Die zugrunde liegende JET_INSTANCE wird zugeordnet, aber nicht initialisiert.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Typ: [System.String](/dotnet/api/system.string)  
    
    Der Name der Instanz. Diese Zeichenfolge muss innerhalb eines bestimmten Prozesses, der die Datenbank-Engine hosten, eindeutig sein.

<!-- end list -->

  - displayName  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Ein Anzeigename für die Instanz. Dies wird in Eventlogeinträgen verwendet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Instanzklasse](./instance-class.md)

[Instanzmitglieder](./instance-members.md)

[Instanzüberladung](./instance-constructor.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
