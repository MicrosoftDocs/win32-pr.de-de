---
description: Die DisableAutoMouseProcessing-Eigenschaft aktiviert oder deaktiviert die Mausverarbeitungsfunktion des MSWebDVD-Objekts.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: DisableAutoMouseProcessing-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9728f968e1ce562bc8cc643b5c27b8ac2ace3db1b2d39c45a8ae1fa78b44971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749150"
---
# <a name="disableautomouseprocessing-property"></a>DisableAutoMouseProcessing-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DisableAutoMouseProcessing` -Eigenschaft aktiviert oder deaktiviert die Mausverarbeitungsfunktionalität des **MSWebDVD-Objekts.**

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob die Standardmäßige Mausverarbeitung deaktiviert werden soll.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist mit dem Standardwert false gelesen/geschrieben. Das **MSWebDVD-Objekt** verarbeitet standardmäßig automatisch Mausaktionen für DVD-Menüs auf dem Bildschirm. Benutzer können Menüschaltflächen ohne spezielle Programmierung durch die Anwendung hervorheben und aktivieren. Eine Anwendung kann diese standardmäßige Mausbehandlungsfunktion deaktivieren, indem diese Eigenschaft auf **true festgelegt wird.** Wenn die automatische Mausverarbeitung deaktiviert ist, muss eine Anwendung die verschiedenen schaltflächenbezogenen Methoden und Eigenschaften verwenden, um Mausbewegungen und Mausklicks in den Menüs auf dem Bildschirm zu verarbeiten. Außerdem kann eine Anwendung die schaltflächenbezogenen Methoden verwenden, um die automatische Mausbehandlung zu überschreiben, auch wenn auf `DisableAutoMouseProcessing` **FALSE festgelegt ist.**

 

 



