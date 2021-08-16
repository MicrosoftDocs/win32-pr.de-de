---
description: Die \_ Clone-Methode des SWbemLastError-Objekts gibt ein neues -Objekt zurück, das ein Klon des aktuellen SWbemLastError-Objekts ist.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: SWbemLastError.Clone_-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 162944eeb4ee7ca0c72102b704e9f75851bbfb41885e6b79e86d1a438487473f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314666"
---
# <a name="swbemlasterrorclone_-method"></a>SWbemLastError.Clone-Methode \_

Die **\_ Clone-Methode** des [**SWbemLastError-Objekts**](swbemlasterror.md) gibt ein neues -Objekt zurück, das ein Klon des aktuellen **SWbemLastError-Objekts** ist.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die **Clone-Methode \_** erfolgreich ist, wird ein neues [**SWbemLastError-Objekt**](swbemlasterror.md) zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **\_ Clone-Methode** kann das **Err-Objekt** einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie die **\_ Clone-Methode,** um eine Klassendefinition oder -instanz zu duplizieren. Diese Methode ist nützlich, wenn Sie die ursprüngliche Kopie des Objekts sichern müssen, während Sie eine neue Kopie ändern. Verwenden Sie diese Methode auch, um viele neue Instanzen aus einer einzelnen Quellinstanz zu erstellen. Verwenden Sie beispielsweise [**SWbemObject.SpawnInstance, \_**](swbemobject-spawninstance-.md) um eine einzelne Startinstanz zu erstellen, und verwenden **Sie SWbemLastError.Clone, \_** um schnell 100 Kopien der Instanz zu erstellen. Anschließend können Sie die Objekte ändern und jedem Objekt bestimmte Werte geben.

Es ist nicht möglich, diese Methode zum Konvertieren einer Klassendefinition in eine Instanz oder zum Konvertieren einer Instanz in eine Klassendefinition zu verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




