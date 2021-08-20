---
title: External.download-Methode
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die Downloadmethode initiiert den Download eines Satzes von Medienelementen.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- download method Windows Media Player
- download-Methode Windows Media Player , External-Klasse
- Externe Klasse Windows Media Player , Downloadmethode
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 766f96a6db5f2114724e7545eaac7a269bf52e2e657872a8078b490621c794df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649220"
---
# <a name="externaldownload-method"></a>External.download-Methode

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **Downloadmethode** initiiert den Download eines Satzes von Medienelementen.

## <a name="syntax"></a>Syntax


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* \[ In\]
</dt> <dd>

Eine [Bibliotheksspeicherort-Konstante,](library-location-constants.md) die den Typ des herunterzuladenden Elements angibt. CPTrackID gibt beispielsweise an, dass mindestens eine Spur heruntergeladen werden soll.

</dd> <dt>

*IDs* \[ In\]
</dt> <dd>

**Zeichenfolge,** die die durch Semikolons getrennten IDs der herunterzuladenden Medienelemente enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Herunterladen von Medieninhalten**](downloading-media-content.md)
</dt> <dt>

[**Externes Objekt für Onlineshops vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.buy**](external-buy.md)
</dt> <dt>

[**IWMPContentPartner::D ownload**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





