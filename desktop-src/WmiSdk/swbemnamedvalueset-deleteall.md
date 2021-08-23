---
description: Die DeleteAll-Methode des SWbemNamedValueSet-Objekts entfernt alle benannten Werte aus der Auflistung und leert sie daher.
ms.assetid: db5d2e68-028e-4902-ad42-0b46e1a96bcb
ms.tgt_platform: multiple
title: SWbemNamedValueSet.DeleteAll-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b6878494c31823b1c081a69b4d58b3a802cf820dd10bbcb20f14ed7087bb84c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612070"
---
# <a name="swbemnamedvaluesetdeleteall-method"></a>SWbemNamedValueSet.DeleteAll-Methode

Die **DeleteAll-Methode** des [**SWbemNamedValueSet-Objekts**](swbemnamedvalueset.md) entfernt alle benannten Werte aus der Auflistung und leert sie daher.

## <a name="syntax"></a>Syntax


```VB
SWbemNamedValueSet.DeleteAll()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **DeleteAll-Methode** kann das **Err-Objekt** den folgenden Fehlercode enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

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
</dt> <dt>

[**SWbemNamedValueSet.Remove**](swbemnamedvalueset-remove.md)
</dt> </dl>

 

 




