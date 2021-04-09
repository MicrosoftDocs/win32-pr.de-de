---
description: Die Item-Methode des-Objekts von "taubemqualifierset" gibt ein benanntes "Swap"-Objekt aus der Auflistung zurück. Dies ist die Standardmethode dieses Objekts.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: Taubemqualifierset. Item-Methode (wbemdisp. h)
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
ms.openlocfilehash: 9c89ff554b049e6730a64ebf7e5f017fc8a5652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868572"
---
# <a name="swbemqualifiersetitem-method"></a>Taubemqualifierset. Item-Methode

Die **Item** -Methode des-Objekts von " [**taubemqualifierset**](swbemqualifierset.md) " gibt ein benanntes " [**Swap**](swbemqualifier.md) "-Objekt aus der Auflistung zurück. Dies ist die Standardmethode dieses Objekts.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *Name* \[ " in\]
</dt> <dd>

Erforderlich. Der Name des abzurufenden Qualifizierers.

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Der Standardwert ist 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, wird das angeforderte [**Austausch qualifizierungsobjekt**](swbemqualifier.md) zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Element** Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Der *IFlags* -Parameter war ungültig.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Der angegebene Qualifizierer ist nicht vorhanden.

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

[**Austausch Qualifizierer**](swbemqualifier.md)
</dt> </dl>

 

 




