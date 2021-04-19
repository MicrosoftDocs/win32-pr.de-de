---
description: Die GetAt-Methode ruft ein Element durch einen NULL basierten Index aus der Auflistung ab.
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'Iportabledevicevaluescollection:: GetAt-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ffbc65f39aab63189aa451005008f585c46bd8d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373590"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a>Iportabledevicevaluescollection:: GetAt-Methode

Die **GetAt** -Methode ruft ein Element durch einen NULL basierten Index aus der Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

**DWORD** , das einen NULL basierten Index in der Auflistung angibt.

</dd> <dt>

*ppvalues* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf eine [**iportableendvicevalues**](iportabledevicevalues.md) -Schnittstelle aus der Auflistung empfängt. Der Aufrufer ist für das Aufrufen der **Freigabe** auf dieser Schnittstelle verantwortlich, wenn er damit abgeschlossen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                                                 |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der null basierte Index, der in der Übergabe war, liegt außerhalb des zulässigen Bereichs.<br/>             |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | Ein erforderliches Zeigerargument war **null**.<br/>                             |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Die-Auflistung enthält einen **null** - **iportableendvicevalues** -Zeiger.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Alle Änderungen, die an Werten in der abgerufenen Schnittstelle vorgenommen werden, werden an der in der Auflistung gespeicherten Version vorgenommen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Portablede vicetypes. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Portabledeviceguids. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iportableabvicevaluescollection-Schnittstelle**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




