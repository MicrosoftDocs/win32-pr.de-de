---
description: 'Weitere Informationen zu: EsentApiException-Konstruktor (String, JET_err)'
title: EsentApiException-Konstruktor (String, JET_err)
TOCTitle: EsentApiException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentApiException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101058
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f13858d07b10ff222e58d851ceafa086eaaeeeedcfd83765c8732869a619c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117716129"
---
# <a name="esentapiexception-constructor-string-jet_err"></a>EsentApiException-Konstruktor (String, JET_err)

Initialisiert eine neue Instanz der EsentApiException-Klasse.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Dim instance As New EsentApiException(description, _
    err)
```

``` csharp
protected EsentApiException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a>Parameter

  - description  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Die Beschreibung des Fehlers.

<!-- end list -->

  - Err  
    Typ: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)  
    
    Der Fehlercode der Ausnahme.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentApiException-Klasse](./esentapiexception-class.md)

[EsentApiException-Member](./esentapiexception-members.md)

[EsentApiException-Überladung](./esentapiexception-constructor.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
