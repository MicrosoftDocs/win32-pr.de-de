---
description: Die CurrentAudioStream-Eigenschaft legt die Nummer des aktivierten Audiostreams fest oder ruft sie ab.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: CurrentAudioStream-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd814d5b560ed55ea312fbebb8678c67b1422b0cf3d47917fbf772f56a0d3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075970"
---
# <a name="currentaudiostream-property"></a>CurrentAudioStream-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `CurrentAudioStream` -Eigenschaft legt die Nummer des aktivierten Audiostreams fest oder ruft sie ab.

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zwischen 0 und 7 zurück, der den aktuellen Audiostream angibt.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist Lese-/Schreibzugriff ohne Standardwert. Bevor Sie versuchen, einen neuen Audiostream festzulegen, rufen Sie [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) auf, um zu überprüfen, ob der Stream verfügbar ist.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AudioStreamsAvailable**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



