---
title: IConfigAsfWriter2 SetParam-Methode
description: Die SetParam-Methode legt den Wert des angegebenen Filterkonfigurationsparameters fest.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- SetParam-Methode windows Media Format
- SetParam-Methode windows Media Format , IConfigAsfWriter2-Schnittstelle
- IConfigAsfWriter2-Schnittstelle windows Media Format , SetParam-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e7c73831ec45e6e0b65444e93e976fe349a2d4576d578f3399c60c399628cbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847498"
---
# <a name="iconfigasfwriter2setparam-method"></a>IConfigAsfWriter2::SetParam-Methode

Die **SetParam-Methode** legt den Wert des angegebenen Filterkonfigurationsparameters fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwParam* \[ In\]
</dt> <dd>

Gibt den festzulegenden Parameter an. Es muss sich um einen Wert handeln, der in der [ \_ AM \_ ASFWRITERCONFIG \_ PARAM-Enumeration](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) definiert ist.

</dd> <dt>

*dwParam1* \[ In\]
</dt> <dd>

Gibt den Wert an, der dem *dwParam-Parameter* zugewiesen werden soll.

</dd> <dt>

*dwParam2* \[ In\]
</dt> <dd>

Nicht verwendet; muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn ein Fehler auftritt, wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IConfigAsfWriter2-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2::GetParam**](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 