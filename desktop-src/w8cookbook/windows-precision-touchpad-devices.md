---
title: Windows Präzisionstouchpad-Geräte
description: Windows Präzisionstouchpad-Geräte
ms.assetid: 026F9940-C985-4F3A-BDBB-2977B14EAB1F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb81978c9c9849dfa0d073a4b37af3760d1d4e5bc8e8fa2e81317293db04fc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007900"
---
# <a name="windows-precision-touchpad-devices"></a>Windows Präzisionstouchpad-Geräte

## <a name="platforms"></a>Plattformen

<dl> Clients – Windows 8.1  
</dl>

## <a name="description"></a>Beschreibung

Das Windows Precision Touchpad ist eine neue Klasse von Eingabegeräten, die Eingabe- und Gestenfunktionen mit hoher Genauigkeit bereitstellen. Standardmäßig generieren diese Geräte Scrollradmeldungen mit äußerst hoher Genauigkeit für die Nutzung von Desktopanwendungen.

## <a name="manifestations"></a>Manifestationen

Anwendungen, die nicht für die Verarbeitung von Scrollradnachrichten mit äußerst hoher Genauigkeit konzipiert sind, können entweder über- oder nicht ordnungsgemäß scrollen.

## <a name="mitigation"></a>Minderung

Anwendungsentwickler sollten sich das Scrolldelta in Mausradmeldungen ansehen und ihre Apps entsprechend ändern. In der Zwischenzeit kann eine Anwendung jedoch Scrollradnachrichten mit äußerst hoher Genauigkeit (Delta = 1) deaktivieren und sich für den Empfang von Scrollradnachrichten mit hoher Genauigkeit (Delta = 40) oder Standard-Scrollradnachrichten (Delta = 120) entscheiden.

## <a name="solution"></a>Lösung

Wenn die Anwendung Scrollradnachrichten mit äußerst hoher Genauigkeit verarbeiten kann, muss nichts geschehen, da dies die Standardnachricht ist, die von Windows Precision Touchpads gesendet wird.

Wenn die Anwendung Scrollradnachrichten mit hoher Genauigkeit verarbeiten kann, aber keine Radnachrichten mit äußerst hoher Genauigkeit, fügen Sie dem Anwendungsmanifest Folgendes hinzu:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



Wenn die Anwendung nicht in der Lage ist, Scrollradnachrichten mit hoher Genauigkeit oder Radnachrichten mit äußerst hoher Genauigkeit zu verarbeiten, fügen Sie dem Anwendungsmanifest Folgendes hinzu, um anzugeben, dass Standardmäßige Scrollradnachrichten gewünscht sind:


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




