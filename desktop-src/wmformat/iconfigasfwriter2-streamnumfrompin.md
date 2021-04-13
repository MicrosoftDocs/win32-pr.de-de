---
title: IConfigAsfWriter2 streamnumfrompin-Methode
description: Die streamnumfrompin-Methode ruft die Datenstrom Nummer ab, die der angegebenen Eingabe-PIN zugeordnet ist.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- Streamnumfrompin-Methode Windows Media-Format
- Streamnumfrompin-Methode, Windows Media-Format, IConfigAsfWriter2-Schnittstelle
- IConfigAsfWriter2-Schnittstelle Windows Media-Format, streamnumfrompin-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c63a31d515e70b0ee0ac5be617ee52fe23bd5416
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390453"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>IConfigAsfWriter2:: streamnumfrompin-Methode

Die **streamnumfrompin** -Methode ruft die Datenstrom Nummer ab, die der angegebenen Eingabe-PIN zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppin* \[ in\]
</dt> <dd>

Zeiger auf die **IPin** -Schnittstelle für die Eingabe-PIN.

</dd> <dt>

*pwstreamnum* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger, der die streamnummer empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Manchmal müssen Sie die SDK-Schnittstellen des Windows Media-Formats direkt verwenden, um einen Stream vor dem Ausführen eines Filter Diagramms zu bearbeiten. Da Sie nicht davon ausgehen können, dass eine ASF-Datenstrom Nummer mit der Nummer der DirectShow-Pin übereinstimmt, wird diese Methode bereitgestellt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IConfigAsfWriter2-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 