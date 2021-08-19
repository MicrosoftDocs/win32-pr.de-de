---
description: Die IsSubpictureStreamEnabled-Methode ruft einen Wert ab, der angibt, ob der angegebene Unterbilddatenstrom im aktuellen Titel aktiviert ist.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: IsSubpictureStreamEnabled-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc982120b6a7a57d59d5213fc57b5ba3851d7d9d2f4c3e553fba97d3307d8bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817047"
---
# <a name="issubpicturestreamenabled-method"></a>IsSubpictureStreamEnabled-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `IsSubpictureStreamEnabled` -Methode ruft einen Wert ab, der angibt, ob der angegebene Unterbilddatenstrom im aktuellen Titel aktiviert ist.

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Gibt den Unterbilddatenstrom als ganze Zahl an.



| Wert   | Beschreibung              |
|---------|--------------------------|
| 0 bis 31 | Subpicture-Datenstrom        |
| 63      | Stummgeschalteter Datenstrom mit niedriger Bitrate |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob der angegebene Audiostream im aktuellen Titel verfügbar ist. True bedeutet, dass sie verfügbar ist.

## <a name="remarks"></a>Hinweise

Obwohl ein Datenträger bis zu 32 Datenströme enthalten kann, ist nicht unbedingt jeder Stream für jeden Titel verfügbar. Überprüfen Sie immer, ob ein Stream für einen Titel verfügbar ist, bevor Sie die [**CurrentSubpictureStream-Eigenschaft**](currentsubpicturestream-property.md) festlegen.

 

 



