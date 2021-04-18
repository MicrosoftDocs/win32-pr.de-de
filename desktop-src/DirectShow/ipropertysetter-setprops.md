---
description: Die SetProperties-Methode legt die Eigenschaften des Zielobjekts für den angegebenen Zeitraum auf den entsprechenden Zustand fest.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: 'Ipropertysetter:: setrequiproperemethode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a36b1735ea5b8261c37bee66ac90b9a186a55f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361325"
---
# <a name="ipropertysettersetprops-method"></a>Ipropertysetter:: setrequiproper-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetProps` Methode legt die Eigenschaften des Zielobjekts für den angegebenen Zeitraum auf den entsprechenden Zustand fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTARGET* \[ in\]
</dt> <dd>

Zeiger auf das Zielobjekt, für das die Eigenschaften festgelegt werden sollen.

</dd> <dt>

*rtnow* \[ in\]
</dt> <dd>

Der Zeitpunkt, zu dem die Eigenschaften festgelegt werden sollen, in 100-Nanosecond-Einheiten oder – 1, um statische Eigenschaften festzulegen (solche, die sich im Laufe der Zeit nicht unterscheiden).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird von des aufgerufen, um die Eigenschaften eines Übergangs oder Effekts festzulegen. Eine Anwendung ruft normalerweise diese Methode nicht auf.

Das von *pTARGET* angegebene Objekt muss die **IDispatch** -Schnittstelle implementieren.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ipropertysetter-Schnittstelle**](ipropertysetter.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




