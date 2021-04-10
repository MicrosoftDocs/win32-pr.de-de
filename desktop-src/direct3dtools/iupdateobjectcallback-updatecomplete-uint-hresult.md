---
description: Ein Rückruf, der verwendet wird, um den Host zu benachrichtigen, dass ein Objekt aktualisiert wurde.
MS-HAID: vspixengine.IUpdateObjectCallback\_UpdateComplete\_UINT\_HRESULT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iupdateobjectcallback:: updatecomplete-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7F54DDEC-E595-4615-B9B7-B1213A58B362
api_name:
- IUpdateObjectCallback.UpdateComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b601d8ac785f65c4400821741b83e76bd6987481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124694"
---
# <a name="span-idvspixengineiupdateobjectcallback_updatecomplete_uint_hresultspaniupdateobjectcallbackupdatecomplete-method"></a><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>Iupdateobjectcallback:: updatecomplete-Methode

Ein Rückruf, der verwendet wird, um den Host zu benachrichtigen, dass ein Objekt aktualisiert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdateComplete(
   UINT    objectAddress,
   HRESULT result
);
```

## <a name="parameters"></a>Parameter

*objectaddress*   
Die ID des Objekts, das aktualisiert wurde.

*result*   
Gibt an, ob das Update erfolgreich ausgeführt wurde.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Iupdateobjectcallback**](/windows/desktop/direct3dtools/iupdateobjectcallback)

 

 
