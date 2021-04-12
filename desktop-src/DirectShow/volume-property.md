---
description: Die Volume-Eigenschaft legt das Lautstärke-Volume für die audiostreamausgabe fest oder ruft es ab.
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Volume-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9c85bc2d20a613e61d454f75b9663284188c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527806"
---
# <a name="volume-property"></a>Volume-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `Volume` -Eigenschaft legt das Lautsprecher Volume für die audiostreamausgabe fest oder ruft es ab.

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a>Rückgabewert

Gibt den volumengrad als Dämpfung in Dezibel als Ganzzahl zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist Lese-/Schreibzugriff mit einem Standardwert von 0. Das vollständige Volume ist 0, und 10.000 ist Ruhe. die Skala ist logarithmisch. Multiplizieren Sie die gewünschte Dezibelskala-Ebene um 100 (z. b. 10.000 = 100 dB).

 

 



