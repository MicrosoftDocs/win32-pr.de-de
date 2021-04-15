---
description: Weitere Informationen finden Sie in der API. GetBookmark-Methode.
title: API. GetBookmark-Methode
TOCTitle: 'GetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getbookmark(v=EXCHG.10)
ms:contentKeyID: 55100654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edcdfe7ddefadd993ef9c96e6dcc1416080b413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524794"
---
# <a name="apigetbookmark-method"></a>API. GetBookmark-Methode

Ruft das Lesezeichen für den Datensatz ab, der mit dem Index Eintrag an der aktuellen Position eines Cursors verknüpft ist. Dieses Lesezeichen kann dann verwendet werden, um den Cursor mithilfe von jetgobackbookmark wieder in denselben Datensatz zu positionieren.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function GetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Byte()

returnValue = Api.GetBookmark(sesid, _
    tableid)
```

``` csharp
public static byte[] GetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der Cursor, von dem das Lesezeichen abgerufen werden soll.

#### <a name="return-value"></a>Rückgabewert

Sorte \[\]  
Das Lesezeichen des Datensatzes.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
