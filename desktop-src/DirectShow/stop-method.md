---
description: Die Stopp Methode beendet die Wiedergabe.
ms.assetid: e1ebfacc-4f33-4b4d-8e6c-1d1e1f0a22bd
title: Stoppmethode (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c8cae45c7f076f2c4e90f1e7f50676bebbd3482
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960396"
---
# <a name="stop-method-directshow"></a>Stoppmethode (DirectShow)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `Stop` Methode beendet die Wiedergabe.

``` syntax
MSWebDVD.Stop()
```

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn [**enableresetonstopp**](enableresetonstop-property.md) auf true festgelegt ist, wird `Stop` beim Aufrufen der DVD-Navigator zusammen mit dem restlichen Filter Diagramm in einen beendeten Zustand versetzt. das bedeutet, dass die Wiedergabe beim nächsten Drücken **der** Wiedergabe Schaltfläche am Anfang der CD beginnt. Wenn **enableresetonstopps** auf true festgelegt ist, wird die Wiedergabe an der Stelle fortgesetzt, an der der Benutzer den nächsten Befehl zum **abspielen** ausgibt

 

 



