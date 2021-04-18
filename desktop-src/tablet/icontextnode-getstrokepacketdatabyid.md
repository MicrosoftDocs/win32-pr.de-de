---
description: Ruft ein Array ab, das die Paket Eigenschafts Daten für den angegebenen Strich enthält.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'Icontextnode:: getstrokepacketdatabyid-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343316"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a>Icontextnode:: getstrokepacketdatabyid-Methode

Ruft ein Array ab, das die Paket Eigenschafts Daten für den angegebenen Strich enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*strokeid* \[ in\]
</dt> <dd>

Der Bezeichner für den Strich.

</dd> <dt>

*pstrokepacketdatacount* \[ in, out\]
</dt> <dd>

Die Länge des Paketdaten Arrays.

</dd> <dt>

*pplstrokepacketdata* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Paketdaten für den Strich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher aus \* *pplstrokepacketdata* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

*plstrokepacketdata* enthält Paketdaten für alle Punkte im Strich. Verwenden Sie [**icontextnode:: getstrokepacketdescriptionbyid**](icontextnode-getstrokepacketdescriptionbyid.md), um die Typen der Paketdaten zu erhalten, die für jeden Punkt im Strich enthalten sind.

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

[**Icontextnode:: getstrokepacketdescriptionbyid**](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

