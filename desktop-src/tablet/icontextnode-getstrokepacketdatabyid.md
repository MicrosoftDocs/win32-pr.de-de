---
description: Ruft ein Array ab, das die Paketeigenschaftsdaten für den angegebenen Strich enthält.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: IContextNode::GetStrokePacketDataById-Methode (IACom.h)
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
ms.openlocfilehash: f80ad2e4acc88f24a14e21f604eb17dbab51a5bdeca0fc90ffc3ca9beb99f1de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967378"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a>IContextNode::GetStrokePacketDataById-Methode

Ruft ein Array ab, das die Paketeigenschaftsdaten für den angegebenen Strich enthält.

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

*strokeId* \[ In\]
</dt> <dd>

Der Bezeichner für den Strich.

</dd> <dt>

*pStrokePacketDataCount* \[ in, out\]
</dt> <dd>

Die Länge des Paketdatenarrays.

</dd> <dt>

*pplStrokePacketData* \[ out\]
</dt> <dd>

Ein Zeiger auf die Paketdaten für den Strich.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Arbeitsspeicherverlust zu vermeiden, verwenden Sie [**CoTaskMemFree,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um den Arbeitsspeicher aus \* *pplStrokePacketData* frei zu geben, wenn Sie die Informationen nicht mehr benötigen.

 

*plStrokePacketData enthält* Paketdaten für alle Punkte im Strich. Verwenden Sie [**IContextNode::GetStrokePacketDescriptionById,**](icontextnode-getstrokepacketdescriptionbyid.md)um die Paketdatentypen für jeden Punkt im Strich zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

