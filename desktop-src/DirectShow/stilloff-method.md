---
description: Die Methode "stilloff" setzt die Wiedergabe fort und bricht den Modus "immer" ab
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: Stilloff-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8986b62585768b83fc5737012a924e6cf33daf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357880"
---
# <a name="stilloff-method"></a>Stilloff-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die Methode setzt die Wiedergabe fort und bricht den Modus "immer" ab `StillOff` .

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Der [DVD-Navigator](dvd-navigator-filter.md) wechselt in den Modus "immer wieder", wenn er auf einen noch auf der CD erstellten Frame trifft. Sie benachrichtigt Ihre Anwendung, indem eine EC- \_ DVD \_ an das Ereignis gesendet wird \_ . Der Modus unterscheidet sich nicht vom DVD-Navigator aufgrund eines Benutzer Vorgangs in einem angehaltenen Zustand. `StillOff`Beim Aufrufen von wird die Wiedergabe aus dem weiterhin Modus wieder aufgenommen, aber der DVD-Navigator wird nicht neu gestartet, wenn Sie sich im angehaltenen Zustand

 

 



