---
description: Die SubpictureStreamsAvailable-Eigenschaft ruft die Anzahl der im aktuellen Titel verfügbaren Unterbildstreams ab.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: SubpictureStreamsAvailable-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2349cb696c1f6d363fefb6a6e90a662fa7c3233b3b0aefcb57d381a604f41832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633440"
---
# <a name="subpicturestreamsavailable-property"></a>SubpictureStreamsAvailable-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die -Eigenschaft ruft die Anzahl der im aktuellen Titel verfügbaren `SubpictureStreamsAvailable` Unterbildstreams ab.

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a>Rückgabewert

Gibt die Anzahl der verfügbaren Streams als ganze Zahl zurück.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt und hat keinen Standardwert. Um jeden Stream nach seinem Sprachattribut abfragt, rufen Sie zuerst diese Methode auf, um die Obergrenze zu erhalten.

Die Datenstromnummerierung basiert auf null.

 

 



