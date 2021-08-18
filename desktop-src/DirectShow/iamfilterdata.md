---
description: Erfahren Sie mehr über die IAMFilterData-Schnittstelle, die Filterinformationen in gepackte Binärdaten konvertiert. Diese Schnittstelle ist veraltet.
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: IAMFilterData-Schnittstelle (File \_ data.h)
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
ms.openlocfilehash: 9174549c93a76f94ccb7f039343a8eab5e75ece252871d11d60221df03aabe87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823600"
---
# <a name="iamfilterdata-interface"></a>IAMFilterData-Schnittstelle

> [!Note]  
> Diese Schnittstelle ist veraltet. Neue Anwendungen sollten stattdessen die [**IFilterMapper2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) verwenden.

 

Die `IAMFilterData` Schnittstelle konvertiert Filterinformationen in gepackte Binärdaten, die in der Registrierung gespeichert werden können. Das Filterzuordnungsobjekt macht diese Schnittstelle verfügbar.

## <a name="members"></a>Member

Die **IAMFilterData-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMFilterData** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAMFilterData-Schnittstelle** verfügt über diese Methoden.



| Methode                                                     | Beschreibung                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [**CreateFilterData**](iamfilterdata-createfilterdata.md) | Erstellt binäre Registrierungsdaten für einen Filter.<br/>     |
| [**ParseFilterData**](iamfilterdata-parsefilterdata.md)   | Entpackt die binären Registrierungsdaten für einen Filter.<br/> |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Der Header Fil \_ data.h befindet sich im [Verzeichnis Mapper Sample](mapper-sample.md) im Windows SDK.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Fil \_ data.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Veraltete Schnittstellen](deprecated-interfaces.md)
</dt> </dl>

 

 
