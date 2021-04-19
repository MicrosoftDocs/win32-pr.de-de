---
title: Equalizersettings. speakersize
description: Das Attribut "speakersize" gibt die Indexnummer der aktuellen Redner Größe an oder ruft diese ab.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- Equalizersettings. speakersize-Windows-Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366987"
---
# <a name="equalizersettingsspeakersize"></a>Equalizersettings. speakersize

Das Attribut " **speakersize** " gibt die Indexnummer der aktuellen Redner Größe an oder ruft diese ab.

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzahl** (Long), die einen der folgenden Werte enthält.



| Wert | BESCHREIBUNG                              |
|-------|------------------------------------------|
| 0     | Die aktuellen Referenten sind Kopfhörer.     |
| 1     | Die aktuellen Redner haben eine normale Größe. |
| 2     | Die aktuellen Referenten sind groß.          |



 

## <a name="remarks"></a>Bemerkungen

Der Anzeige Name der Redner Größe kann mit dem **currentspeakername** -Attribut abgerufen werden.

Dieses Attribut wird ignoriert, wenn **enhancedaudiowert** auf false festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Equalizersettings-Element**](equalizersettings-element.md)
</dt> <dt>

[**Equalizersettings. currentspeakername**](equalizersettings-currentspeakername.md)
</dt> <dt>

[**Equalizersettings. enhancedaudio**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





