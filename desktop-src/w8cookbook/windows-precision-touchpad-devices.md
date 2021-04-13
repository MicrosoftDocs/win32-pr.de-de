---
title: Touchpad-Geräte mit Windows Precision
description: Touchpad-Geräte mit Windows Precision
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07107c1d9532c4a4663a667a8e3db64124f23e5d
ms.sourcegitcommit: 40dd8501397fc79a643deb528c6c57ac2e9726ce
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/24/2020
ms.locfileid: "104389733"
---
# <a name="windows-precision-touchpad-devices"></a>Touchpad-Geräte mit Windows Precision

## <a name="platforms"></a>Plattformen

<dl> Clients-Windows 8.1  
</dl>

## <a name="description"></a>BESCHREIBUNG

Das Windows Precision Touchpad ist eine neue Klasse von Eingabegeräten, die Zeiger Eingabe-und Gesten Funktionen mit hoher Genauigkeit bereitstellen. Standardmäßig generieren diese Geräte bei der Nutzung von Desktop Anwendungen eine Bild Lauf radnachricht mit hoher Genauigkeit.

## <a name="manifestations"></a>Kundgebungen

Anwendungen, die nicht für das Verarbeiten von Bild Lauf radnachrichten mit hoher Genauigkeit konzipiert sind, können entweder über Scrollen oder nicht ordnungsgemäß scrollen.

## <a name="mitigation"></a>Minderung

Anwendungsentwickler sollten das Bild Lauf Delta in Mausrad-Nachrichten betrachten und ihre apps entsprechend ändern. in der Zwischenzeit kann eine Anwendung jedoch die Schiebe radnachrichten mit hoher Genauigkeit (Delta = 1) abwählen und sich für das Empfangen von Schiebe radnachrichten mit hoher Genauigkeit (Delta = 40) oder Standard-Scrollrad-Nachrichten entscheiden (Delta = 120).

## <a name="solution"></a>Lösung

Wenn die Anwendung in der Lage ist, Bild Lauf radnachrichten mit hoher Genauigkeit zu verarbeiten, muss nichts durchgeführt werden, da dies die von Windows Precision Touchpads gesendete Standardmeldung ist.

Wenn die Anwendung in der Lage ist, Nachrichten mit hoher Genauigkeit, aber nicht mit ultrahohem Genauigkeits Grad zu verarbeiten, fügen Sie dem Anwendungs Manifest Folgendes hinzu:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



Wenn die Anwendung keine Bild Lauf radnachrichten mit hoher Genauigkeit oder mit extrem hoher Genauigkeit verarbeiten kann, fügen Sie dem Anwendungs Manifest Folgendes hinzu, um anzugeben, dass standardmäßige Scrollrad Meldungen gewünscht werden sollen:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




