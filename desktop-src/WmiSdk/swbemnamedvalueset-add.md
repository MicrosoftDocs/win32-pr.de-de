---
description: Die Add-Methode des-Objekts "Swap Name" fügt der-Auflistung ein "-Objekt"-Objekt hinzu. Wenn ein Element bereits in der Auflistung mit dem gleichen Namen vorhanden ist, wird es durch das neue Element ersetzt.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: "' Taubemnamedvalueset. Add '-Methode (wbemdisp. h)"
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
ms.openlocfilehash: 3aa1a3a982d7621c910a5afca95b26db1dd5f4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528481"
---
# <a name="swbemnamedvaluesetadd-method"></a>Methode ' Swap-namedvalueset. Add '

Die **Add** -Methode des-Objekts " [**Swap Name**](swbemnamedvalueset.md) " fügt der-Auflistung [**ein "**](swbemnamedvalue.md) -Objekt"-Objekt hinzu. Wenn ein Element bereits in der Auflistung mit dem gleichen Namen vorhanden ist, wird es durch das neue Element ersetzt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

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

" *Name* \[ " in\]
</dt> <dd>

Erforderlich. Der Name des neuen Werts.

</dd> <dt>

*varval* \[ in\]
</dt> <dd>

Erforderlich. Variant, der den neuen Wert darstellt.

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reserviert und muss auf 0 (null) festgelegt werden, wenn angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, gibt diese Methode das neu geänderte oder neu erstellte " [**Swap Name**](swbemnamedvalue.md) "-Objekt zurück.

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

 

 




