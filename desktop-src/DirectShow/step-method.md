---
description: Mit der Step-Methode wird der DVD-Video Stream um die angegebene Anzahl von Frames erweitert.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Step-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9c3f20e41c52bfa32c2cf0138c9e286c98e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362612"
---
# <a name="step-method"></a>Step-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `Step` Methode verschiebt den DVD-Video Stream um die angegebene Anzahl von Frames.

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*
</dt> <dd>

Gibt die Anzahl der Rahmen an, die als ganze Zahl durchlaufen werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Rufen Sie vor dem Aufrufen dieser Methode [**canstep**](canstep-method.md) auf, um zu bestimmen, ob der Decoder Frame-Step unterstützt.

Wenn die DVD-Video im umgekehrten Modus wiedergegeben wird, wenn diese Methode aufgerufen wird, und der Decoder die umgekehrte Frame Ausführung unterstützt, erfolgt die schrittweise Ausführung der Frame Ausführung in umgekehrter Reihenfolge.

 

 



