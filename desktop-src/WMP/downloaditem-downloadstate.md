---
title: Downloadaditem. DownloadState
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die DownloadState-Eigenschaft ruft den Status des Downloads ab.
ms.assetid: dde27f43-40ee-4eb9-b316-42312ee937d0
keywords:
- Download Status-Windows-Media Player
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
ms.openlocfilehash: fbd2af2fab2ecb69df5b4695b227631b5be2dd96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358142"
---
# <a name="downloaditemdownloadstate"></a>Downloadaditem. DownloadState

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **DownloadState** -Eigenschaft ruft den Status des Downloads ab.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).downloadState
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** , die einen der folgenden Werte enthält.



| Wert | BESCHREIBUNG |
|-------|-------------|
| 0     | Herunterladen |
| 1     | Angehalten      |
| 2     | Verarbeitung  |
| 3     | Abgeschlossen   |
| 4     | Canceled    |



 

## <a name="remarks"></a>Bemerkungen

Download Zustände können in beliebiger Reihenfolge auftreten. Schreiben Sie keinen Code, der von dem Vorkommen eines bestimmten Download Status abhängt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Download Item-Objekt**](downloaditem-object.md)
</dt> </dl>

 

 





