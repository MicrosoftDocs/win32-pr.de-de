---
title: Wiedergabeliste. Kopieren
description: Die Copy-Methode startet einen Kopiervorgang von der CD.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- Wiedergabeliste. Windows-Media Player kopieren
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1c24de6af571eec948a92f666a76df6b65187c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370687"
---
# <a name="playlistcopy"></a>Wiedergabeliste. Kopieren

Die **Copy** -Methode startet einen Kopiervorgang von der CD.

``` syntax
        elementID.copy()
```

## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode kopiert nur die aktivierten Elemente in der Wiedergabeliste und funktioniert auf die gleiche Weise wie im Bereich **aus CD kopieren** im vollständigen Modus von Windows Media Player. Damit diese Methode funktioniert, muss sich eine CD auf dem CD-Laufwerk befinden. Legen Sie das **checkboxesvisible** -Attribut auf "true" fest, damit Benutzer einzelne Elemente auf einer CD vor dem Kopieren auswählen können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Wiedergabelisten Element**](playlist-element.md)
</dt> <dt>

[**Wiedergabeliste. abortcopy**](playlist-abortcopy.md)
</dt> <dt>

[**Wiedergabeliste. Kopieren**](playlist-copying.md)
</dt> </dl>

 

 





