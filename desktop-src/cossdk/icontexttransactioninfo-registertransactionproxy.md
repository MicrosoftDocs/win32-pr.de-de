---
description: Ordnet eine itransaktionproxy-Implementierung dem aktuellen Kontext zu.
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: 'Icontexttransaktioninfo:: registertransaktionproxy-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342389"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a>Icontexttransaktioninfo:: registertransaktionproxy-Methode

Ordnet eine [**itransaktionproxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) -Implementierung dem aktuellen Kontext zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pproxy* \[ in\]
</dt> <dd>

Eine [**itransaktionproxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) -Implementierung, die dem aktuellen Kontext zugeordnet werden soll.

</dd> <dt>

*pguid* \[ vorgenommen\]
</dt> <dd>

Eine GUID zum Identifizieren des Transaktions Proxys. Com+ verwendet diese GUID beim Aufrufen von [**itransaktionproxy:: Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) für den Transaktions Proxy.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ oudef Memory und e sowie \_ die folgenden Werte zurückgeben.



| Rückgabecode                                                                                                     | Beschreibung                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                            | Die Methode wurde erfolgreich abgeschlossen.<br/>                                                                           |
| <dl> <dt>**Kontext \_ E \_ alleseryintransaction**</dt> </dl> | Dem aktuellen Kontext ist bereits eine [**itransaktionproxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) -Implementierung zugeordnet.<br/> |
| <dl> <dt>**E \_ notimpl**</dt> </dl>                       | Der aktuelle Kontext gehostet eine Bring Your Own Transaction (BYOT)-Transaktion oder eine nicht-root-Transaktion.<br/>    |



 

## <a name="remarks"></a>Bemerkungen

Die **registertransaktionproxy** -Methode kann nur aufgerufen werden, wenn der aktuelle Kontext ein Stamm Transaktionskontext ist. Er kann nicht aufgerufen werden, wenn der Kontext eine BYOT-Transaktion oder eine nicht-root-Transaktion gehostet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontexttransaktioninfo**](icontexttransactioninfo.md)
</dt> </dl>

 

 




