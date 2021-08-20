---
description: 'Weitere Informationen zu: Instanzkonstruktor (String, String, TermGrbit)'
title: Instanzkonstruktor (String, String, TermGrbit)
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c341e13b35709fca7126fe346c2aad64d7ac15b96551716ad04a4fcded08981
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117895851"
---
# <a name="instance-constructor-string-string-termgrbit"></a>Instanzkonstruktor (String, String, TermGrbit)

Initialisiert eine neue Instanz der Instanzklasse. Die zugrunde liegende JET_INSTANCE zugeordnet, aber nicht initialisiert.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
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

<!-- end list -->

  - termGrbit  
    Typ: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)  
    
    Das TermGrbit, das zur JetTerm-Zeit verwendet werden soll.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Instanzklasse](./instance-class.md)

[Instanzmitglieder](./instance-members.md)

[Instanzüberladung](./instance-constructor.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
