---
description: Die Item-Methode des "errbemubjectset"-Objekts Ruft ein "errbewbject" aus der Auflistung ab.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: Errbemubjectset. Item-Methode (wbemdisp. h)
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
ms.openlocfilehash: 69267b86a45cc1b95160e1400440b868426b7cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348881"
---
# <a name="swbemobjectsetitem-method"></a>Errbemubjectset. Item-Methode

Die **Item** -Methode des " [**errbemubjectset**](swbemobjectset.md) "-Objekts Ruft ein " [**errbewbject**](swbemobject.md) " aus der Auflistung ab.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strobjectpath* 
</dt> <dd>

Erforderlich. Relativer Pfad des-Objekts, das aus der Auflistung abgerufen werden soll. Beispiel: Win32 \_ LogicalDisk = "C:"

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, gibt das angeforderte [**Swap**](swbemobject.md) -Objekt zurück.

## <a name="error-codes"></a>Fehlercodes

Nach Abschluss der **Element** Methode kann das **Err** -Objekt einen der folgenden Fehlercodes enthalten.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Unbekannter Fehler.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Es wurde ein ungültiger Parameter angegeben.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)
</dt> <dd>

Das angeforderte Element wurde nicht gefunden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Item** -Methode kann viel Prozessorzeit erfordern, da eine komplette Enumeration durch den Anbieter der Elemente des Satzes erforderlich ist, um das Ergebnis zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Objekt Satz<br/>                                                        |
| IID<br/>                      | IID \_ iswbemubjectset<br/>                                                         |



 

 




