---
description: Die WindowlessActivation-Eigenschaft initialisiert das MSWebDVD-Objekt zur Entwurfszeit für den Fenstermodus oder den fensterlosen Modus.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: WindowlessActivation-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6915dbf2ddcfe1b8925ccc1dc3c163799563d137e39e6d6260ad75f5496a0b1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982250"
---
# <a name="windowlessactivation-property"></a>WindowlessActivation-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `WindowlessActivation` -Eigenschaft initialisiert das **MSWebDVD-Objekt** zur Entwurfszeit für den Fenstermodus oder den fensterlosen Modus.

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a>Rückgabewert

Gibt zurück, ob sich das Objekt im Fenstermodus als boolescher Wert befindet.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist lese-/schreibgeschützt und hat den Standardwert true. Daher müssen Sie diese Eigenschaft nur festlegen, wenn Sie das **MSWebDVD-Objekt** in einem Container mit Fenstern ausführen. Wenn MSWebDVD auf einer Webseite in Microsoft enthalten ist® Internet Explorer befindet sich **mswebdvd** immer im Fensterlosen Modus, und Sie müssen diese Eigenschaft nicht festlegen.

 

 



