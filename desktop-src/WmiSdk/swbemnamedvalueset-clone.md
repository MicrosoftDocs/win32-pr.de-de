---
description: Die Clone-Methode des SWbemNamedValueSet-Objekts gibt ein neues -Objekt zurück, das ein Klon der aktuellen Auflistung ist.
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: SWbemNamedValueSet.Clone-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9158901a39fa80e49404912ee5458c416069bbe354e19059ef4622ae4257fda9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314191"
---
# <a name="swbemnamedvaluesetclone-method"></a>SWbemNamedValueSet.Clone-Methode

Die **Clone-Methode** des [**SWbemNamedValueSet-Objekts**](swbemnamedvalueset.md) gibt ein neues -Objekt zurück, das ein Klon der aktuellen Auflistung ist.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird ein neues [**SWbemNamedValueSet-Objekt**](swbemnamedvalueset.md) zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Clone-Methode** kann das **Err-Objekt** einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher zum Klonen des Objekts.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um eine [**SWbemNamedValueSet-Auflistung**](swbemnamedvalueset.md) zu duplizieren.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> </dl>

 

 




