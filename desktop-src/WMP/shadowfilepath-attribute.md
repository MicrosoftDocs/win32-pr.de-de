---
title: ShadowFilePath-Attribut
description: Das ShadowFilePath-Attribut ist der vollqualifizierte Pfad zu einer Schattendatei.
ms.assetid: dd00d53c-8a95-450c-a65b-1763e9112941
keywords:
- ShadowFilePath-Attribut Windows Media Player
topic_type:
- apiref
api_name:
- ShadowFilePath
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf1e8f2eb5cb810004ea219aac62973377111902071beb78eca051df19877f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002150"
---
# <a name="shadowfilepath-attribute"></a>ShadowFilePath-Attribut

Das **ShadowFilePath-Attribut** ist der vollqualifizierte Pfad zu einer Schattendatei.

## <a name="applies-to"></a>Gilt für

-   [Audioelemente](audio-item-attributes.md)

## <a name="remarks"></a>Hinweise

Eine *Schattendatei* wird im Rahmen einer Dateiformatkonvertierung erstellt. Dies ist die Kopie einer Datei, die der Player verwendet, wenn der Benutzer Inhalte vom Computer mit einem Gerät synchronisiert, für das der Inhalt das ursprüngliche Dateiformat aufweisen muss. Dieses Attribut wird festgelegt, damit die konvertierte Datei auf den Speicherort der Schattendatei verweist.

Verwenden Sie die [Media.isReadOnlyItem-Methode,](media-isreadonlyitem.md) um zu bestimmen, ob Sie den Wert dieses Attributs ändern können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Informationen zum Konvertierungsprozess**](about-the-conversion-process.md)
</dt> <dt>

[**Attributverweis**](attribute-reference.md)
</dt> </dl>

 

 





