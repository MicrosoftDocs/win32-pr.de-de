---
title: Wmdrmkreateprovider-Funktion (wmdrmsdk. h)
description: Die wmdrmkreateprovider-Funktion erstellt eine Klassenfactory, die die anderen Objekte der erweiterten APIs für den Windows Media DRM-Client erstellen kann.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- Wmdrmkreateprovider-Funktion Windows Media-Format
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370587"
---
# <a name="wmdrmcreateprovider-function"></a>Wmdrmkreateprovider-Funktion

Die **wmdrmkreateprovider** -Funktion erstellt eine Klassenfactory, die die anderen Objekte der erweiterten APIs für den Windows Media DRM-Client erstellen kann. Diese Funktion erfordert keine stubbibliothek von Microsoft und erstellt Objekte, die die geschützten DRM-Funktionen nicht unterstützen.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
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



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Funktionen**](drm-functions.md)
</dt> <dt>

[**Wmdrmkreateprotectedprovider**](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 





