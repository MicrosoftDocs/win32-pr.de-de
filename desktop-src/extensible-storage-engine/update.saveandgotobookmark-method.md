---
description: 'Weitere Informationen finden Sie hier: Update. saveandgodebookmark-Methode'
title: Update. saveandgodebookmark-Methode
TOCTitle: 'SaveAndGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.saveandgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55104204
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d682657b9821f782af339a3d0c3253b6fa771d37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356512"
---
# <a name="updatesaveandgotobookmark-method"></a>Update. saveandgodebookmark-Methode

Aktualisieren Sie TableID, und positionieren Sie TableID für den geänderten Datensatz. Dies kann hilfreich sein, wenn ein Datensatz eingefügt wird, da die TableID standardmäßig an der alten Position verbleibt.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Sub SaveAndGotoBookmark
'Usage
Dim instance As Update

instance.SaveAndGotoBookmark()
```

``` csharp
public void SaveAndGotoBookmark()
```

## <a name="remarks"></a>Bemerkungen

Speichern ist der letzte Schritt beim Ausführen einer INSERT-oder Update-Ausführung. Das Update wird zunächst durch Aufrufen eines Update Objekts und anschließendes Aufrufen von jetsetcolumn oder jetsetcolumns gestartet, um den Daten Satz Status festzulegen. Zum Schluss wird das Update aufgerufen, um den Aktualisierungs Vorgang abzuschließen. Indizes werden nur durch Update oder nicht von jetsetcolumn oder jetsetcolumns aktualisiert.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Update-Klasse](./update-class.md)

[Mitglieder aktualisieren](./update-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
