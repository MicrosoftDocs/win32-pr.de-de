---
description: Die \_ Path-Eigenschaft des SWbemLastError-Objekts gibt ein SWbemObjectPath-Objekt zurück, das den Objektpfad der aktuellen Klasse oder Instanz darstellt. Diese Eigenschaft kann als Parameter an Methoden übergeben werden, die einen Objektpfad erfordern.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: SWbemLastError.Path_-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5503d11d5c73f2bf955b25da9b5dbccbc18d41b9bc9b84bc3235993562938b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612200"
---
# <a name="swbemlasterrorpath_-property"></a>SWbemLastError.Path-Eigenschaft \_

Die **\_ Path-Eigenschaft** des [**SWbemLastError-Objekts**](swbemlasterror.md) gibt ein [**SWbemObjectPath-Objekt**](swbemobjectpath.md) zurück, das den Objektpfad der aktuellen Klasse oder Instanz darstellt. Diese Eigenschaft kann als Parameter an Methoden übergeben werden, die einen Objektpfad erfordern.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Nur die [**Class-Eigenschaft**](swbemobjectpath-class.md) der zurückgegebenen [**SWbemObjectPath-Instanz**](swbemobjectpath.md) kann geändert werden. Wenn Sie versuchen, eine andere Eigenschaft zu ändern oder die [**Methoden SetAsClass**](swbemobjectpath-setasclass.md) oder [**SetAsSingleton**](swbemobjectpath-setassingleton.md) aufzurufen, erhalten Sie den Fehler **wbemErrReadOnly.**

Aus diesem Grund können Sie das [**SWbemNamedValueSet-Objekt,**](swbemnamedvalueset.md) das der Wert der [**Keys-Eigenschaft**](swbemobjectpath-keys.md) der zurückgegebenen [**SWbemObjectPath-Instanz**](swbemobjectpath.md) ist, nicht ändern. Wenn Sie versuchen, die Methoden [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)oder [**DeleteAll**](swbemnamedvalueset-deleteall.md) für diesen Wert aufzurufen, erhalten Sie einen **wbemErrReadOnly-Fehler.** Darüber hinaus können Sie keine [**SWbemNamedValue**](swbemnamedvalue.md) ändern, die aus dieser Auflistung abgerufen wurden. Versuche, die [**Value-Eigenschaft**](swbemnamedvalue-value.md) zu ändern, geben den gleichen Fehlercode zurück.

Wenn Sie jedoch [**SWbemObject.Clone \_**](swbemobject-clone-.md) aufrufen, um eine Kopie zu erstellen, kann die [**Path-Eigenschaft \_**](swbemobject-path-.md) der Kopie vollständig geändert werden.

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



 

 




