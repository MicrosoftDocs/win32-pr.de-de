---
title: Downloader. Cancel-Methode
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Mit der Cancel-Methode wird der Download abgebrochen.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- Cancel-Methode, Windows-Media Player
- Cancel-Methode, Windows Media Player, Downloader-Klasse
- Download Item-Klasse, Windows Media Player, Cancel-Methode
topic_type:
- apiref
api_name:
- DownloadItem.cancel
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c14d538e85d0930a43db883e226c007bea70de24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361641"
---
# <a name="downloaditemcancel-method"></a>Downloader. Cancel-Methode

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Mit der Cancel-Methode wird der Download abgeb **Rochen** .

## <a name="syntax"></a>Syntax


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Abgebrochene Elemente werden nicht aus der Download Sammlung entfernt. Abgebrochene Elemente geben einen **DownloadState** -Wert von 4 (abgebrochen) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Download Item-Objekt**](downloaditem-object.md)
</dt> <dt>

[**Downloadaditem. DownloadState**](downloaditem-downloadstate.md)
</dt> </dl>

 

 





