---
description: Beachten Sie, dass diese Schnittstelle veraltet ist.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: Iamfilterdata-Schnittstelle (fil \_ Data. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368368"
---
# <a name="iamfilterdata-interface"></a>Iamfilterdata-Schnittstelle

> [!Note]  
> Diese Schnittstelle ist veraltet. Neue Anwendungen sollten stattdessen die [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) -Schnittstelle verwenden.

 

Die- `IAMFilterData` Schnittstelle konvertiert Filter Informationen in gepackte Binärdaten, die in der Registrierung gespeichert werden können. Diese Schnittstelle wird vom filtermapper-Objekt verfügbar gemacht.

## <a name="members"></a>Member

Die **iamfilterdata** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamfilterdata** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamfilterdata** -Schnittstelle verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [**"Kreatefilterdata"**](iamfilterdata-createfilterdata.md) | Erstellt binäre Registrierungsdaten für einen Filter.<br/>     |
| [**"Parameterfilterdata"**](iamfilterdata-parsefilterdata.md)   | Entpackt die binären Registrierungsdaten für einen Filter.<br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Der Header "fil \_ Data. h" befindet sich im Verzeichnis " [Mapper Sample](mapper-sample.md) " in der Windows SDK.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Fil- \_ Daten. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Veraltete Schnittstellen](deprecated-interfaces.md)
</dt> </dl>

 

 
