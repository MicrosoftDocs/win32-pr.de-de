---
description: Die imediaobjectimpl-Klassen Vorlage stellt eine Basis Implementierung für die imediaobject-Schnittstelle bereit. Weitere Informationen zur Verwendung dieser Vorlage finden Sie unter Verwenden der DMO-Klassen Vorlage.
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: Imediaobjectimpl-Klassen Vorlage (dmuimpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfa1be82ffeaa9e05eb6460249e0c40bb2989c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373871"
---
# <a name="imediaobjectimpl-class-template"></a>Imediaobjectimpl-Klassen Vorlage

Die `IMediaObjectImpl` Klassen Vorlage stellt eine Basis Implementierung für die [**imediaobject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) -Schnittstelle bereit. Weitere Informationen zur Verwendung dieser Vorlage finden Sie unter [Verwenden der DMO-Klassen Vorlage](using-the-dmo-class-template.md).

Diese `IMediaObjectImpl` Vorlage macht die folgenden Member verfügbar.



| -Klasse                              | BESCHREIBUNG                                  |
|-------------------------------------------|----------------------------------------------|
| [**Sperren**](imediaobjectimpl-lockit.md) | Hilfsklasse, die den DMO sperrt und entsperrt. |



 



| Methode                                                                      | BESCHREIBUNG                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**Checktypesset**](/previous-versions/ms807621(v=msdn.10))                     | Bestimmt, ob alle nicht optionalen Streams über Medientypen verfügen. |
| [**InputType**](/previous-versions/ms807633(v=msdn.10))                             | Ruft den aktuellen Medientyp für einen angegebenen Eingabedaten Strom ab.       |
| [**Inputtypeset**](/previous-versions/ms807638(v=msdn.10))                       | Fragt ab, ob der Medientyp für einen Eingabestream festgelegt wurde.           |
| [**Internalakzeptinginput**](/previous-versions/ms809095(v=msdn.10))   | Fragt ab, ob ein Eingabedaten Strom mehr Eingaben akzeptieren kann.               |
| [**Internalcheckinputtype**](/previous-versions/ms809096(v=msdn.10))   | Fragt ab, ob ein Eingabedaten Strom einen bestimmten Medientyp annehmen kann.       |
| [**Internalcheckoutputtype**](/previous-versions/ms809098(v=msdn.10)) | Fragt ab, ob ein Ausgabestream einen bestimmten Medientyp annehmen kann.      |
| [**Sperre**](/previous-versions/ms809100(v=msdn.10))                                       | Sperrt den DMO.                                                        |
| [**OutputType**](/previous-versions/ms807644(v=msdn.10))                           | Ruft den aktuellen Medientyp für einen angegebenen Ausgabestream ab.      |
| [**Outputtypeset**](/previous-versions/ms807649(v=msdn.10))                     | Fragt ab, ob der Medientyp für einen Ausgabestream festgelegt wurde.          |
| [**Entsperren**](/previous-versions/ms809101(v=msdn.10))                                   | Entsperrt den DMO                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dmuimpl. h</dt> </dl>                                                                     |
| Bibliothek<br/> | <dl> <dt>Dmuguids. lib; </dt> <dt>Msdmo. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DMO-Referenz](dmo-reference.md)
</dt> <dt>

[Verwenden der DMO-Klassen Vorlage](using-the-dmo-class-template.md)
</dt> </dl>

 

 
