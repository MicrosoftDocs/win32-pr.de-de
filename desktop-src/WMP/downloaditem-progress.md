---
title: Download Item. Progress
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Status-Eigenschaft ruft den Fortschritt des Downloads in Bytes ab.
ms.assetid: 58644eac-8dd0-4e9d-8055-03833c863a6e
keywords:
- Download Element. Progress (Windows-Media Player
topic_type:
- apiref
api_name:
- DownloadItem.progress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a1967c1eb3dc72c00b8b10b70da5d797343e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369617"
---
# <a name="downloaditemprogress"></a>Download Item. Progress

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die Status **-Eigenschaft ruft den fort** Schritt des Downloads in Bytes ab.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).progress
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Download Item-Objekt**](downloaditem-object.md)
</dt> <dt>

[**Download Item. Size**](downloaditem-size.md)
</dt> </dl>

 

 





