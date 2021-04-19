---
description: 'Weitere Informationen finden Sie unter: esentquotaexception-Konstruktor (String, JET_err)'
title: Esentquotaexception-Konstruktor (Zeichenfolge, JET_err)
TOCTitle: EsentQuotaException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentQuotaException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102558
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f615cf2a46beb8c504de3dcc7d6fab1fc23da47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362249"
---
# <a name="esentquotaexception-constructor-string-jet_err"></a>Esentquotaexception-Konstruktor (Zeichenfolge, JET_err)

Initialisiert eine neue Instanz der esentquotaexception-Klasse.

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

Dim instance As New EsentQuotaException(description, _
    err)
```

``` csharp
protected EsentQuotaException(
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

[EsentQuotaException-Klasse](./esentquotaexception-class.md)

[Esentquotaexception-Member](./esentquotaexception-members.md)

[Esentquotaexception-Überladung](./esentquotaexception-constructor.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
