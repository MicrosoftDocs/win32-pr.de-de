---
description: 'Weitere Informationen finden Sie unter: Update.SaveAndGotoBookmark-Methode'
title: Update.SaveAndGotoBookmark-Methode
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
ms.openlocfilehash: 566be9b1af403a794b6ac87259a0fd6b6c0fea46c0b45287c536f336ee734b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106954"
---
# <a name="updatesaveandgotobookmark-method"></a>Update.SaveAndGotoBookmark-Methode

Aktualisieren Sie die tableid, und positionieren Sie die tableid im geänderten Datensatz. Dies kann beim Einfügen eines Datensatzes nützlich sein, da die tableid standardmäßig an ihrer alten Position verbleibt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

## <a name="remarks"></a>Hinweise

Speichern ist der letzte Schritt beim Ausführen eines Einfüge- oder Aktualisierungsschritts. Das Update wird gestartet, indem das Erstellen eines Update-Objekts und dann JetSetColumn oder JetSetColumns einmal oder mehrmals zum Festlegen des Datensatzzustands aufruft. Zum Schluss wird Update aufgerufen, um den Updatevorgang abschließen zu können. Indizes werden nur durch Update oder und nicht während JetSetColumn oder JetSetColumns aktualisiert.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Update-Klasse](./update-class.md)

[Aktualisieren von Mitgliedern](./update-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
