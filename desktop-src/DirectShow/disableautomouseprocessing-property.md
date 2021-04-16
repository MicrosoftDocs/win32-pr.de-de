---
description: Die disableautomouseprocessing-Eigenschaft aktiviert oder deaktiviert die mouseprocessing-Funktionalität des mswebdvd-Objekts.
ms.assetid: d438deb8-3c6d-49c1-923b-d4c57e236fc9
title: Disableautomouabprocessing (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b606392acd4030d68af9590555a40d571d70c581
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480859"
---
# <a name="disableautomouseprocessing-property"></a>Disableautomouabprocessing (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `DisableAutoMouseProcessing` -Eigenschaft aktiviert oder deaktiviert die mouseprocessing-Funktionalität des **mswebdvd** -Objekts.

``` syntax
[ bMouseProcessing = ] MSWebDVD.DisableAutoMouseProcessing
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob die Standard Maus Verarbeitung deaktiviert werden soll.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist Lese-/Schreibzugriff und hat den Standardwert false. Das **mswebdvd** -Objekt verarbeitet automatisch Mausaktionen für DVD-Menüs auf dem Bildschirm. Benutzer können Menü Schaltflächen ohne besondere Programmierung durch die Anwendung markieren und aktivieren. Eine Anwendung kann diese standardmäßige mousehandling-Funktion deaktivieren, indem diese Eigenschaft auf **true** festgelegt wird. Wenn die automatische Maus Verarbeitung deaktiviert ist, muss eine Anwendung die verschiedenen Schaltflächen bezogenen Methoden und Eigenschaften verwenden, um Mausbewegungen und Mausklicks in den Menüs auf dem Bildschirm zu behandeln. Außerdem kann eine Anwendung mit den Schaltflächen bezogenen Methoden die automatische Maus Behandlung überschreiben, auch wenn `DisableAutoMouseProcessing` auf **false** festgelegt ist.

 

 



