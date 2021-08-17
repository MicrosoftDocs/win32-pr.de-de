---
description: Die IMediaObjectImpl-Klassenvorlage stellt eine Basisimplementierung für die IMediaObject-Schnittstelle bereit. Weitere Informationen zur Verwendung dieser Vorlage finden Sie unter Verwenden der DMO-Klassenvorlage.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: IMediaObjectImpl-Klassenvorlage (Dmoimpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b166836ff4da6100f61fca5d3a0c2887462b37adcbdd2ec61abeb919553a59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015578"
---
# <a name="imediaobjectimpl-class-template"></a>IMediaObjectImpl-Klassenvorlage

Die `IMediaObjectImpl` Klassenvorlage stellt eine Basisimplementierung für die [**IMediaObject-Schnittstelle**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) bereit. Weitere Informationen zur Verwendung dieser Vorlage finden Sie unter [Verwenden der DMO-Klassenvorlage.](using-the-dmo-class-template.md)

Diese `IMediaObjectImpl` Vorlage macht die folgenden Member verfügbar.



| Geschachtelte Klasse                              | Beschreibung                                  |
|-------------------------------------------|----------------------------------------------|
| [**LockIt**](imediaobjectimpl-lockit.md) | Hilfsklasse, die die -Klasse sperrt und entsperrt DMO. |



 



| Methode                                                                      | Beschreibung                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))                     | Bestimmt, ob alle nicht optionalen Streams Medientypen haben. |
| [**InputType**](/previous-versions/ms807633(v=msdn.10))                             | Ruft den aktuellen Medientyp für einen angegebenen Eingabestream ab.       |
| [**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))                       | Fragt ab, ob der Medientyp für einen Eingabestream festgelegt wurde.           |
| [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))   | Fragt ab, ob ein Eingabestream mehr Eingaben akzeptieren kann.               |
| [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))   | Fragt ab, ob ein Eingabestream einen bestimmten Medientyp akzeptieren kann.       |
| [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10)) | Fragt ab, ob ein Ausgabestream einen bestimmten Medientyp akzeptieren kann.      |
| [**Sperre**](/previous-versions/ms809100(v=msdn.10))                                       | Sperrt die DMO                                                        |
| [**Outputtype**](/previous-versions/ms807644(v=msdn.10))                           | Ruft den aktuellen Medientyp für einen angegebenen Ausgabestream ab.      |
| [**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))                     | Fragt ab, ob der Medientyp für einen Ausgabestream festgelegt wurde.          |
| [**Entsperren**](/previous-versions/ms809101(v=msdn.10))                                   | Entsperrt die DMO                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dmoimpl.h</dt> </dl>                                                                     |
| Bibliothek<br/> | <dl> <dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DMO Verweis](dmo-reference.md)
</dt> <dt>

[Verwenden der DMO-Klassenvorlage](using-the-dmo-class-template.md)
</dt> </dl>

 

 
