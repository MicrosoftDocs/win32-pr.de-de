---
title: IConfigAsfWriter2 GetParam-Methode
description: Die GetParam-Methode ruft den aktuellen Wert des angegebenen Filterkonfigurationsparameters ab.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- GetParam-Methode windows Media Format
- GetParam-Methode windows Media Format , IConfigAsfWriter2-Schnittstelle
- IConfigAsfWriter2-Schnittstelle windows Media Format , GetParam-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a411e4b1896174e25a1f671f3f42fd83c1376713f10e9e4cb2b2d2186b3d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809140"
---
# <a name="iconfigasfwriter2getparam-method"></a>IConfigAsfWriter2::GetParam-Methode

Die **GetParam-Methode** ruft den aktuellen Wert des angegebenen Filterkonfigurationsparameters ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwParam* \[ In\]
</dt> <dd>

Gibt den abzurufenden Parameter an. Es muss sich um einen Wert handeln, der in der [ \_ AM \_ ASFWRITERCONFIG \_ PARAM-Enumeration](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) definiert ist.

</dd> <dt>

*pdwParam1* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die den Wert des in *dwParam* angegebenen Parameters abruft.

</dd> <dt>

*pdwParam2* \[ out\]
</dt> <dd>

Nicht verwendet, muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn ein Fehler auftritt, wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IConfigAsfWriter2-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 