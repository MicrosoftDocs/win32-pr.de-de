---
description: Weitere Informationen finden Sie in der Update. Save-Methode.
title: Update. Save-Methode
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad933c9601dc1a20932550aef363e067458ff79e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389029"
---
# <a name="updatesave-method"></a>Update. Save-Methode

Aktualisieren Sie TableID.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a>Bemerkungen

Speichern ist der letzte Schritt beim Ausführen einer INSERT-oder Update-Ausführung. Das Update wird zunächst durch Aufrufen eines Update Objekts und anschließendes Aufrufen von jetsetcolumn oder jetsetcolumns gestartet, um den Daten Satz Status festzulegen. Zum Schluss wird das Update aufgerufen, um den Aktualisierungs Vorgang abzuschließen. Indizes werden nur durch Update oder nicht von jetsetcolumn oder jetsetcolumns aktualisiert.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Update-Klasse](./update-class.md)

[Mitglieder aktualisieren](./update-members.md)

[Überladung speichern](./update.save-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
