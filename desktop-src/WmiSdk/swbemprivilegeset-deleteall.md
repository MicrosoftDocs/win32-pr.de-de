---
description: Mit der DeleteAll-Methode des Objekts "pulbemprivilegeset" werden alle Berechtigungen aus der Auflistung entfernt und somit geleert.
ms.assetid: 368caa14-1c53-4090-8569-97ea743905de
ms.tgt_platform: multiple
title: Taubemprivilegeset. DeleteAll-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 382382b0c22c029f41c9ab33fb959287e5222d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352504"
---
# <a name="swbemprivilegesetdeleteall-method"></a>Taubemprivilegeset. DeleteAll-Methode

Mit der **DeleteAll** -Methode des Objekts " [**pulbemprivilegeset**](swbemprivilegeset.md) " werden alle Berechtigungen aus der Auflistung entfernt und somit geleert.

## <a name="syntax"></a>Syntax


```VB
SWbemPrivilegeSet.DeleteAll()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **DeleteAll** -Methode kann das **Err** -Objekt den folgenden Fehlercode enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-taubemprivilegeset<br/>                                                     |
| IID<br/>                      | IID \_ iswbemprivilegeset<br/>                                                      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swap-Privileg**](swbemprivilegeset.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge](executing-privileged-operations.md)
</dt> <dt>

[**"Swap-privilegeset. Remove"**](swbemprivilegeset-remove.md)
</dt> </dl>

 

 




