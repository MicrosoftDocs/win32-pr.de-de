---
description: Die Add-Methode des SWbemQualifierSet-Objekts fügt der SWbemQualifierSet-Auflistung ein SWbemQualifier-Objekt hinzu. Wenn ein Qualifizierer mit dem gleichen Namen bereits in der Auflistung vorhanden ist, wird er ersetzt.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: SWbemQualifierSet.Add-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 64a85e10614595d9dd6492d3f4b412f1d89432c0188801ea60a09e294846297b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897780"
---
# <a name="swbemqualifiersetadd-method"></a>SWbemQualifierSet.Add-Methode

Die **Add-Methode** des [**SWbemQualifierSet-Objekts**](swbemqualifierset.md) fügt der **SWbemQualifierSet-Auflistung ein SWbemQualifier-Objekt** hinzu. [](swbemqualifier.md) Wenn ein Qualifizierer mit dem gleichen Namen bereits in der Auflistung vorhanden ist, wird er ersetzt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strName* \[ In\]
</dt> <dd>

Erforderlich. Name des neuen Qualifizierers.

</dd> <dt>

*varVal* \[ In\]
</dt> <dd>

Erforderlich. Variant-Wert des neuen Qualifizierers.

</dd> <dt>

*bPropagatesToSubclasses* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob dieser neue Qualifizierer an Unterklassen weitergegeben wird. Der Standardwert ist **TRUE.**

</dd> <dt>

*bPropagatesToInstances* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob dieser neue Qualifizierer an Instanzen weitergegeben wird. Der Standardwert ist **TRUE.**

</dd> <dt>

*bOverridable* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob dieser Qualifizierer überschrieben werden kann, wenn er weitergegeben wird. Der Standardwert ist **TRUE.**

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Der Standardwert ist 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Methode ein [**SWbemQualifier-Objekt**](swbemqualifier.md) zurück, das den neuen Qualifizierer darstellt. Andernfalls wird ein **NULL-Objekt** zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Add-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Der *iFlags-Parameter* war ungültig.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrCannotBeKey** – 2147749919 (0x8004101F)
</dt> <dd>

Es wurde ein unzulässiger Versuch unternommen, einen **Schlüsselqualifizierer** für eine Eigenschaft anzugeben, die kein Schlüssel sein kann. Die Schlüssel sind in der Klassendefinition für ein Objekt angegeben und können nicht für jede Instanz einzeln geändert werden.

</dd> <dt>

**wbemErrInvalidQualifierType** – 2147749929 (0x80041029)
</dt> <dd>

Der *varVal-Parameter* ist kein zulässiger Qualifizierertyp.

</dd> <dt>

**wbemErrOverrideNotAllowed** – 2147749914 (0x8004101A)
</dt> <dd>

Es ist nicht möglich, den **SWbemQualifierSet.Add-Vorgang** für diesen Qualifizierer auszuführen, da das besitzende Objekt keine Außerkraftsetzungen zulässt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemQualifierSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemQualifierSet<br/>                                                      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SWbemQualifierSet**](swbemqualifierset.md)
</dt> <dt>

[**SWbemQualifierSet.Remove**](swbemqualifierset-remove.md)
</dt> </dl>

 

 




