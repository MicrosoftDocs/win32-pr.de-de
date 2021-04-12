---
description: Die autoreconnetct-Eigenschaft des-Objekts "Swap-Aktualisierungs Programm" ist ein boolescher Wert, der angibt, ob das Aktualisierungs Programm automatisch erneut eine Verbindung mit einem Remote Anbieter herstellt, wenn die Verbindung getrennt ist.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: Taubemaktusher. autoreconnetct-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4faa02a4a77409bb8b1813ee433c326d1c45d1bd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351319"
---
# <a name="swbemrefresherautoreconnect-property"></a>' Swap. autoreconnetct '-Eigenschaft

Die **autoreconnetct** -Eigenschaft des-Objekts " [**Swap**](swbemrefresher.md) -Aktualisierungs Programm" ist ein boolescher Wert, der angibt, ob das Aktualisierungs Programm automatisch erneut eine Verbindung mit einem Remote Anbieter herstellt, wenn die Verbindung getrennt ist.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Das Ändern dieser Eigenschaft wirkt sich nur auf Objekte im Aktualisierungs Programm aus, die von einem Hochleistungs Anbieter unterstützt werden. Wenn es sich bei dem Anbieter nicht um einen Hochleistungs Anbieter handelt, hat das Festlegen der **autoreconnetct** -Eigenschaft auf **true** keine Auswirkung, da das Objekt " [**Swap**](swbemrefresher.md) -Aktualisierungs Programm" nie erneut eine Verbindung herstellt.

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

 

 




