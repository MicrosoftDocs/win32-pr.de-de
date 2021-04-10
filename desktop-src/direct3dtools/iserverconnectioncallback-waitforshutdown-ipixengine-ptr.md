---
description: Wartet auf das Herunterfahren der angegebenen Engine (Blockierungs aufzurufen).
MS-HAID: vspixengine.IServerConnectionCallback\_WaitForShutdown\_IPixEngine\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iserverconnectioncallback:: waitforshutdown-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B70229D5-3C41-4B50-8336-A1271A9EBE81
api_name:
- IServerConnectionCallback.WaitForShutdown
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d98bd5f398748e6e62a099bcc2be94b5e5f27bc8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125354"
---
# <a name="span-idvspixengineiserverconnectioncallback_waitforshutdown_ipixengine_ptrspaniserverconnectioncallbackwaitforshutdown-method"></a><span id="vspixengine.iserverconnectioncallback_waitforshutdown_ipixengine_ptr"></span>Iserverconnectioncallback:: waitforshutdown-Methode

Wartet auf das Herunterfahren der angegebenen Engine (Blockierungs aufzurufen).

## <a name="syntax"></a>Syntax


```C++
HRESULT WaitForShutdown(
   IPixEngine * pEngine
);
```

## <a name="parameters"></a>Parameter

*Pendel*   
Die Engine, die heruntergefahren werden soll.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Iserverconnectioncallback**](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
