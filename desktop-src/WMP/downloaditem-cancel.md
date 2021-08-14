---
title: DownloadItem.cancel-Methode
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die cancel-Methode bricht den Download ab.
ms.assetid: b3715fde-6a83-45fa-92ea-1cbffbee7274
keywords:
- cancel-Windows Media Player
- cancel-Windows Media Player , DownloadItem-Klasse
- DownloadItem-Klasse Windows Media Player , cancel-Methode
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
ms.openlocfilehash: 6208719b5ac2e81fb9175db9de67bcf1f00ad7c34787ed1ab45251abd517bd65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749731"
---
# <a name="downloaditemcancel-method"></a>DownloadItem.cancel-Methode

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **cancel-Methode** bricht den Download ab.

## <a name="syntax"></a>Syntax


```JScript
DownloadItem.cancel()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Abgebrochene Elemente werden nicht aus der Downloadsammlung entfernt. Abgebrochene Elemente geben den **downloadState-Wert** 4 (abgebrochen) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DownloadItem-Objekt**](downloaditem-object.md)
</dt> <dt>

[**DownloadItem.downloadState**](downloaditem-downloadstate.md)
</dt> </dl>

 

 





