---
title: Wmdrmkreateprotectedprovider-Funktion (wmdrmsdk. h)
description: Die wmdrmkreateprotectedprovider-Funktion erstellt eine Klassenfactory, die die anderen Objekte der erweiterten APIs für den Windows Media DRM-Client erstellen kann.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- Wmdrmkreateprotectedprovider-Funktion Windows Media-Format
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
ms.openlocfilehash: f1f046de906c7753fa200de5075cf2064721940b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365923"
---
# <a name="wmdrmcreateprotectedprovider-function"></a>Wmdrmkreateprotectedprovider-Funktion

Die **wmdrmkreateprotectedprovider** -Funktion erstellt eine Klassenfactory, die die anderen Objekte der erweiterten APIs für den Windows Media DRM-Client erstellen kann. Diese Funktion erfordert eine stubbibliothek von Microsoft und erstellt Objekte, die die geschützten DRM-Features unterstützen.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppdrmprovider* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iwmdrmprovider**](iwmdrmprovider.md) -Schnittstelle des neu erstellten Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Funktionen**](drm-functions.md)
</dt> <dt>

[**Wmdrmkreateprovider**](wmdrmcreateprovider.md)
</dt> </dl>

 

 





