---
description: 'Weitere Informationen finden Sie unter: EsentFatalException-Konstruktor (String, JET_err)'
title: EsentFatalException-Konstruktor (String, JET_err)
TOCTitle: EsentFatalException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFatalException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101610
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f258d291961add7f97fd8f67da46bc2e3e64d57eda942fbffd9aeded7f15aafc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118778508"
---
# <a name="esentfatalexception-constructor-string-jet_err"></a>EsentFatalException-Konstruktor (String, JET_err)

Initialisiert eine neue Instanz der EsentFatalException-Klasse.

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

Dim instance As New EsentFatalException(description, _
    err)
```

``` csharp
protected EsentFatalException(
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

[EsentFatalException-Klasse](./esentfatalexception-class.md)

[EsentFatalException-Member](./esentfatalexception-members.md)

[EsentFatalException-Überladung](./esentfatalexception-constructor.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
