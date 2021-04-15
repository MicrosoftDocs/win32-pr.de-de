---
description: 'Weitere Informationen finden Sie unter: Update. Save-Methode (Byte, Int32, Int32)'
title: Update. Save-Methode (Byte, Int32, Int32)
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
ms.openlocfilehash: e2c798f22039ced1bab30ecaa9c3f650079be0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485155"
---
# <a name="updatesave-method-byte--int32-int32"></a>Update. Save-Methode (Byte, Int32, Int32)

Aktualisieren Sie TableID.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Sorte \[\]  
    
    Gibt das Lesezeichen des aktualisierten Datensatzes zurück. Diese kann NULL sein.

<!-- end list -->

  - bookmarksize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Größe des Lesezeichen Puffers.

<!-- end list -->

  - actualbookmarksize  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Gibt die tatsächliche Größe des Lesezeichens zurück.

## <a name="remarks"></a>Bemerkungen

Speichern ist der letzte Schritt beim Ausführen einer INSERT-oder Update-Ausführung. Das Update wird zunächst durch Aufrufen eines Update Objekts und anschließendes Aufrufen von jetsetcolumn oder jetsetcolumns gestartet, um den Daten Satz Status festzulegen. Zum Schluss wird das Update aufgerufen, um den Aktualisierungs Vorgang abzuschließen. Indizes werden nur durch Update oder nicht von jetsetcolumn oder jetsetcolumns aktualisiert.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Update-Klasse](./update-class.md)

[Mitglieder aktualisieren](./update-members.md)

[Überladung speichern](./update.save-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
