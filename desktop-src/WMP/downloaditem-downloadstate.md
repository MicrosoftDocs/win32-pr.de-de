---
title: DownloadItem.downloadState
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die downloadState-Eigenschaft ruft den Status des Downloads ab.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- DownloadItem.downloadState Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.downloadState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f2f1d7338370aaa5132c479d155ffbfc4282a686d082df37446be053efab3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997050"
---
# <a name="downloaditemdownloadstate"></a>DownloadItem.downloadState

> [!Note]  
> In diesem Abschnitt werden funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **downloadState-Eigenschaft** ruft den Status des Downloads ab.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl,** die einen der folgenden Werte enthält.



| Wert | Beschreibung |
|-------|-------------|
| 0     | Herunterladen |
| 1     | Angehalten      |
| 2     | Verarbeitung  |
| 3     | Abgeschlossen   |
| 4     | Canceled    |



 

## <a name="remarks"></a>Hinweise

Downloadzustände können in beliebiger Reihenfolge auftreten. Schreiben Sie keinen Code, der vom Auftreten eines bestimmten Downloadzustands abhängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DownloadItem-Objekt**](downloaditem-object.md)
</dt> </dl>

 

 





