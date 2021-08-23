---
description: Die Volume-Eigenschaft legt die Lautstärke des Lautsprechers für die Audiostreamausgabe fest oder ruft sie ab.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Volume-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c7ebd89b971e8a8f934608ff38dc741c0db91ac2d25f717d7354b3d6294b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632880"
---
# <a name="volume-property"></a>Volume-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `Volume` -Eigenschaft legt die Lautstärke des Lautsprechers für die Audiostreamausgabe fest oder ruft sie ab.

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a>Rückgabewert

Gibt die Volumeebene als Dämpfung in Dezibel als ganze Zahl zurück.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist mit dem Standardwert 0 (0) gelesen/geschrieben. Das vollständige Volume ist 0, und 10.000 ist Stille. die Skala logarithmisch ist. Multiplizieren Sie den gewünschten Dezibelwert mit 100 (z. B. 10.000 = 100 dB).

 

 



