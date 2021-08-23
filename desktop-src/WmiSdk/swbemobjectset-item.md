---
description: Die Item-Methode des SWbemObjectSet-Objekts ruft ein SWbemObject aus der Auflistung ab.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: SWbemObjectSet.Item-Methode (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a0d357eda1098bd20e4ebc68f5b959b7ac5ffd4fb46788ffac99d1f18678d6a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857220"
---
# <a name="swbemobjectsetitem-method"></a>SWbemObjectSet.Item-Methode

Die **Item-Methode** des [**SWbemObjectSet-Objekts**](swbemobjectset.md) ruft ein [**SWbemObject**](swbemobject.md) aus der Auflistung ab.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

## <a name="syntax"></a>Syntax


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Erforderlich. Relativer Pfad des Objekts, das aus der Auflistung abgerufen werden soll. Beispiel: Win32 \_ LogicalDisk="C:"

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, wird das angeforderte [**SWbemObject-Objekt**](swbemobject.md) zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Item-Methode** kann das **Err-Objekt** einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Nicht genügend Arbeitsspeicher, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrNotFound** – 2147749890 (0x80041002)
</dt> <dd>

Angefordertes Element wurde nicht gefunden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Item-Methode** kann viel Prozessorzeit erfordern, da eine vollständige Enumeration durch den Anbieter der Elemente des Satzes erforderlich ist, um das Ergebnis zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



 

 




