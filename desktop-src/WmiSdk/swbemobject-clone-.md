---
description: Die Clone- \_ Methode des "errbemubject"-Objekts gibt ein neues-Objekt zurück, das ein Klon des aktuellen-Objekts ist.
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: SWbemObject.Clone_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050344"
---
# <a name="swbemobjectclone_-method"></a>Errbemubject. Clone- \_ Methode

Die **Clone \_** -Methode des " [**errbemubject**](swbemobject.md) "-Objekts gibt ein neues-Objekt zurück, das ein Klon des aktuellen-Objekts ist.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn der [**Vorgang**](swbemobject.md) erfolgreich ist, gibt diese Methode ein neues-Objekt vom Metadatenobjekt zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Klon \_** Methode kann das **Err** -Objekt einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde **nichts** als Parameter angegeben, und es ist in dieser Verwendung nicht zulässig.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher zum Klonen des Objekts.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie **die \_ Clone** -Methode, um eine Klassendefinition oder eine-Instanz zu duplizieren. Dies ist hilfreich, wenn Sie die ursprüngliche Kopie des Objekts zu Sicherungszwecken benötigen, während Sie eine neue Kopie ändern. Verwenden Sie diese Methode ebenso, um viele neue Instanzen aus einer einzelnen Quell Instanz zu erstellen. Verwenden Sie z [**. b. "errbemubject. \_ SpawnInstance**](swbemobject-spawninstance-.md) ", um eine einzelne Start Instanz zu erstellen, und verwenden Sie " **errbemubject. Clone \_** ", um 100 Kopien der Instanz schnell zu erzeugen. Anschließend können Sie die Objekte ändern und jedem einzelnen bestimmte Werte geben.

Es ist nicht möglich, diese Methode zu verwenden, um eine Klassendefinition in eine-Instanz zu konvertieren oder um eine Instanz in eine Klassendefinition zu konvertieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Objekt<br/>                                                           |
| IID<br/>                      | IID \_ iswbemujekt<br/>                                                            |



 

 




