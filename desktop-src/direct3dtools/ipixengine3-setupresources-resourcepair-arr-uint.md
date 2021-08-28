---
description: Übergibt Ressourcen an die Engine, z. B. Zeichenfolgen für Fehlermeldungen.
MS-HAID: vspixengine.IPixEngine3\_SetupResources\_ResourcePair\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine3::SetupResources-Methode
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
ms.openlocfilehash: 6c33bb9eea38575fa3acb4a94b926f9cce1af250
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628156"
---
# <a name="span-idvspixengineipixengine3_setupresources_resourcepair_arr_uintspanipixengine3setupresources-method"></a><span id="vspixengine.ipixengine3_setupresources_resourcepair_arr_uint"></span>IPixEngine3::SetupResources-Methode

Übergibt Ressourcen an die Engine, z. B. Zeichenfolgen für Fehlermeldungen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetupResources(
   ResourcePair [] count1_resources,
   UINT            count
);
```

## <a name="parameters"></a>Parameter

*\_count1-Ressourcen*   
Die übergebenen Ressourcenressourcen.

*Count*   
Die Anzahl der übergebenen Ressourcen.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPixEngine3**](/windows/desktop/direct3dtools/ipixengine3)

 

 
