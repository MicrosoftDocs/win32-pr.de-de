---
title: Iwmdrmprovider-Methode "kreateobject" (wmdrmsdk. h)
description: Die Methode "kreateobject" Ruft einen Zeiger auf eine angegebene Schnittstelle ab und erstellt bei Bedarf das implementierende Objekt.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Methode "kreateobject" Windows Media Format
- Kreateobject-Methode Windows Media-Format, iwmdrmprovider-Schnittstelle
- Iwmdrmprovider-Schnittstelle Windows Media-Format, Methode "kreateobject"
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
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356358"
---
# <a name="iwmdrmprovidercreateobject-method"></a>Iwmdrmprovider:: kreateobject-Methode

Die Methode " **kreateobject** " Ruft einen Zeiger auf eine angegebene Schnittstelle ab und erstellt bei Bedarf das implementierende Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* \[ in\]
</dt> <dd>

Der Bezeichner der zu erstellenden Schnittstelle. Legen Sie auf einen der folgenden Werte fest.

-   IID \_ iwmdrmlicenabmanagement
-   IID \_ iwmdrmlicensequery
-   IID \_ iwmdrmnetreceiver
-   IID \_ iwmdrmnettransmitter
-   IID \_ iwmdrmsecurity

</dd> <dt>

*ppvobject* \[ vorgenommen\]
</dt> <dd>

Adresse eines Zeigers, der die Adresse der angeforderten Schnittstelle empfängt.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmprovider-Schnittstelle**](iwmdrmprovider.md)
</dt> <dt>

[**Iwmdrmlicenabmanagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Iwmdrmlicensequery-Schnittstelle**](iwmdrmlicensequery.md)
</dt> <dt>

[**Iwmdrmnetreceiver-Schnittstelle**](iwmdrmnetreceiver.md)
</dt> <dt>

[**Iwmdrmnettransmitter-Schnittstelle**](iwmdrmnettransmitter.md)
</dt> <dt>

[**Iwmdrmsecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> </dl>

 

 





