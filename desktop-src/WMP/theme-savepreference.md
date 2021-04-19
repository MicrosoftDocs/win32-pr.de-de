---
title: Design. savepreference
description: Die savepreference-Methode speichert eine bevorzugte Einstellung in der Registrierung.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- Design. savepreference-Fenster Media Player
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89633d71dd75f4ef5e804aefddc85cf00ad5c03b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373929"
---
# <a name="themesavepreference"></a>Design. savepreference

Die **savepreference** -Methode speichert eine bevorzugte Einstellung in der Registrierung.

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*der Schlüssel*
</dt> <dd>

Eine **Zeichenfolge** , die den Schlüssel des zu speichernden Einstellungs Werts angibt.

</dd> <dt>

<span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*Parallelitätstyp*
</dt> <dd>

Eine **Zeichenfolge** , die den zu speichernden Wert angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Bevorzugung ist ein Schlüssel-Wert-Paar, das in der Registrierung gespeichert werden kann, um Informationen über den Status der Windows-Media Player zwischen den Ausführungen zu erhalten. Diese Funktion kann z. b. verwendet werden, um Anpassungs Einstellungen zu speichern, sodass Sie nicht jedes Mal neu eingegeben werden müssen, wenn Windows Media Player gestartet wird.

Die Einstellungen werden nicht verschlüsselt und sind daher keine sichere Methode zum Speichern von Daten. Verwenden Sie keine Einstellungen, um private Daten zu speichern.

## <a name="examples"></a>Beispiele


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Design-Element**](theme-element.md)
</dt> <dt>

[**Design. loadpreference**](theme-loadpreference.md)
</dt> </dl>

 

 





