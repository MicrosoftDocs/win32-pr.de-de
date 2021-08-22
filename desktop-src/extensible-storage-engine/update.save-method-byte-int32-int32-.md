---
description: 'Weitere Informationen zu: Update.Save-Methode (Byte, Int32, Int32)'
title: Update.Save-Methode (Byte, Int32, Int32)
TOCTitle: Save method (Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save(System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55107759
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17e586177075a34f3832486a9ace4a919abaad65dad21c0e54eba47b79f207be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603540"
---
# <a name="updatesave-method-byte--int32-int32"></a>Update.Save-Methode (Byte, Int32, Int32)

Aktualisieren Sie tableid.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Sub Save ( _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim instance As Update
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer

instance.Save(bookmark, bookmarkSize, _
    actualBookmarkSize)
```

``` csharp
public void Save(
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a>Parameter

  - Lesezeichen (bookmark)  
    Typ: \[\]  
    
    Gibt das Lesezeichen des aktualisierten Datensatzes zurück. Diese kann NULL sein.

<!-- end list -->

  - bookmarkSize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Größe des Lesezeichenpuffers.

<!-- end list -->

  - actualBookmarkSize  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Gibt die tatsächliche Größe des Lesezeichens zurück.

## <a name="remarks"></a>Hinweise

Speichern ist der letzte Schritt beim Ausführen einer Einfügung oder eines Updates. Das Update wird gestartet, indem ein Update-Objekt erstellt und dann mindestens ein Mal JetSetColumns oder JetSetColumns aufgerufen wird, um den Datensatzzustand festzulegen. Schließlich wird Update aufgerufen, um den Updatevorgang abzuschließen. Indizes werden nur durch Update oder aktualisiert und nicht während JetSetColumns oder JetSetColumns.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Update-Klasse](./update-class.md)

[Aktualisieren von Membern](./update-members.md)

[Speichern der Überladung](./update.save-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
