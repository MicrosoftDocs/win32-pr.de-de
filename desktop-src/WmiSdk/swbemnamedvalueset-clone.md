---
description: Die Clone-Methode des Swap-namedvalueset-Objekts gibt ein neues-Objekt zurück, das ein Klon der aktuellen Auflistung ist.
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: Swap-namedvalueset. Clone-Methode (wbemdisp. h)
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
ms.openlocfilehash: 17678d36a553c84c008f606c647d7ff1fa9dfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756973"
---
# <a name="swbemnamedvaluesetclone-method"></a>Swap-namedvalueset. Clone-Methode

Die **Clone** -Methode des [**Swap-namedvalueset**](swbemnamedvalueset.md) -Objekts gibt ein neues-Objekt zurück, das ein Klon der aktuellen Auflistung ist.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt ein neues Objekt vom [**metadatennamedvalueset**](swbemnamedvalueset.md) zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Klon** Methode kann das **Err** -Objekt einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher zum Klonen des Objekts.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um eine Sammlung von " [**Swap namedvalueset**](swbemnamedvalueset.md) " zu duplizieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-namedvalueset<br/>                                                    |
| IID<br/>                      | IID \_ iswbemnamedvalueset<br/>                                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Austausch Elementname**](swbemnamedvalueset.md)
</dt> </dl>

 

 




