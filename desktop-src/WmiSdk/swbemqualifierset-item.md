---
description: Die Item-Methode des SWbemQualifierSet-Objekts gibt ein benanntes SWbemQualifier-Objekt aus der Auflistung zurück. Dies ist die Standardmethode dieses -Objekts.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: SWbemQualifierSet.Item-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Item
- ISWbemQualifierSet.Item
- ISWbemQualifierSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 99b735f52ac4d311af6e35f7e214322c55345e4c029e73a342baa52dfa72de6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312991"
---
# <a name="swbemqualifiersetitem-method"></a>SWbemQualifierSet.Item-Methode

Die **Item-Methode** des [**SWbemQualifierSet-Objekts**](swbemqualifierset.md) gibt ein benanntes [**SWbemQualifier-Objekt**](swbemqualifier.md) aus der Auflistung zurück. Dies ist die Standardmethode dieses -Objekts.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strName* \[ In\]
</dt> <dd>

Erforderlich. Name des abzurufende Qualifizierers.

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Der Standardwert ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg wird das angeforderte [**SWbemQualifier-Objekt**](swbemqualifier.md) zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Item-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Der *iFlags-Parameter* war ungültig.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Der angegebene Qualifizierer ist nicht vorhanden.

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

[**SWbemQualifier**](swbemqualifier.md)
</dt> </dl>

 

 




