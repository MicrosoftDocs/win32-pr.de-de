---
title: IConfigAsfWriter2 GetParam-Methode
description: Die GetParam-Methode ruft den aktuellen Wert des angegebenen Filter Konfigurations Parameters ab.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- GetParam-Methode Windows Media-Format
- GetParam-Methode, Windows Media-Format, IConfigAsfWriter2-Schnittstelle
- IConfigAsfWriter2-Schnittstelle Windows Media-Format, GetParam-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339508"
---
# <a name="iconfigasfwriter2getparam-method"></a>IConfigAsfWriter2:: GetParam-Methode

Die **GetParam** -Methode ruft den aktuellen Wert des angegebenen Filter Konfigurations Parameters ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwparam* \[ in\]
</dt> <dd>

Gibt den Parameter an, der abgerufen werden soll. Dabei muss es sich um einen Wert handeln, der in der Enumeration [ \_ am \_ asfschreiterconfig-Parameter \_ ](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) definiert ist.

</dd> <dt>

*pdwParam1* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die den Wert des in *dwparam* angegebenen Parameters abruft.

</dd> <dt>

*pdwParam2* \[ vorgenommen\]
</dt> <dd>

Nicht verwendet, muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IConfigAsfWriter2-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 