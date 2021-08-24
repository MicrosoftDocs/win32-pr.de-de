---
description: Die Add-Methode des SWbemNamedValueSet-Objekts fügt der Auflistung ein SWbemNamedValue-Objekt hinzu. Wenn ein Element bereits in der Auflistung mit dem gleichen Namen vorhanden ist, ersetzt das neue Element es.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: SWbemNamedValueSet.Add-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a7a911dcfa6371421fd4033524400d0c818e814d3bd52f90b677ac7c9fcf1b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612120"
---
# <a name="swbemnamedvaluesetadd-method"></a>SWbemNamedValueSet.Add-Methode

Die **Add-Methode** des [**SWbemNamedValueSet-Objekts**](swbemnamedvalueset.md) fügt der Auflistung ein [**SWbemNamedValue-Objekt**](swbemnamedvalue.md) hinzu. Wenn ein Element bereits in der Auflistung mit dem gleichen Namen vorhanden ist, ersetzt das neue Element es.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strName* \[ In\]
</dt> <dd>

Erforderlich. Name des neuen Werts.

</dd> <dt>

*varVal* \[ In\]
</dt> <dd>

Erforderlich. Variante, die den neuen Wert darstellt.

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Reserviert und müssen bei Angabe auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Methode das neu geänderte oder neu erstellte [**SWbemNamedValue-Objekt**](swbemnamedvalue.md) zurück.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemNamedValueSet**](swbemnamedvalueset.md)
</dt> </dl>

 

 




