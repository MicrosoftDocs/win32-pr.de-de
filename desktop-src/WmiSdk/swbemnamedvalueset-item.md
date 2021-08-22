---
description: Die Item-Methode des SWbemNamedValueSet-Objekts ruft ein SWbemNamedValue-Objekt aus der Auflistung ab.
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: SWbemNamedValueSet.Item-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
- ISWbemNamedValueSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 688c78aa644b7a5eab3fd6be9ae806ec254a7a50647dc9e87539e96049d6df04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992080"
---
# <a name="swbemnamedvaluesetitem-method"></a>SWbemNamedValueSet.Item-Methode

Die **Item-Methode** des [**SWbemNamedValueSet-Objekts**](swbemnamedvalueset.md) ruft ein [**SWbemNamedValue-Objekt**](swbemnamedvalue.md) aus der Auflistung ab.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strName* \[ In\]
</dt> <dd>

Erforderlich. Name des abzurufende Werts.

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Dieser Wert muss 0 (null) sein, wenn er angegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird das [**angeforderte SWbemNamedValue-Objekt**](swbemnamedvalue.md) zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Item-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Ein ungültiger Parameter wurde angegeben, oder der Namespace konnte nicht analysiert werden.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Das angeforderte Element wurde nicht gefunden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beispiele zum Hinzufügen und Abrufen benannter Werte finden Sie unter [**SWbemNamedValue.Value.**](swbemnamedvalue-value.md)

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

 

 




