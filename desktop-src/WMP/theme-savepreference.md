---
title: THEME.savePreference
description: Die savePreference-Methode speichert eine Einstellung in der Registrierung.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- THEME.savePreference-Windows Media Player
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d5f9edca154ff6402028ba873c1643e330ab316a54a63f14fa4f9b5bdb244483
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134543"
---
# <a name="themesavepreference"></a>THEME.savePreference

Die **savePreference-Methode** speichert eine Einstellung in der Registrierung.

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

Eine **Zeichenfolge,** die den Schlüssel des zu speichernden Einstellungswerts angibt.

</dd> <dt>

<span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*theValue*
</dt> <dd>

Eine **Zeichenfolge,** die den zu speichernden Wert angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Eine Einstellung ist ein Schlüssel-Wert-Paar, das in der Registrierung gespeichert werden kann, um Informationen über den Zustand der Windows Media Player zwischen den Windows Media Player beibehalten. Dieses Feature kann beispielsweise verwendet werden, um Anpassungseinstellungen zu speichern, damit sie nicht jedes Mal erneut eingegeben werden müssen, wenn Windows Media Player wird.

Einstellungen werden nicht verschlüsselt und sind daher keine sichere Methode zum Speichern von Daten. Verwenden Sie keine Einstellungen zum Speichern privater Daten.

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
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**THEME-Element**](theme-element.md)
</dt> <dt>

[**THEME.loadPreference**](theme-loadpreference.md)
</dt> </dl>

 

 





