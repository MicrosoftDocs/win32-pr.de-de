---
title: External.buy-Methode
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die Buy-Methode initiiert den Kauf einer Gruppe von Medienelementen.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- buy-Windows Media Player
- buy-Methode Windows Media Player , Externe Klasse
- Externe Klasse Windows Media Player , buy-Methode
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acc578d18c2a93118e1d7aa55b0fdcbe474a8698a0982ef8c2df7edb3802ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649520"
---
# <a name="externalbuy-method"></a>External.buy-Methode

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **Buy-Methode** initiiert den Kauf einer Gruppe von Medienelementen.

## <a name="syntax"></a>Syntax


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ViewType* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Typ des zu erwerbenden Artikels angibt. Der Aufrufer muss diesen Parameter auf eine der folgenden [Bibliotheksspeicherortkonst constants festlegen:](library-location-constants.md)

CPListID

CPTrackID

CP CpuId

</dd> <dt>

*ViewIDs* \[ In\]
</dt> <dd>

**Eine** Zeichenfolge, die die durch Semikolons getrennten IDs der zu erwerbenden Artikel enthält.

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

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.download**](external-download.md)
</dt> <dt>

[**IWMPContentPartner::Buy**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[**Erwerb von Medieninhalten**](purchasing-media-content.md)
</dt> </dl>

 

 





