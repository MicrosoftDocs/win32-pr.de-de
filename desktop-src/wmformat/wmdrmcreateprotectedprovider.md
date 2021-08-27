---
title: WMDRMCreateProtectedProvider-Funktion (Wmdrmsdk.h)
description: Die WMDRMCreateProtectedProvider-Funktion erstellt eine Klassen factory, die die anderen Objekte der erweiterten APIs des Windows Media DRM-Clients erstellen kann.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- WMDRMCreateProtectedProvider-Funktion windows Media Format
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b5d71ff1deed01cc10d7342286b443b9f64b1a1c192af575a599a2fc8d8c9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026928"
---
# <a name="wmdrmcreateprotectedprovider-function"></a>WMDRMCreateProtectedProvider-Funktion

Die **WMDRMCreateProtectedProvider-Funktion** erstellt eine Klassen factory, die die anderen Objekte der erweiterten APIs des Windows Media DRM-Clients erstellen kann. Diese Funktion erfordert eine Stubbibliothek von Microsoft und erstellt Objekte, die die geschützten DRM-Funktionen unterstützen.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDRMProvider* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IWMDRMProvider-Schnittstelle**](iwmdrmprovider.md) des neu erstellten Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Funktionen**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProvider**](wmdrmcreateprovider.md)
</dt> </dl>

 

 





