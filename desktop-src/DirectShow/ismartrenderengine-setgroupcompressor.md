---
description: Gibt einen Komprimierungs Filter an, der beim Rendern der angegebenen Gruppe verwendet werden soll.
ms.assetid: ba717cac-c5a8-4821-a5f0-dd9d5fe4834e
title: 'Ismartrenderengine:: setgroupcompressor-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.SetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cb02a9d8daf7e6ba74a45299daa9d45ab63d5db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367139"
---
# <a name="ismartrenderenginesetgroupcompressor-method"></a>Ismartrenderengine:: setgroupcompressor-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Gibt einen Komprimierungs Filter an, der beim Rendern der angegebenen Gruppe verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetGroupCompressor(
   long        Group,
   IBaseFilter *pCompressor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gruppieren* 
</dt> <dd>

Der null basierte Index der Gruppe.

</dd> <dt>

*pkompressor* 
</dt> <dd>

Ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Komprimierungs Filters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ismartrenderengine-Schnittstelle**](ismartrenderengine.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




