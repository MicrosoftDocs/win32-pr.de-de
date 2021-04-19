---
title: Downloader. getiteminfo-Methode
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die getiteminfo-Methode ruft den Wert eines Attributs für das Download Element ab.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- getiteminfo-Methode, Windows Media Player
- getiteminfo-Methode, Windows Media Player, Downloader-Klasse
- Downloader-Klasse, Windows Media Player, getiteminfo-Methode
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367624"
---
# <a name="downloaditemgetiteminfo-method"></a>Downloader. getiteminfo-Methode

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **getiteminfo** -Methode ruft den Wert eines Attributs für das Download Element ab.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ItemName* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Attributnamen enthält. Unterstützte Werte sind albumartist, Album, Duration, WM/Provider, Title, userrating und WM/tracknumber.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück, die den Wert des durch *ItemName* angegebenen Attributs enthält.

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft mithilfe der Bits-Beschreibungs Zeichenfolge angegebene Attribute ab. Weitere Informationen finden Sie unter [Windows Media Player Bits-Auftrags Konvention](windows-media-player-bits-job-convention.md).

Diese Methode wird für das Herunterladen im Hintergrund unterstützt. Der Code sollte diese Methode bei Verwendung von Echt Zeit Downloads nicht aufzurufen.

Diese Methode kann nur Informationen für BITS-Aufträge abrufen, die während der aktuellen Windows Media Player-Sitzung hinzugefügt wurden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Download Item. Type**](downloaditem-type.md)
</dt> <dt>

[**Download Item-Objekt**](downloaditem-object.md)
</dt> </dl>

 

 





