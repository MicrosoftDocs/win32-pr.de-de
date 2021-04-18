---
description: Die windowlessactivation-Eigenschaft initialisiert das mswebdvd-Objekt zur Entwurfszeit für den Fenstermodus oder den fensterlosen Modus.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Windowlessactivation (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427fdcb265d60200bfe8716cd1ece384861fbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352535"
---
# <a name="windowlessactivation-property"></a>Windowlessactivation (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `WindowlessActivation` Eigenschaft initialisiert das **mswebdvd** -Objekt zur Entwurfszeit für den Fenstermodus oder den fensterlosen Modus.

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a>Rückgabewert

Gibt zurück, ob sich das Objekt im Fenstermodus als boolescher Wert befindet.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft verfügt über Lese-/Schreibzugriff mit dem Standardwert true. Daher müssen Sie diese Eigenschaft nur festlegen, wenn Sie das **mswebdvd** -Objekt in einem Fenster Container ausführen. Wenn Sie in einer Webseite in Microsoft® Internet Explorer enthalten ist, befindet sich **mswebdvd** immer im fensterlosen Modus, und Sie müssen diese Eigenschaft nicht festlegen.

 

 



