---
description: Die Methode "Swap. Item" gibt das angegebene "taubemfreshableitem" aus der Auflistung zurück. "Taubemerfrischendes ableitem" aus der Sammlung.
ms.assetid: 8ae3dea5-0582-422e-9cd8-b6d91b41588a
ms.tgt_platform: multiple
title: Taubemaktusher. Item-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Item
- ISWbemRefresher.Item
- ISWbemRefresher.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cfdbb592e6358fb1f8c5f3d45bb7e6bb780641c3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104218990"
---
# <a name="swbemrefresheritem-method"></a>Taubemaktusher. Item-Methode

Die Methode " **Swap. Item** " gibt das angegebene " [**taubemfreshableitem**](swbemrefreshableitem.md) " aus der Auflistung zurück.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
objItem = .Item( _
  ByVal lIndex _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Lindex* 
</dt> <dd>

Der Indexwert des Elements in der Auflistung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der-Befehl erfolgreich ausgeführt wurde, wird das angegebene-Objekt von " [**Swap-ableitem**](swbemrefreshableitem.md) " zurückgegeben.

## <a name="error-codes"></a>Fehlercodes

Wenn das Aktualisierungs Programm kein Element mit dem angegebenen Index enthält, wird **wbemErrNotFound** generiert.

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

 

 




