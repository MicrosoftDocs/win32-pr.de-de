---
description: Ruft die Anzahl der Tablets ab, die an das System angefügt sind.
ms.assetid: b2027336-611b-4d17-8943-f16770effaf8
title: 'Itabletmanager:: gettabletcount-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager.GetTabletCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fbdd485c44bc67b3ecaec5aa279d4bc20e18d167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218366"
---
# <a name="itabletmanagergettabletcount-method"></a>Itabletmanager:: gettabletcount-Methode

Ruft die Anzahl der Tablets ab, die an das System angefügt sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTabletCount(
  [out] ULONG *pcTablets
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pctablets* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der Tablets, die an das System angefügt sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itabletmanager-Schnittstelle**](itabletmanager.md)
</dt> </dl>

 

 




