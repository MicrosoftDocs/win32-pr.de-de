---
description: Die Item-Methode des SWbemMethodSet-Objekts gibt ein benanntes SWbemMethod-Objekt aus der Auflistung zurück.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: SWbemMethodSet.Item-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fd78277be4611507a7f7a488dae0d4edda832afeac8c4a947d4c56277d9af397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679450"
---
# <a name="swbemmethodsetitem-method"></a>SWbemMethodSet.Item-Methode

Die **Item-Methode** des [**SWbemMethodSet-Objekts**](swbemmethodset.md) gibt ein benanntes [**SWbemMethod-Objekt**](swbemmethod.md) aus der Auflistung zurück.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strName* \[ In\]
</dt> <dd>

Erforderlich. Name der abzurufende Methode.

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Der Standardwert ist 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt das angeforderte [**SWbemMethod-Objekt**](swbemmethod.md) zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Item-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Der *iFlags-Parameter* war ungültig.

</dd> <dt>

**wbemErrFailed** – 2147749894
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Die angegebene Methode ist nicht vorhanden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethodSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemMethodSet<br/>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemMethodSet**](swbemmethodset.md)
</dt> <dt>

[**SWbemMethod**](swbemmethod.md)
</dt> </dl>

 

 




