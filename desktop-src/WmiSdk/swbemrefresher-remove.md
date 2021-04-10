---
description: Die Methode "Swap. Remove" entfernt das Objekt "pulbemfreshableitem" mit dem angegebenen Index aus dem Aktualisierungs Programm.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: Taubemaktusher. Remove-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961180"
---
# <a name="swbemrefresherremove-method"></a>Swap. Remove-Methode

Die Methode " **Swap. Remove** " entfernt das Objekt " [**pulbemfreshableitem**](swbemrefreshableitem.md) " mit dem angegebenen Index aus dem Aktualisierungs Programm. Das Objekt " **taubemerfrischendes ableitem** " kann entweder ein einzelnes Objekt oder einen Objekt Satz darstellen.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Lindex* 
</dt> <dd>

Der Index des Elements im " [**Swap**](swbemrefresher.md) -Aktualisierer"-Objekt.

</dd> <dt>

*IFlags* \[ optionale\]
</dt> <dd>

Flags müssen auf T0 (null) festgelegt werden.

</dd> <dt>

*objwbemnamedvalueset* \[ optionale\]
</dt> <dd>

Null.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode hat keine Rückgabewerte.

## <a name="remarks"></a>Bemerkungen

**Fehlercodes** Wenn das Aktualisierungs Programm kein Element mit dem angegebenen Index enthält, wird **wbemErrNotFound** generiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austauschprogramm<br/>                                                        |
| IID<br/>                      | IID \_ iswbemfreshsher<br/>                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swap-Aktualisierungs Programm**](swbemrefresher.md)
</dt> </dl>

 

 




