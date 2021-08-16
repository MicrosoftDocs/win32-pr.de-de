---
description: Die CurrentSubpictureStream-Eigenschaft legt den aktuellen Unterbilddatenstrom fest oder ruft den Datenstrom ab.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: CurrentSubpictureStream-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c4af677180d4893ef56a9d2bff1fb034971969e2e64d648d53e19d0814a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821945"
---
# <a name="currentsubpicturestream-property"></a>CurrentSubpictureStream-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `CurrentSubpictureStream` -Eigenschaft legt den aktuellen Unterbilddatenstrom fest oder ruft sie ab.

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der den Stream darstellt.

## <a name="remarks"></a>Hinweise

Die möglichen Werte dieser Eigenschaft sind:



| Wert   | Beschreibung              |
|---------|--------------------------|
| 0 bis 31 | Der Subpicture-Datenstrom    |
| 63      | Stummgeschalteter Datenstrom mit niedriger Bitrate |



 

Diese Eigenschaft ist Lese-/Schreibzugriff ohne Standardwert. Rufen Sie vor dem Festlegen eines neuen Subpicture-Streams [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) auf, um zu überprüfen, ob der Stream verfügbar ist.

Wenn Sie diese Eigenschaft festlegen, wird die [**SubpictureOn-Eigenschaft**](subpictureon-property.md) auf **True** umgeschaltet.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SubpictureOn**](subpictureon-property.md)
</dt> <dt>

[**SubpictureStreamsAvailable**](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



