---
description: Ruft ein Array ab, das die Paket Eigenschaften Bezeichner für den angegebenen Strich enthält.
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'Icontextnode:: getstrokepacketdescriptionbyid-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348195"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a>Icontextnode:: getstrokepacketdescriptionbyid-Methode

Ruft ein Array ab, das die Paket Eigenschaften Bezeichner für den angegebenen Strich enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lstrokeid* \[ in\]
</dt> <dd>

Der Bezeichner für den Strich.

</dd> <dt>

*pulstrokepacketdescriptioncount* \[ in, out\]
</dt> <dd>

Die Anzahl der Paket Eigenschaften in jedem Paket.

</dd> <dt>

*ppstrokepacketdescriptionguids* \[ vorgenommen\]
</dt> <dd>

Ein Array, das die Paket Eigenschaften Bezeichner enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppstrokepacketdescriptionguids* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

\**ppstrokepacketdescriptionguids* enthält die global eindeutigen Bezeichner (GUIDs), die die Typen der Paketdaten beschreiben, die für jeden Punkt im Strich enthalten sind. Eine umfassende Liste der verfügbaren Paket Eigenschaften finden Sie unter [packetpropertyguids-Konstanten](packetpropertyguids-constants.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Icontextnode:: getstrokepacketdatabyid**](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

