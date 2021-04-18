---
description: Ruft die Isolationsstufe und den Timeout Wert einer Transaktion ab, die im Stamm Transaktionskontext gehostet wird.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: 'Icontexttransaktioninfo:: gettxisolationlevelandtimeout-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.GetTxIsolationLevelAndTimeout
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8545a697e672af7206a69ffa19618d5b70e055c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344847"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a>Icontexttransaktioninfo:: gettxisolationlevelandtimeout-Methode

Ruft die Isolationsstufe und den Timeout Wert einer Transaktion ab, die im Stamm Transaktionskontext gehostet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pisolevel* \[ vorgenommen\]
</dt> <dd>

Der [IsolationLevel](/previous-versions/windows/desktop/ms679234(v=vs.85)) -Wert für die Transaktion.

</dd> <dt>

*dwTime* \[ vorgenommen\]
</dt> <dd>

Das Timeout der Transaktion in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann die Standard Rückgabewerte e \_ invalidArg, e \_ oudef Memory, e \_ unerwartet und S OK zurückgeben \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontexttransaktioninfo**](icontexttransactioninfo.md)
</dt> </dl>

 

