---
description: Die Item-Methode des "Swap Name"-Objekts Ruft ein "taubemnamedvalue"-Objekt aus der Auflistung ab.
ms.assetid: ccebe65e-6032-43d5-9004-2247c3b96d6d
ms.tgt_platform: multiple
title: Swap-namedvalueset. Item-Methode (wbemdisp. h)
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
ms.openlocfilehash: a4932409fa7b8ac9e0f326e5de7e8ecf0f89c2b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528478"
---
# <a name="swbemnamedvaluesetitem-method"></a>Swap-namedvalueset. Item-Methode

Die **Item** -Methode des " [**Swap Name**](swbemnamedvalueset.md) "-Objekts Ruft ein " [**taubemnamedvalue**](swbemnamedvalue.md) "-Objekt aus der Auflistung ab.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objNamedValue = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *Name* \[ " in\]
</dt> <dd>

Erforderlich. Der Name des abzurufenden Werts.

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Dieser Wert muss NULL sein, wenn angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, wird das angeforderte " [**Swap Name**](swbemnamedvalue.md) "-Objekt zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Element** Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben, oder der Namespace konnte nicht analysiert werden.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Das angeforderte Element wurde nicht gefunden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beispiele zum Hinzufügen und Abrufen benannter [**Werte finden Sie**](swbemnamedvalue-value.md)unter "".

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

 

 




