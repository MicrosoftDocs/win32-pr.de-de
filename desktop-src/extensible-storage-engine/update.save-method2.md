---
description: Weitere Informationen finden Sie unter Update.Save-Methode.
title: Update.Save-Methode
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
ms.openlocfilehash: 75927144f887ab5cd7dbfe05c6d8fbf4c690a0e29786c1834fa00f8e29fae76c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890061"
---
# <a name="updatesave-method"></a>Update.Save-Methode

Aktualisieren Sie tableid.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

## <a name="remarks"></a>Hinweise

Speichern ist der letzte Schritt beim Ausführen einer Einfügung oder eines Updates. Das Update wird gestartet, indem das Erstellen eines Update-Objekts und dann mindestens ein Mal JetSetColumns oder JetSetColumns aufgerufen wird, um den Datensatzzustand festzulegen. Schließlich wird Update aufgerufen, um den Updatevorgang abzuschließen. Indizes werden nur durch Update oder aktualisiert und nicht während JetSetColumns oder JetSetColumns.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Update-Klasse](./update-class.md)

[Aktualisieren von Membern](./update-members.md)

[Speichern der Überladung](./update.save-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
