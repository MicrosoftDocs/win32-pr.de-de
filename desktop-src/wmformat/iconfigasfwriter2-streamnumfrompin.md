---
title: IConfigAsfWriter2-StreamNumFromPin-Methode
description: Die StreamNumFromPin-Methode ruft die Streamnummer ab, die dem angegebenen Eingabepin zugeordnet ist.
ms.assetid: f645a742-e6dc-4041-8a56-3bbb5188a9a9
keywords:
- 'StreamNumFromPin-Methode : Windows Media Format'
- StreamNumFromPin-Methode windows Media Format , IConfigAsfWriter2-Schnittstelle
- IConfigAsfWriter2-Schnittstelle windows Media Format , StreamNumFromPin-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.StreamNumFromPin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9124d3acaea81e36b212f3dec001374cc035efca449f35af5e43fa18ce50d6dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839821"
---
# <a name="iconfigasfwriter2streamnumfrompin-method"></a>IConfigAsfWriter2::StreamNumFromPin-Methode

Die **StreamNumFromPin-Methode** ruft die Streamnummer ab, die dem angegebenen Eingabepin zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT StreamNumFromPin(
  [in]  IPin *pPin,
  [out] WORD *pwStreamNum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPin* \[ In\]
</dt> <dd>

Zeiger auf die **IPin-Schnittstelle** auf dem Eingabepin.

</dd> <dt>

*pwStreamNum* \[ out\]
</dt> <dd>

Zeiger, der die Streamnummer empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn ein Fehler auftritt, wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Manchmal müssen Sie möglicherweise die Windows Media Format SDK-Schnittstellen direkt verwenden, um einen Stream vor dem Ausführen eines Filterdiagramms zu bearbeiten. Da Sie nicht davon ausgehen können, dass eine ASF-Streamnummer mit der Pinnummer von DirectShow identisch ist, wird diese Methode bereitgestellt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IConfigAsfWriter2-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

 