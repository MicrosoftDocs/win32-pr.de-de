---
title: WM/MediaClassPrimaryID
description: Das WM/MediaClassPrimaryID-Attribut enthält die GUID der primären Medienklasse.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- WM/MediaClassPrimaryID windows Media Format
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d650c15a861cdf55af07fba6d47fb416d61a56d399b855efc461cddd2f628edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027058"
---
# <a name="wmmediaclassprimaryid"></a>WM/MediaClassPrimaryID

Das **WM/MediaClassPrimaryID-Attribut** enthält die GUID der primären Medienklasse.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMMediaClassPrimaryID

## <a name="data-type"></a>Datentyp

**\_ \_ WMT-TYP-GUID**

## <a name="remarks"></a>Hinweise

Dieses Attribut sollte auf einen der Werte in der folgenden Tabelle festgelegt werden.



| Primäre Klassen-GUID                     | Beschreibung                                                  |
|----------------------------------------|--------------------------------------------------------------|
| "D1607DBC-E323-4BE2-86A1-48A42A28441E" | Wird für Musikdateien verwendet. Verwenden Sie nicht für Audiodaten, bei denen es sich nicht um Musik handelt. |
| "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B" | Wird für Videodateien verwendet.                                         |
| "01CD0F29-DA4E-4157-897B-6275D50C4F11" | Wird für Audiodateien verwendet, die keine Musik sind.                      |
| "FCF24A76-9A57-4036-990D-E35DD8B244E1" | Verwenden Sie für Dateien, bei denen es sich weder um Audio- noch um Videodateien handelt.               |



 

Wenn Sie einen primären Klassenbezeichner angeben, sollten Sie auch einen sekundären Klassenbezeichner festlegen, um den Inhaltstyp in der Datei zu verdeutlichen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)
</dt> </dl>

 

 




