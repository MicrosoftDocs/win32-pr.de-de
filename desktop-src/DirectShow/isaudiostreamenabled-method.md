---
description: Die IsAudioStreamEnabled-Methode ruft einen Wert ab, der angibt, ob der angegebene Audiostream im aktuellen Titel aktiviert ist.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: IsAudioStreamEnabled-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2131376346f2a0311fc5acd8e0051292a12fb0145b44226363c7d891a5ef3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817475"
---
# <a name="isaudiostreamenabled-method"></a>IsAudioStreamEnabled-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `IsAudioStreamEnabled` -Methode ruft einen Wert ab, der angibt, ob der angegebene Audiostream im aktuellen Titel aktiviert ist.

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Gibt den Audiostream als Ganzzahlwert von 0 bis 7 an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob der angegebene Audiostream für den aktuellen Titel verfügbar ist. True bedeutet, dass es verfügbar ist.

## <a name="remarks"></a>Hinweise

Obwohl ein Datenträger bis zu acht unabhängige Audiostreams enthalten kann, ist nicht unbedingt jeder Stream für jeden Titel verfügbar. Ein Haupttitel eines Films kann beispielsweise drei Audiostreams für Englisch, Spanisch und Japanisch haben, aber der Titel "ComingEntspricht" kann nur einen Audiostream auf Englisch haben. Überprüfen Sie immer, ob ein Stream für einen Titel verfügbar ist, bevor Sie die [**CurrentAudioStream-Eigenschaft**](currentaudiostream-property.md) festlegen.

 

 



