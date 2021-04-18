---
description: Die Clone- \_ Methode des-Objekts von "taubemlasterror" gibt ein neues-Objekt zurück, das ein Klon des aktuellen "taubemlasterror"-Objekts ist.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: SWbemLastError.Clone_-Methode (wbemdisp. h)
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
ms.openlocfilehash: 7d4d43f73ab42021235db39adba0a77bc783b97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358583"
---
# <a name="swbemlasterrorclone_-method"></a>Methode ' Swap. Clone ' \_

Die **Clone \_** -Methode des-Objekts von " [**taubemlasterror**](swbemlasterror.md) " gibt ein neues-Objekt zurück, das ein Klon des aktuellen " **taubemlasterror** "-Objekts ist.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die **Klon \_** Methode erfolgreich ist, gibt Sie ein neues-Objekt mit dem Wert " [**taubemlasterror**](swbemlasterror.md) " zurück.

## <a name="error-codes"></a>Fehlercodes

Nach dem Abschluss der **Klon \_** Methode kann das **Err** -Objekt einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Ein angegebener Parameter ist ungültig.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie **die \_ Clone** -Methode, um eine Klassendefinition oder-Instanz zu duplizieren. Diese Methode ist nützlich, wenn Sie die ursprüngliche Kopie des Objekts sichern müssen, während Sie eine neue Kopie ändern. Verwenden Sie diese Methode auch, um viele neue Instanzen aus einer einzelnen Quell Instanz zu erstellen. Verwenden Sie z [**. b. "errbeapbject. \_ SpawnInstance**](swbemobject-spawninstance-.md) ", um eine einzelne Start Instanz zu erstellen, und verwenden Sie " **taubemlasterror. Clone \_** ", um 100 Kopien der Instanz schnell zu erstellen. Anschließend können Sie die Objekte ändern und jedem Objekt bestimmte Werte erteilen.

Es ist nicht möglich, diese Methode zu verwenden, um eine Klassendefinition in eine-Instanz zu konvertieren oder um eine Instanz in eine Klassendefinition zu konvertieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Fehler<br/>                                                        |
| IID<br/>                      | IID \_ iswbemlasterror<br/>                                                         |



 

 




