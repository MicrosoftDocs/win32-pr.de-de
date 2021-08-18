---
title: IWMDRMProvider CreateObject-Methode (Wmdrmsdk.h)
description: Die CreateObject-Methode ruft einen Zeiger auf eine angegebene Schnittstelle ab und erstellt bei Bedarf das implementierende Objekt.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- CreateObject-Methode windows Media Format
- CreateObject-Methode windows Media Format , IWMDRMProvider-Schnittstelle
- IWMDRMProvider-Schnittstelle windows Media Format , CreateObject-Methode
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f50341e33092b33b19ec3f41d968e0a1b7bc883ae959b200f6c7062e4c69996b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700776"
---
# <a name="iwmdrmprovidercreateobject-method"></a>IWMDRMProvider::CreateObject-Methode

Die **CreateObject-Methode** ruft einen Zeiger auf eine angegebene Schnittstelle ab und erstellt bei Bedarf das implementierende Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* \[ In\]
</dt> <dd>

Bezeichner der zu erstellenden Schnittstelle. Legen Sie auf einen der folgenden Werte fest.

-   IID \_ IWMDRMLicenseManagement
-   IID \_ IWMDRMLicenseQuery
-   IID \_ IWMDRMNetReceiver
-   IID \_ IWMDRMNetTransmitter
-   IID \_ IWMDRMSecurity

</dd> <dt>

*ppvObject* \[ out\]
</dt> <dd>

Adresse eines Zeigers, der die Adresse der angeforderten Schnittstelle empfängt.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMProvider-Schnittstelle**](iwmdrmprovider.md)
</dt> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**IWMDRMLicenseQuery-Schnittstelle**](iwmdrmlicensequery.md)
</dt> <dt>

[**IWMDRMNetReceiver-Schnittstelle**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetTransmitter-Schnittstelle**](iwmdrmnettransmitter.md)
</dt> <dt>

[**IWMDRMSecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> </dl>

 

 





