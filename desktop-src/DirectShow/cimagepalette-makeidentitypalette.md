---
description: Die MakeIdentityPalette-Methode versucht, eine &\# 0034;Identitätspalette,&\# 0034; zu erstellen, die direkt der im Anzeigegerät ausgewählten Palette zugeordnet ist.
ms.assetid: 08a0cf67-f43f-44c0-bfb3-6527fd434ea4
title: CImagePalette.MakeIdentityPalette-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakeIdentityPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb6e9a4e2c6adc411b7b043e35dc6dacf45dbb6a6ee4cf326a1c1953c559c16f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916130"
---
# <a name="cimagepalettemakeidentitypalette-method"></a>CImagePalette.MakeIdentityPalette-Methode

Die `MakeIdentityPalette` -Methode versucht, eine "Identitätspalette" zu erstellen, die als eine definiert ist, die direkt der im Anzeigegerät ausgewählten Palette zugeordnet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT MakeIdentityPalette(
   PALETTEENTRY *pEntry,
   INT          iColours,
   LPSTR        szDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pEntry* 
</dt> <dd>

Zeiger auf ein Array von Paletteneinträgen.

</dd> <dt>

*iColours* 
</dt> <dd>

Anzahl der Paletteneinträge in *pEntry*.

</dd> <dt>

*szDevice* 
</dt> <dd>

Zeiger auf eine Zeichenfolge, die den Namen des Anzeigegeräts enthält, wie von der **GDI-Funktion EnumDisplayDevices** zurückgegeben. Um das Hauptanzeigegerät zu verwenden, legen Sie diesen Parameter auf **NULL** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg S \_ OK oder bei Erfolg S FALSE \_ zurück.

## <a name="remarks"></a>Hinweise

Diese Methode vergleicht die reservierten Einträge in der Systempalette mit den entsprechenden Einträgen im *pEntry-Array.* Wenn sie genau übereinstimmen, legt die -Methode das \_ PC-NOCOLLAPSE-Flag in den verbleibenden (nicht reservierten) Paletteneinträgen in *pEntry fest.* Dieses Flag verhindert, dass GDI versucht, Einträge der logischen Palette zu Systempaletteneinträgen zuzuordnen.

Die [**CImagePalette::MakePalette-Methode**](cimagepalette-makepalette.md) ruft diese Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CImagePalette-Klasse**](cimagepalette.md)
</dt> </dl>

 

 




