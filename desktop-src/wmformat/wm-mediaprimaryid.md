---
title: WM/mediaclassprimaryid
description: Das WM/mediaclassprimaryid-Attribut enthält die GUID der primären Medienklasse.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- WM/mediaclassprimaryid Windows Media-Format
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857579"
---
# <a name="wmmediaclassprimaryid"></a>WM/mediaclassprimaryid

Das **WM/mediaclassprimaryid-** Attribut enthält die GUID der primären Medienklasse.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmmediaclassprimaryid

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ- \_ GUID**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut sollte auf einen der Werte in der folgenden Tabelle festgelegt werden.



| GUID der primär Klasse                     | BESCHREIBUNG                                                  |
|----------------------------------------|--------------------------------------------------------------|
| "D1607DBC-E323-4BE2-86A1-48A42A28441E" | Verwenden Sie für Musikdateien. Nicht für Audiodaten verwenden, die kein Musik ist. |
| "DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B" | Verwenden Sie für Videodateien.                                         |
| "01cd0f 29-da4e-4157-897b-6275d50c4f" | Verwenden Sie dies für Audiodateien, die keine Musik sind.                      |
| "FCF24A76-9A57-4036-990D-E35DD8B244E1" | Verwenden Sie für Dateien, die weder Audiodaten noch Videos sind.               |



 

Wenn Sie einen Bezeichner der primären Klasse angeben, sollten Sie auch einen sekundären Klassen Bezeichner festlegen, um den Typ des Inhalts in der Datei zu verdeutlichen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> <dt>

[**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)
</dt> </dl>

 

 




