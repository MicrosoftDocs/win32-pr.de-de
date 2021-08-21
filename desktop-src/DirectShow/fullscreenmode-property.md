---
description: Die FullScreenMode-Eigenschaft legt einen Wert fest oder ruft einen Wert ab, der angibt, ob sich die Anzeige im Vollbildmodus befindet.
ms.assetid: e4682f50-080c-4f38-b2ca-ce4ca6b746d7
title: FullScreenMode-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 103938afa6710b858329147eafadec4e06fd7d2ba244b896dd1ac39c74cd12c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015618"
---
# <a name="fullscreenmode-property"></a>FullScreenMode-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `FullScreenMode` -Eigenschaft legt einen Wert fest oder ruft einen Wert ab, der angibt, ob sich die Anzeige im Vollbildmodus befindet.

``` syntax
[ bFullScreen = ] MSWebDVD.FullScreenMode
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob die Vollbildwiedergabe aktiviert oder deaktiviert werden soll.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist lese-/schreibgeschützt und hat den Standardwert false.



| Wert | BESCHREIBUNG                                            |
|-------|--------------------------------------------------------|
| true  | Aktivieren Sie die Vollbildwiedergabe. Dies ist der Standardwert. |
| false | Deaktivieren Sie die Vollbildwiedergabe.                          |



 

Der Vollbildmodus ist nur verfügbar, wenn das MSWebDVD-Steuerelement im Fenstermodus ausgeführt wird.

 

 



