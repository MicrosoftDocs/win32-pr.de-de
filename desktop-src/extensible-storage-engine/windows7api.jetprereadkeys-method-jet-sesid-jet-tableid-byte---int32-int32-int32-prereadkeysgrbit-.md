---
description: 'Weitere Informationen finden Sie unter: Windows7Api.JetPrereadKeys-Methode (JET_SESID, JET_TABLEID, Byte[][], Int32, Int32, Int32, PrereadKeysGrbit)'
title: Windows7Api.JetPrereadKeys-Methode (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, PrereadKeysGrbit) (Microsoft.Isam.Esent.Interop.Windows7)
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55107785
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6880e7fa1520f55f4cf1dd8300c4f7b75002a84e164cd80e1be341a0548bd9fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470890"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-prereadkeysgrbit"></a>Windows7Api.JetPrereadKeys-Methode (JET_SESID, JET_TABLEID, Byte, \[ \] \[ \] Int32 , Int32, Int32, PrereadKeysGrbit)

Wenn sich die Datensätze mit den angegebenen Schlüsseln nicht im Puffercache befinden, starten Sie asynchrone Leseläufe, um die Datensätze in den Datenbankpuffercache zu übertragen.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyCount, keysPreread, _
    grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Die Tabelle, für die die Prereads ausgefertigt werden.

<!-- end list -->

  - keys  
    Typ: \[\]  
    
    Die schlüssel, die im Voraus gelesen werden. Die Schlüssel müssen sortiert werden.

<!-- end list -->

  - keyLengths  
    Typ: \[\]  
    
    Die Längen der Schlüssel, die vorgelesen werden.

<!-- end list -->

  - keyCount  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die maximale Anzahl von Schlüsseln, die vorab gelesen werden müssen.

<!-- end list -->

  - keysPreread  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Gibt die Anzahl der Schlüssel zurück, die tatsächlich vorgelesen werden.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)  
    
    Vorableseoptionen. Wird verwendet, um die Richtung des Vorlesens anzugeben.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Windows7Api-Klasse](./windows7api-class.md)

[Windows7Api-Member](./windows7api-members.md)

[JetPrereadKeys-Überladung](./windows7api.jetprereadkeys-method.md)

[Microsoft.Isam.Esent.Interop.Windows7-Namespace](./microsoft.isam.esent.interop.windows7-namespace.md)
