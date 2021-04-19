---
title: Shadowfilepath-Attribut
description: Das shadowfilepath-Attribut ist der voll qualifizierte Pfad zu einer Schattendatei.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- Shadowfilepath-Attribut, Windows Media Player
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef79271995e9817315fb918049fc22491e232a5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366040"
---
# <a name="shadowfilepath-attribute"></a>Shadowfilepath-Attribut

Das **shadowfilepath** -Attribut ist der voll qualifizierte Pfad zu einer Schattendatei.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)

## <a name="remarks"></a>Bemerkungen

Eine *Schattendatei* wird als Teil einer Dateiformat Konvertierung erstellt. Dabei handelt es sich um die Kopie einer Datei, die der Player verwendet, wenn der Benutzerinhalte vom Computer mit einem Gerät synchronisiert, für das der Inhalt im ursprünglichen Dateiformat erforderlich ist. Dieses Attribut wird für die konvertierte Datei festgelegt, um auf den Speicherort der Schattendatei zu verweisen.

Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Informationen zum Konvertierungsprozess**](about-the-conversion-process.md)
</dt> <dt>

[**Attribut Verweis**](attribute-reference.md)
</dt> </dl>

 

 





