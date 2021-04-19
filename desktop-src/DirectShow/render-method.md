---
description: Die Methode "Rendering" initialisiert das DVD-Filter Diagramm.
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Render-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342546"
---
# <a name="render-method"></a>Render-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `Render` Methode initialisiert das DVD-Filter Diagramm.

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*nicht ender*
</dt> <dd>

Gibt einen ganzzahligen Wert an, der angibt, ob das Filter Diagramm zerstört und neu erstellt wird.



| Wert | BESCHREIBUNG                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| 0     | Das Filter Diagramm wird nicht zerstört und neu erstellt, wenn es bereits vorhanden ist. Dies ist der Standardwert. |
| 1     | Das Filter Diagramm wird zerstört und neu erstellt, wenn es bereits vorhanden ist.                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Mit der- `Render` Methode kann das **mswebdvd** -Objekt beim Start das zugrunde liegende DirectShow-Filter Diagramm vollständig initialisieren. Dadurch entfällt die geringfügige Verzögerung, die andernfalls auftritt, wenn der Benutzer den ersten Befehl ausgibt, um eine CD wiederzugeben oder ein Menü anzuzeigen. Es gibt keinen Fall, in dem `Render` aufgerufen werden muss, bevor eine andere Methode aufgerufen wird. Wenn die Anwendung z. b. [**playtitle**](playtitle-method.md) aufruft, bevor das Filter Diagramm initialisiert wurde, ruft das **mswebdvd** -Objekt `Render` automatisch auf, bevor versucht wird, die Festplatte wiederzugeben.

 

 



