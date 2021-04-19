---
title: Extern. Download-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die Download-Methode initiiert den Download eines Satzes von Medien Elementen.
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- Windows-Media Player für die Download Methode
- Download Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, Download Methode
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
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352831"
---
# <a name="externaldownload-method"></a>Extern. Download-Methode

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **Download** -Methode initiiert den Download eines Satzes von Medien Elementen.

## <a name="syntax"></a>Syntax


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* \[ in\]
</dt> <dd>

Eine [Bibliotheks Speicherort Konstante](library-location-constants.md) , die den Typ des herunter zuladenden Elements angibt. Beispielsweise gibt cptrackid an, dass mindestens ein Titel heruntergeladen werden soll.

</dd> <dt>

*IDs* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die durch Semikolons getrennten IDs der zu ladenden Medienelemente enthält.

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

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern. kaufen**](external-buy.md)
</dt> <dt>

[**Iwmpcontentpartner::D ownload**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





