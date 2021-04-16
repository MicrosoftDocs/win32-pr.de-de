---
description: 'Weitere Informationen finden Sie unter: esentresourceexception-Konstruktor (String, JET_err)'
title: Esentresourceexception-Konstruktor (Zeichenfolge, JET_err)
TOCTitle: EsentResourceException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResourceException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55107307
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 458b12a80fdc0e6d7883d966f2e50aa8c1f6d69b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529459"
---
# <a name="esentresourceexception-constructor-string-jet_err"></a>Esentresourceexception-Konstruktor (Zeichenfolge, JET_err)

Initialisiert eine neue Instanz der esentresourceexception-Klasse.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentResourceException(description, _
    err)
```

``` csharp
protected EsentResourceException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a>Parameter

  - description  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Die Beschreibung des Fehlers.

<!-- end list -->

  - irre  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)  
    
    Der Fehlercode der Ausnahme.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[EsentResourceException-Klasse](./esentresourceexception-class.md)

[Esentresourceexception-Member](./esentresourceexception-members.md)

[Esentresourceexception-Überladung](./esentresourceexception-constructor.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
