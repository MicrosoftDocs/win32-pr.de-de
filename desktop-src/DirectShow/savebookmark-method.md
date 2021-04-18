---
description: Die savebookmark-Methode speichert die aktuelle Position und den Zustand des mswebdvd-Objekts, sodass der Benutzer später zum gleichen Ort zurückkehren kann.
ms.assetid: 975687c5-f93e-4473-b23b-63e0ae6bbb5d
title: Savebookmark-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2013a56d3f6885f7a4235497ad42bb03f0ebf7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364662"
---
# <a name="savebookmark-method"></a>Savebookmark-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SaveBookmark` -Methode speichert die aktuelle Position und den Zustand des **mswebdvd** -Objekts, sodass der Benutzer später zum gleichen Ort zurückkehren kann.

``` syntax
MSWebDVD.SaveBookmark()
```

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Ein Lesezeichen ist eine Momentaufnahme des aktuellen Zustands des DVD-Navigators. Hierzu gehören Informationen wie z. b. der Speicherort auf der Festplatte und welche Audiodaten Ströme ausgewählt werden. Durch das Speichern eines Lesezeichens kann der Benutzer die Anwendung schließen, den Computer Herunterfahren und später zurückkehren, um die CD direkt dort anzuzeigen, wo Sie aufgehört hat, und alle Einstellungen so wie zuvor. Es kann immer nur ein Lesezeichen gespeichert werden. Wenn Sie anrufen `SaveBookmark` , wird das alte Lesezeichen überschrieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Restorebookmark**](restorebookmark-method.md)
</dt> </dl>

 

 




