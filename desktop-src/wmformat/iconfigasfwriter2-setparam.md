---
title: IConfigAsfWriter2 SetParam-Methode
description: Die SetParam-Methode legt den Wert des angegebenen Filter Konfigurations Parameters fest.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- SetParam-Methode Windows Media-Format
- SetParam-Methode, Windows Media-Format, IConfigAsfWriter2-Schnittstelle
- IConfigAsfWriter2-Schnittstelle Windows Media-Format, SetParam-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341316"
---
# <a name="iconfigasfwriter2setparam-method"></a>IConfigAsfWriter2:: SetParam-Methode

Die **SetParam** -Methode legt den Wert des angegebenen Filter Konfigurations Parameters fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwparam* \[ in\]
</dt> <dd>

Gibt den festzulegenden Parameter an. Dabei muss es sich um einen Wert handeln, der in der Enumeration [ \_ am \_ asfschreiterconfig-Parameter \_ ](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) definiert ist.

</dd> <dt>

*dwParam1* \[ in\]
</dt> <dd>

Gibt den Wert an, der dem *dwparam* -Parameter zugewiesen werden soll.

</dd> <dt>

*dwParam2* \[ in\]
</dt> <dd>

Nicht verwendet; muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IConfigAsfWriter2-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2:: GetParam**](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 