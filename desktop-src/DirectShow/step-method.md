---
description: Die Step-Methode gibt DVD-Video um die angegebene Anzahl von Frames an.
ms.assetid: 6f67335e-51c7-4b81-8ab3-86a3d70ac871
title: Step-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5738e8704b24d64a429d8d38f1b9eac2f9b8ff7e22a7e9d1d2a29fb9df4f03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050310"
---
# <a name="step-method"></a>Step-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `Step` -Methode gibt DVD-Video um die angegebene Anzahl von Frames an.

``` syntax
MSWebDVD.Step(iFrames)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*Iframes*
</dt> <dd>

Gibt die Anzahl der Frames an, für die ein Einzelschritt als ganze Zahl festgelegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Rufen Sie vor dem Aufrufen dieser Methode [**CanStep**](canstep-method.md) auf, um zu bestimmen, ob der Decoder Frameschritte unterstützt.

Wenn die DVD-Video beim Aufrufen dieser Methode im umgekehrten Modus abspielt und der Decoder umgekehrte Rahmenschritte unterstützt, erfolgt die Frameschritte umgekehrt.

 

 



