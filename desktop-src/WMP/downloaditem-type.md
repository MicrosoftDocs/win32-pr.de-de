---
title: Download Item. Type
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Type-Eigenschaft ruft den Typ des Downloads ab.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- Download Item. Type Windows Media Player
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
ms.openlocfilehash: 4cdcf21ce7443d7730d4a75518fb4749af0b9e52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351234"
---
# <a name="downloaditemtype"></a>Download Item. Type

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **Type** -Eigenschaft ruft den Typ des Downloads ab.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** , die einen der folgenden Werte enthält.



| Wert      | BESCHREIBUNG                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (Nur Windows XP.) Der Download erfolgt als Hintergrundprozess, wenn die Prozessorzeit verfügbar wird. Download Zustände bleiben auch dann erhalten, wenn Windows Media Player oder Windows XP heruntergefahren wird. |
| Echt Zeit  | (Alle unterstützten Betriebssysteme) Der Download erfolgt alle auf einmal. Zwischen den Sitzungen bleiben keine Download Zustände erhalten.                                                                       |



 

## <a name="remarks"></a>Bemerkungen

Jede Art von Download hat vor-und Nachteile. Durch das Herunterladen im Hintergrund kann der Benutzer mit anderen Aufgaben fortfahren und Windows neu starten, ohne den Download abzubrechen, aber es dauert mehr Zeit, bis der Download durchgeführt wird, und wird nur für Windows XP unterstützt. Das Herunterladen in Echtzeit dauert weniger Zeit, erfordert jedoch, dass der Benutzer vor dem Schließen von Windows Media Player den gesamten Download abgeschlossen hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Download Item-Objekt**](downloaditem-object.md)
</dt> </dl>

 

 





