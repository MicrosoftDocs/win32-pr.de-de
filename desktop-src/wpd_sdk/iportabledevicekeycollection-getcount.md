---
description: Die GetCount-Methode ruft die Anzahl der Schlüssel in dieser Auflistung ab.
ms.assetid: 963f514e-3e0f-4334-ac29-6de7cc8aa336
title: IPortableDeviceKeyCollection::GetCount-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d5cd44ebcb17df00f8af2dad5d92445346c3c929500a78fce28358c0cf39a2cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194415"
---
# <a name="iportabledevicekeycollectiongetcount-method"></a>IPortableDeviceKeyCollection::GetCount-Methode

Die **GetCount-Methode** ruft die Anzahl der Schlüssel in dieser Auflistung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcElems* \[ In\]
</dt> <dd>

Zeiger auf ein **DWORD,** das die Anzahl der Schlüssel in der Auflistung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                               | Beschreibung                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Die Methode wurde erfolgreich ausgeführt.<br/>                     |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl> | Ein erforderliches Zeigerargument war **NULL.**<br/> |



 

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Abrufen von unterstützten Dienstereignissen.](retrieving-supported-events.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[Abrufen unterstützter Dienstereignisse](retrieving-supported-events.md)
</dt> <dt>

[Abrufen unterstützter Dienstmethoden](retrieving-supported-methods.md)
</dt> </dl>

 

 




