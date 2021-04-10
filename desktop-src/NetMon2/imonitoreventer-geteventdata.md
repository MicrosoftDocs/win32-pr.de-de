---
description: Die geteventdata-Methode ordnet Speicherplatz für die nmeventdata-und nmcolumninfo-Strukturen zu.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'Imonitoreventer:: geteventdata-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: be1654c38f51fa62909e10c12900c087bf0842fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214532"
---
# <a name="imonitoreventergeteventdata-method"></a>Imonitoreventer:: geteventdata-Methode

Die **geteventdata** -Methode ordnet Speicherplatz für die [nmeventdata](nmeventdata.md) -und [nmcolumninfo](nmcolumninfo.md) -Strukturen zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bnumcolumns* \[ in\]
</dt> <dd>

Anzahl der **nmcolumninfo** -Strukturen, die benötigt werden.

</dd> <dt>

*ppnmeventdata* \[ vorgenommen\]
</dt> <dd>

Die Adresse der **nmeventdata** -Struktur, die zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert nmerr nicht genügend Arbeits \_ \_ \_ Speicher.

## <a name="remarks"></a>Bemerkungen

Monitore verwenden diese Methode, um Speicher für die Struktur von Ereignisdaten und Spalten Informationen zuzuweisen. Informationen zum Freigeben von Arbeitsspeicher, der einer **nmeventdata** -Struktur zugeordnet ist, finden Sie unter [imonitoreventer:: freeeventdata](imonitoreventer-freeeventdata.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Imonitoreventer Enter](imonitoreventer.md)
</dt> <dt>

[Imonitoreventer:: freeventdata](imonitoreventer-freeeventdata.md)
</dt> <dt>

[Nmeventdata](nmeventdata.md)
</dt> <dt>

[Nmcolumninfo](nmcolumninfo.md)
</dt> </dl>

 

 




