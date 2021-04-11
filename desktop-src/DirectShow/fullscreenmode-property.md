---
description: Die Fullscreenmode-Eigenschaft legt einen Wert fest, der angibt, ob die Anzeige im Vollbildmodus ist, oder ruft diesen ab.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: Fullscreenmode (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96b3c0ca8261eb934e95eb7235b51e76e8c7579
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123554"
---
# <a name="fullscreenmode-property"></a>Fullscreenmode (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `FullScreenMode` Eigenschaft legt einen Wert fest, der angibt, ob die Anzeige im Vollbildmodus ist, oder ruft diesen ab.

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob die Vollbildwiedergabe aktiviert oder deaktiviert werden soll.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist Lese-/Schreibzugriff und hat den Standardwert false.



| Wert | BESCHREIBUNG                                            |
|-------|--------------------------------------------------------|
| true  | Aktivieren Sie die Vollbildwiedergabe. Dies ist der Standardwert. |
| false | Deaktivieren Sie die Vollbildwiedergabe.                          |



 

Der Vollbildmodus ist nur verfügbar, wenn das mswebdvd-Steuerelement im Fenstermodus ausgeführt wird.

 

 



