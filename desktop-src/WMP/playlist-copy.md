---
title: PLAYLIST.copy
description: Die Kopiermethode startet einen Kopiervorgang von der CD.
ms.assetid: 7d919ae5-456b-4cb9-ad52-9396f5c867d6
keywords:
- PLAYLIST.copy Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b897d22c1aa8e666c5de40aecb8ef63d17384957e82eee8dc7d569f0e71f57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003190"
---
# <a name="playlistcopy"></a>PLAYLIST.copy

Die **Kopiermethode** startet einen Kopiervorgang von der CD.

``` syntax
        elementID.copy()
```

## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode kopiert nur die überprüften Elemente in der Wiedergabeliste und funktioniert genauso wie im Bereich **Aus CD kopieren** im vollständigen Modus von Windows Media Player. Damit diese Methode funktioniert, muss sich eine CD auf dem CD-Laufwerk befindet. Legen Sie die **KontrollkästchenVisible-Attribut** auf TRUE fest, damit Benutzer einzelne Elemente auf einer CD vor dem Kopieren auswählen können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PLAYLIST-Element**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.abortCopy**](playlist-abortcopy.md)
</dt> <dt>

[**PLAYLIST.copying**](playlist-copying.md)
</dt> </dl>

 

 





