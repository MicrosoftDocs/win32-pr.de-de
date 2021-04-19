---
description: Die currentaudiostream-Eigenschaft legt die Nummer des aktivierten Audiostreams fest oder ruft Sie ab.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Currentaudiostream (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346823"
---
# <a name="currentaudiostream-property"></a>Currentaudiostream (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `CurrentAudioStream` -Eigenschaft legt die Nummer des aktivierten Audiostreams fest oder ruft Sie ab.

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert von 0 bis 7 zurück, der den aktuellen Audiostream angibt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist Lese-/Schreibzugriff und hat keinen Standardwert. Bevor Sie versuchen, einen neuen Audiostream festzulegen, wenden Sie [**isaudiostreamaktivierte**](isaudiostreamenabled-method.md) an, um sicherzustellen, dass der Stream verfügbar ist.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Audiostreamsavailable**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



