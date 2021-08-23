---
description: Die Remove-Methode des SWbemPrivilegeSet-Objekts löscht eine Berechtigung aus der Auflistung.
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.tgt_platform: multiple
title: SWbemPrivilegeSet.Remove-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 825fbdc18537fa73561f8a662ecc0388ab18be0b9bf26ca2cbfeadd7bfb9b469
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732290"
---
# <a name="swbemprivilegesetremove-method"></a>SWbemPrivilegeSet.Remove-Methode

Die **Remove-Methode** des [**SWbemPrivilegeSet-Objekts**](swbemprivilegeset.md) löscht eine Berechtigung aus der Auflistung.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
SWbemPrivilegeSet.Remove( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iPrivilege* 
</dt> <dd>

Erforderlich. Dies ist eine der WMI-Konstanten aus der [**WbemPrivilegeEnum-Gruppe.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) Diese Konstanten sind im Wesentlichen ganze Zahlen, die bestimmte Berechtigungen darstellen. Um beispielsweise die Berechtigung zu entfernen, mit der Sie ein Windows System herunterfahren können, verwenden Sie die **Konstante wbemPrivilegeShutdown** oder die numerische Entsprechung von 0x17.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Remove-Methode** kann das **Err-Objekt** einen der Fehlercodes in der folgenden Liste enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Die angegebene Berechtigung ist nicht vorhanden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md)
</dt> </dl>

 

 




