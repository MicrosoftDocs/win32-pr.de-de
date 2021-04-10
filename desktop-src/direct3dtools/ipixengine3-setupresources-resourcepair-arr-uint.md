---
description: Übergibt Ressourcen an die-Engine, z. b. Zeichen folgen für Fehlermeldungen.
MS-HAID: vspixengine.IPixEngine3\_SetupResources\_ResourcePair\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine3:: setupresources-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1BB4BE17-51A2-4BA4-81F5-3678B7D5802B
api_name:
- IPixEngine3.SetupResources
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c2b103c5c27bf3929f72d909c9000a1e252e8dee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124729"
---
# <a name="span-idvspixengineipixengine3_setupresources_resourcepair_arr_uintspanipixengine3setupresources-method"></a><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>IPixEngine3:: setupresources-Methode

Übergibt Ressourcen an die-Engine, z. b. Zeichen folgen für Fehlermeldungen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetupResources(
   ResourcePair [] count1_resources,
   UINT            count
);
```

## <a name="parameters"></a>Parameter

*count1- \_ Ressourcen*   
Die Ressourcen Ressourcen wurden übermittelt.

*Countdown*   
Die Anzahl der bestandenen Ressourcen.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPixEngine3**](/windows/desktop/direct3dtools/ipixengine3)

 

 
