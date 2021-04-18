---
description: Die Item-Methode des Objekts "Swap-methodset" gibt ein benanntes "taubemmethod"-Objekt aus der Auflistung zurück.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: Swap. Item-Methode (wbemdisp. h)
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
ms.openlocfilehash: 89d20dc652189abe3354f5d1b51c03279d3f74c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347313"
---
# <a name="swbemmethodsetitem-method"></a>Taubemmethodset. Item-Methode

Die **Item** -Methode des Objekts " [**Swap-methodset**](swbemmethodset.md) " gibt ein benanntes " [**taubemmethod**](swbemmethod.md) "-Objekt aus der Auflistung zurück.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *Name* \[ " in\]
</dt> <dd>

Erforderlich. Der Name der abzurufenden Methode.

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Der Standardwert ist 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt das angeforderte " [**Swap Method**](swbemmethod.md) "-Objekt zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Element** Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Der *IFlags* -Parameter war ungültig.

</dd> <dt>

**wbemErrFailed** -2147749894
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Die angegebene Methode ist nicht vorhanden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Methode<br/>                                                        |
| IID<br/>                      | IID \_ iswbemmethodset<br/>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swap-methodset**](swbemmethodset.md)
</dt> <dt>

[**Swap-Methode**](swbemmethod.md)
</dt> </dl>

 

 




