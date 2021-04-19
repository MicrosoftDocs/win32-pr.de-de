---
title: Extern. Buy-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Methode kaufen initiiert den Kauf eines Satzes von Medien Elementen.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- Windows-Media Player "Methode kaufen"
- Kaufmethode Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, Methode kaufen
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
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354212"
---
# <a name="externalbuy-method"></a>Extern. Buy-Methode

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die Methode **kaufen** initiiert den Kauf eines Satzes von Medien Elementen.

## <a name="syntax"></a>Syntax


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ViewType* \[ in\]
</dt> <dd>

Eine **Zeichenfolge** , die den Typ des zu erstellenden Elements angibt. Der Aufrufer muss diesen Parameter auf eine der folgenden [Bibliotheks Speicherort Konstanten](library-location-constants.md)festlegen:

Cplistid

Cptrackid

Cpalbumid

</dd> <dt>

*Viewids* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die durch Semikolons getrennten IDs der zu erwerbenden Elemente enthält.

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

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern. Download**](external-download.md)
</dt> <dt>

[**Iwmpcontentpartner:: kaufen**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[**Erwerben von Medieninhalten**](purchasing-media-content.md)
</dt> </dl>

 

 





