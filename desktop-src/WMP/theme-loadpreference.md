---
title: Design. loadpreference
description: Die loadpreference-Methode lädt eine bevorzugte Einstellung aus der Registrierung.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- Design. loadpreference-Windows-Media Player
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365436"
---
# <a name="themeloadpreference"></a>Design. loadpreference

Die **loadpreference** -Methode lädt eine bevorzugte Einstellung aus der Registrierung.

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*der Schlüssel*
</dt> <dd>

Eine **Zeichenfolge** , die den Schlüssel des zu ladenden Einstellungs Werts angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück.

## <a name="remarks"></a>Bemerkungen

Eine Bevorzugung ist ein Schlüssel-Wert-Paar, das in der Registrierung gespeichert werden kann, um Informationen über den Status der Windows-Media Player zwischen den Ausführungen zu erhalten. Diese Funktion kann z. b. verwendet werden, um Anpassungs Einstellungen zu speichern, sodass Sie nicht jedes Mal neu eingegeben werden müssen, wenn Windows Media Player gestartet wird.

Die Einstellungen werden nicht verschlüsselt und sind daher keine sichere Methode zum Speichern von Daten. Verwenden Sie keine Einstellungen, um private Daten zu speichern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Design-Element**](theme-element.md)
</dt> <dt>

[**Design. savepreference**](theme-savepreference.md)
</dt> </dl>

 

 





