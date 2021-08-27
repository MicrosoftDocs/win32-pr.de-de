---
description: Ein Rückruf, der den Host von Mesh-Informationen benachrichtigt, die von der zugeordneten Anforderung geschrieben wurden.
MS-HAID: vspixengine.IPipeLineStagesCallback3\_MeshFileReadyCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback3::MeshFileReadyCallback-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BD4719A5-AC07-446A-A7CA-5978F869F66E
api_name:
- IPipeLineStagesCallback3.MeshFileReadyCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5c695ebad2f8a23757419fe3c6894a91b00cbd2d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625146"
---
# <a name="span-idvspixengineipipelinestagescallback3_meshfilereadycallback_bstrspanipipelinestagescallback3meshfilereadycallback-method"></a><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3::MeshFileReadyCallback-Methode

Ein Rückruf, der den Host von Mesh-Informationen benachrichtigt, die von der zugeordneten Anforderung geschrieben wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT MeshFileReadyCallback(
   BSTR meshFilename
);
```

## <a name="parameters"></a>Parameter

*meshFilename*   
Eine COM-Zeichenfolge, die den Pfadnamen der Datei enthält, in die die Gitternetzdaten geschrieben werden.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPipeLineStagesCallback3**](/windows/desktop/direct3dtools/ipipelinestagescallback3)

 

 
