---
title: DownloadItem.type
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die type-Eigenschaft ruft den Typ des Downloads ab.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem.type Windows Media Player
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 038f348093a512095ee930c4147024bc789ead5edd3498243eb83a01608bfac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749711"
---
# <a name="downloaditemtype"></a>DownloadItem.type

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **type-Eigenschaft** ruft den Typ des Downloads ab.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge,** die einen der folgenden Werte enthält.



| Wert      | Beschreibung                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (nur Windows XP.) Der Download erfolgt als Hintergrundprozess, wenn die Prozessorzeit verfügbar wird. Downloadzustände bleiben auch dann erhalten, Windows Media Player oder Windows XP heruntergefahren wird. |
| Echtzeit  | (Alle unterstützten Betriebssysteme.) Der Download erfolgt auf einmal. Zwischen Sitzungen werden keine Downloadzustände beibehalten.                                                                       |



 

## <a name="remarks"></a>Hinweise

Jeder Downloadtyp hat Vor- und Nachteile. Das Herunterladen im Hintergrund ermöglicht es dem Benutzer, mit anderen Aufgaben fortzufahren und sogar Windows neu zu starten, ohne den Download abzubricht. Es dauert jedoch insgesamt mehr Zeit, um den Download durchzuführen, und wird nur für Windows XP unterstützt. Das Herunterladen in Echtzeit dauert weniger Zeit, erfordert jedoch, dass der Benutzer alle Downloads abgeschlossen hat, bevor er Windows Media Player.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DownloadItem-Objekt**](downloaditem-object.md)
</dt> </dl>

 

 





