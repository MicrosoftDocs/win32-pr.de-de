---
description: 'Weitere Informationen finden Sie unter: esentdataexception-Konstruktor (String, JET_err)'
title: Esentdataexception-Konstruktor (Zeichenfolge, JET_err)
TOCTitle: EsentDataException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDataException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101571
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e39638d6e5458c0dcc555f31bec12e752d84337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130920"
---
# <a name="esentdataexception-constructor-string-jet_err"></a>Esentdataexception-Konstruktor (Zeichenfolge, JET_err)

Initialisiert eine neue Instanz der esentdataexception-Klasse.

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

Dim instance As New EsentDataException(description, _
    err)
```

``` csharp
protected EsentDataException(
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

[Esentdataexception-Klasse](./esentdataexception-class.md)

[Esentdataexception-Member](./esentdataexception-members.md)

[Esentdataexception-Überladung](./esentdataexception-constructor.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
