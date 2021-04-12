---
description: Die Remove-Methode des-Objekts aus der-Auflistung löscht einen benannten Qualifizierer.
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: Taubemqualifierset. Remove-Methode (wbemdisp. h)
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
ms.openlocfilehash: 39c95f268328bc0cad3f3c0874b633fc36c4f5b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528472"
---
# <a name="swbemqualifiersetremove-method"></a>Taubemqualifierset. Remove-Methode

Die **Remove** -Methode des [**-Objekts aus der-**](swbemqualifierset.md) Auflistung löscht einen benannten Qualifizierer.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

" *Name* \[ " in\]
</dt> <dd>

Erforderlich. Der Name des zu entfernenden Qualifizierers.

</dd> <dt>

*IFlags* \[ in, optional\]
</dt> <dd>

Reserviert. Der Standardwert ist 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Remove** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.

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

</dd> <dt>

**wbemErrInvalidOperation** -2147749910 (0x80041016)
</dt> <dd>

Das Entfernen dieses Qualifizierers ist unzulässig.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beim Entfernen von Elementen ist es nicht möglich, eine Auflistung zu durchlaufen, denn wenn Sie ein Element aus einer Auflistung entfernen, wird der Auflistungs Zeiger zum nächsten Element verschoben. Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).

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

[**Austauschen von "austauschen. hinzufügen"**](swbemqualifierset-add.md)
</dt> </dl>

 

 




