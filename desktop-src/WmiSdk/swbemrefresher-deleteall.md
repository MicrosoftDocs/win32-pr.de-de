---
description: Die Methode "Swap. DeleteAll" entfernt alle Elemente aus der Auflistung im Objekt "Swap-Aktualisierungs Programm". Das Swap-Aktualisierungs Objekt.
ms.assetid: c6e462d3-52b3-40c0-9a9c-fa268415a5f0
ms.tgt_platform: multiple
title: Taubemaktusher. DeleteAll-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
- ISWbemRefresher.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ddeb1c5fc8e7fb1f9c5682a2da0d9a1d6f53ba5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106355101"
---
# <a name="swbemrefresherdeleteall-method"></a>Taubemaktusher. DeleteAll-Methode

Die Methode " **Swap. DeleteAll** " entfernt alle Elemente aus der Auflistung im Objekt " [**Swap**](swbemrefresher.md) -Aktualisierungs Programm".

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemRefresher.DeleteAll()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

[**Die Aktualisierungs Eigenschaft für**](swbemrefreshableitem-refresher.md) das zugehörige " [**Swap**](swbemrefreshableitem.md) "-Element für jedes entfernte Element ist auf **null** festgelegt, was darauf hinweist, dass es kein übergeordnetes Aktualisierungs Programm mehr aufweist.

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

 

 




