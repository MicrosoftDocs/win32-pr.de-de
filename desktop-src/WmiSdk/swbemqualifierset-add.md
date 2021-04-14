---
description: Die Add-Methode des-Objekts von "Swap. Set" fügt der Auflistung von "taubemqualifierset" ein "taubemqualifier"-Objekt hinzu. Wenn ein Qualifizierer mit dem gleichen Namen bereits in der Auflistung vorhanden ist, wird er ersetzt.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Taubemqualifierset. Add-Methode (wbemdisp. h)
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
ms.openlocfilehash: bbbef15ccc45aeba5b7e3c03f6cb9448cfe03ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349199"
---
# <a name="swbemqualifiersetadd-method"></a>Taubemqualifierset. Add-Methode

Die **Add** -Methode des-Objekts von " [**Swap. set**](swbemqualifierset.md) " fügt der Auflistung von "taubemqualifierset" ein "  [**taubemqualifier**](swbemqualifier.md) "-Objekt hinzu. Wenn ein Qualifizierer mit dem gleichen Namen bereits in der Auflistung vorhanden ist, wird er ersetzt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

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

" *Name* \[ " in\]
</dt> <dd>

Erforderlich. Der Name des neuen Qualifizierers.

</dd> <dt>

*varval* \[ in\]
</dt> <dd>

Erforderlich. Der Variant-Wert des neuen Qualifizierers.

</dd> <dt>

*bpropagatestosubclasses* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob dieser neue Qualifizierer an Unterklassen weitergegeben wird. Der Standardwert ist " **true**".

</dd> <dt>

*bpropagatestoinstance* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob dieser neue Qualifizierer an-Instanzen weitergegeben wird. Der Standardwert ist " **true**".

</dd> <dt>

*boverridable* \[ in, optional\]
</dt> <dd>

Boolescher Wert, der angibt, ob dieser Qualifizierer bei der Weitergabe überschrieben werden kann. Der Standardwert ist " **true**".

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Der Standardwert ist 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt diese [**Methode ein-**](swbemqualifier.md) Objekt zurück, das den neuen Qualifizierer darstellt. Andernfalls wird ein **null** -Objekt zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Add** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Der *IFlags* -Parameter war ungültig.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrCannotBeKey** -2147749919 (0x8004101f)
</dt> <dd>

Es wurde ein unzulässiger Versuch unternommen, einen **Schlüssel** Qualifizierer für eine Eigenschaft anzugeben, die kein Schlüssel sein kann. Die Schlüssel sind in der Klassendefinition für ein Objekt angegeben und können nicht für jede Instanz einzeln geändert werden.

</dd> <dt>

**wbemErrInvalidQualifierType** -2147749929 (0x80041029)
</dt> <dd>

Der *varval* -Parameter ist kein gültiger qualifizierungstyp.

</dd> <dt>

**wbemErrOverrideNotAllowed** -2147749914 (0x8004101a)
</dt> <dd>

Es ist nicht möglich, den Vorgang " **taubemqualifierset. Add** " für diesen Qualifizierer auszuführen, da das besitzende Objekt keine über schreibungen zulässt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Gruppe<br/>                                                     |
| IID<br/>                      | IID \_ iswbemqualifierset<br/>                                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swap-qualifierset**](swbemqualifierset.md)
</dt> <dt>

[**Swap-qualifierset. Remove**](swbemqualifierset-remove.md)
</dt> </dl>

 

 




