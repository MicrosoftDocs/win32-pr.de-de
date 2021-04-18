---
description: Die Methode "pulbemfreshableitem. Remove" entfernt das Objekt "pulbemfreshableitem" aus dem übergeordneten "pulbemaktusher"-Objekt. Das Objekt "Swap. metadatenableitem" aus dem übergeordneten "Swap"-Objekt.
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.tgt_platform: multiple
title: Taubemaktuableitem. Remove-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 028bff202108481ce498be02c6014141313f27cc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106354906"
---
# <a name="swbemrefreshableitemremove-method"></a>Taubemaktuableitem. Remove-Methode

Die Methode " **pulbemfreshableitem. Remove** " entfernt das Objekt " [**pulbemfreshableitem**](swbemrefreshableitem.md) " aus dem übergeordneten " [**pulbemaktusher**](swbemrefresher.md) "-Objekt.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntax


```VB
SWbemRefreshableItem.Remove( _
  [ ByVal lFlags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in, optional\]
</dt> <dd>

Dieser Parameter muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

**Fehler Codes** Wenn das Aktualisierungs Programm kein Element mit dem angegebenen Index enthält, wird **wbemErrNotFound** generiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID, \_ Swap-ableitem<br/>                                                  |
| IID<br/>                      | IID \_ iswbemerfrischendes ableitem<br/>                                                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Swap-aktuableitem**](swbemrefreshableitem.md)
</dt> <dt>

[**Swap-Aktualisierungs Programm**](swbemrefresher.md)
</dt> </dl>

 

 




