---
description: 'Weitere Informationen finden Sie unter: Windows7Api. jetprereadkeys-Methode (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, Int32, prereadkeysgrbit)'
title: Windows7Api. jetprereadkeys-Methode (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, Int32, prereadkeysgrbit) (Microsoft. ISAM. ESENT. Interop. Windows7)
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55104374
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
ms.openlocfilehash: a799c890887df730fdad97ad4d08fa500a6dd4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214891"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-int32-prereadkeysgrbit"></a>Windows7Api. jetprereadkeys-Methode (JET_SESID, JET_TABLEID, Byte \[ \] \[ \] , Int32, Int32, Int32, Int32, prereadkeysgrbit)

Wenn sich die Datensätze mit den angegebenen Schlüsseln nicht im Puffer Cache befinden, starten Sie asynchrone Lesevorgänge, um die Datensätze in den Daten Bank Puffer Cache zu übertragen.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyIndex As Integer, _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyIndex As Integer
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyIndex, keyCount, _
    keysPreread, grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyIndex,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Die Tabelle, für die die prereads ausgestellt werden sollen.

<!-- end list -->

  - keys  
    Sorte \[\]  
    
    Die Schlüssel für die voraus Anzeige. Die Schlüssel müssen sortiert werden.

<!-- end list -->

  - keylängen  
    Sorte \[\]  
    
    Die Längen der Schlüssel für die Voraussetzungen.

<!-- end list -->

  - keyIndex  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Der Index des ersten Schlüssels im Schlüssel Array, der gelesen werden soll.

<!-- end list -->

  - keycount  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die maximal zulässige Anzahl von Schlüsseln, die Voraussetzungen für die Anzeige sind.

<!-- end list -->

  - keyspreread  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Gibt die Anzahl der Schlüssel zurück, die tatsächlich vorab registriert werden sollen.

<!-- end list -->

  - grbit  
    Geben Sie Folgendes ein: [Microsoft. ISAM. ESENT. Interop. Windows7. prereadkeysgrbit](./prereadkeysgrbit-enumeration.md)  
    
    Preread-Optionen. Wird verwendet, um die Richtung der Preread anzugeben.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Windows7Api-Klasse](./windows7api-class.md)

[Windows7Api-Member](./windows7api-members.md)

[Jetprereadkeys-Überladung](./windows7api.jetprereadkeys-method.md)

[Microsoft. ISAM. ESENT. Interop. Windows7-Namespace](./microsoft.isam.esent.interop.windows7-namespace.md)
