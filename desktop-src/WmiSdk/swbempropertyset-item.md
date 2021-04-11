---
description: Die Item-Methode des Objekts "Swap PropertySet" Ruft eine benannte "taubemproperty" aus der Auflistung ab. Dies ist die Standardmethode für dieses Objekt.
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: "' Swap PropertySet. Item '-Methode (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Item
- ISWbemPropertySet.Item
- ISWbemPropertySet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d4dcbbbcb8b5225af038bf71e67c3a14260942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218292"
---
# <a name="swbempropertysetitem-method"></a>Taubempropertyset. Item-Methode

Die **Item** -Methode des Objekts " [**Swap PropertySet**](swbempropertyset.md) " Ruft eine benannte " [**taubemproperty**](swbemproperty.md) " aus der Auflistung ab. Dies ist die Standardmethode für dieses Objekt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *Name* \[ " in\]
</dt> <dd>

Erforderlich. Der Name der abzurufenden Eigenschaft.

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Dieser Wert muss NULL sein, wenn angegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung wird das angeforderte " [**Swap Property**](swbemproperty.md) "-Objekt zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **Element** Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Nicht spezifizierter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben.

</dd> <dt>

**wbemErrOutOfMemory** -2147749896
</dt> <dd>

Nicht genügend Arbeitsspeicher für die Ausführung dieser Methode.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Eigenschaften Satz<br/>                                                      |
| IID<br/>                      | IID \_ iswbempropertyset<br/>                                                       |



 

 




