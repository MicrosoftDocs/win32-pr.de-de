---
description: Die Remove-Methode des SWbemQualifierSet-Objekts löscht einen benannten Qualifizierer aus der Auflistung.
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: SWbemQualifierSet.Remove-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f4ca62276e39822964d33b58345b4718354bfd63039ec42ab30ac5daf95f6e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463610"
---
# <a name="swbemqualifiersetremove-method"></a>SWbemQualifierSet.Remove-Methode

Die **Remove-Methode** des [**SWbemQualifierSet-Objekts**](swbemqualifierset.md) löscht einen benannten Qualifizierer aus der Auflistung.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strName* \[ In\]
</dt> <dd>

Erforderlich. Name des zu entfernenden Qualifizierers.

</dd> <dt>

*iFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Der Standardwert ist 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Remove-Methode** kann **das Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

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

</dd> <dt>

**wbemErrInvalidOperation** – 2147749910 (0x80041016)
</dt> <dd>

Das Entfernen dieses Qualifizierers ist unzulässig.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können beim Entfernen von Elementen keine Auflistung iterieren, da der Auflistungszeiger zum nächsten Element verschoben wird, wenn Sie ein Element aus einer Auflistung entfernen. Weitere Informationen finden Sie unter [Zugreifen auf eine Auflistung.](accessing-a-collection.md)

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

[**SWbemQualifierSet.Add**](swbemqualifierset-add.md)
</dt> </dl>

 

 




