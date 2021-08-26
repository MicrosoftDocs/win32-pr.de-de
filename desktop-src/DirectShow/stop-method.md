---
description: Die Stop-Methode beendet die Wiedergabe.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Stop-Methode (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9eb216c3ad5c98dd1722ff941131198cfe662d025b20c3f71fe9ea758e0a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050110"
---
# <a name="stop-method-directshow"></a>Stop-Methode (DirectShow)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `Stop` -Methode beendet die Wiedergabe.

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn [**EnableResetOnStop**](enableresetonstop-property.md) auf TRUE festgelegt ist, `Stop` versetzt der Aufruf von den DVD-Navigator zusammen mit dem Rest des Filterdiagramms in einen beendeten Zustand. Dies bedeutet, dass die Wiedergabe beim nächsten Drücken der Wiedergabeschaltfläche am Anfang des Datenträgers beginnt.  Wenn **EnableResetOnStop** auf TRUE festgelegt ist, wird die Wiedergabe dort fortgesetzt, wo sie aufgehört hat, wenn der Benutzer den nächsten **Play-Befehl** ausgibt.

 

 



