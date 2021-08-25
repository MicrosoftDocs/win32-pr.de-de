---
description: Ruft die Isolationsstufe und den Timeoutwert einer Transaktion ab, die im Stammtransaktionskontext gehostet wird.
ms.assetid: bb3ff03e-e69e-4a50-af36-4938eb4323df
title: IContextTransactionInfo::GetTxIsolationLevelAndTimeout-Methode
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
ms.openlocfilehash: 41888a859b6b665390290ba66bed69418cbddd9b708355dc78cc2670ba4d240f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896080"
---
# <a name="icontexttransactioninfogettxisolationlevelandtimeout-method"></a>IContextTransactionInfo::GetTxIsolationLevelAndTimeout-Methode

Ruft die Isolationsstufe und den Timeoutwert einer Transaktion ab, die im Stammtransaktionskontext gehostet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTxIsolationLevelAndTimeout(
  [out] ISOLEVEL *pIsoLevel,
  [out] DWORD    *dwTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pIsoLevel* \[ out\]
</dt> <dd>

Der [ISOLATIONLEVEL-Wert](/previous-versions/windows/desktop/ms679234(v=vs.85)) für die Transaktion.

</dd> <dt>

*dwTime* \[ out\]
</dt> <dd>

Das Timeout der Transaktion in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann die Standardrückgabewerte E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED und S OK \_ zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextTransactionInfo**](icontexttransactioninfo.md)
</dt> </dl>

 

