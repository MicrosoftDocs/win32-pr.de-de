---
description: 'Weitere Informationen finden Sie unter: API. jetretrievekey-Methode'
title: API. jetretrievekey-Methode
TOCTitle: 'JetRetrieveKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievekey(v=EXCHG.10)
ms:contentKeyID: 55100795
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ebf130b4542992e18de49d58801f789d40106fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369868"
---
# <a name="apijetretrievekey-method"></a>API. jetretrievekey-Methode

Ruft den Schlüssel für den Index Eintrag an der aktuellen Position eines Cursors ab. Siehe auch [retrievekey (JET_SESID, JET_TABLEID, retrievekeygrbit)](./api.retrievekey-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetRetrieveKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveKeyGrbitApi.JetRetrieveKey(sesid, tableid, _
    data, dataSize, actualDataSize, grbit)
```

``` csharp
public static void JetRetrieveKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveKeyGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, aus dem der Schlüssel abgerufen werden soll.

<!-- end list -->

  - Daten  
    Sorte \[\]  
    
    Der Puffer, in den der Schlüssel abgerufen werden soll.

<!-- end list -->

  - dataSize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Größe des Puffers.

<!-- end list -->

  - actualdatasize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Gibt die tatsächliche Größe der Daten zurück.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. retrievekeygrbit](./retrievekeygrbit-enumeration.md)  
    
    Abrufen von Schlüsseloptionen

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
