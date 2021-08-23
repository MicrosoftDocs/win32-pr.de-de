---
description: Die Remove-Methode des SWbemNamedValueSet-Objekts löscht einen benannten Wert aus dem Kontext.
ms.assetid: 8cb353fb-c6d7-41d9-a2d0-ff1ad37264e4
ms.tgt_platform: multiple
title: SWbemNamedValueSet.Remove-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
- ISWbemNamedValueSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1c733f932588c5c0d7ccfe3c906f28244d37fee0c649451c05fb8f72742edef4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611920"
---
# <a name="swbemnamedvaluesetremove-method"></a>SWbemNamedValueSet.Remove-Methode

Die **Remove-Methode** des [**SWbemNamedValueSet-Objekts**](swbemnamedvalueset.md) löscht einen benannten Wert aus dem Kontext.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemNamedValueSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strName* \[ In\]
</dt> <dd>

Erforderlich. Name des zu entfernenden Werts.

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Dieser Wert muss 0 (null) sein, wenn angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Remove-Methode** kann **das Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Ein ungültiger Parameter wurde angegeben, oder der Namespace konnte nicht analysiert werden.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Das angeforderte Element wurde nicht gefunden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemNamedValueSet<br/>                                                    |
| IID<br/>                      | IID \_ ISWbemNamedValueSet<br/>                                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> </dl>

 

 




