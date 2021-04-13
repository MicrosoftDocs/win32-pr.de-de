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
# <a name="windows-precision-touchpad-devices"></a><span data-ttu-id="bb603-103">Touchpad-Geräte mit Windows Precision</span><span class="sxs-lookup"><span data-stu-id="bb603-103">Windows precision touchpad devices</span></span>

## <a name="platforms"></a><span data-ttu-id="bb603-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="bb603-104">Platforms</span></span>

<dl> <span data-ttu-id="bb603-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bb603-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="bb603-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb603-106">Description</span></span>

<span data-ttu-id="bb603-107">Das Windows Precision Touchpad ist eine neue Klasse von Eingabegeräten, die Zeiger Eingabe-und Gesten Funktionen mit hoher Genauigkeit bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bb603-107">The Windows Precision Touchpad is a new class of input devices that provide high precision pointer input and gesture functionality.</span></span> <span data-ttu-id="bb603-108">Standardmäßig generieren diese Geräte bei der Nutzung von Desktop Anwendungen eine Bild Lauf radnachricht mit hoher Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="bb603-108">By default, these devices generate ultra-high precision scroll wheel messages for desktop application consumption.</span></span>

## <a name="manifestations"></a><span data-ttu-id="bb603-109">Kundgebungen</span><span class="sxs-lookup"><span data-stu-id="bb603-109">Manifestations</span></span>

<span data-ttu-id="bb603-110">Anwendungen, die nicht für das Verarbeiten von Bild Lauf radnachrichten mit hoher Genauigkeit konzipiert sind, können entweder über Scrollen oder nicht ordnungsgemäß scrollen.</span><span class="sxs-lookup"><span data-stu-id="bb603-110">Applications that are not designed to handle ultra-high precision scroll wheel messages may either over-scroll or not scroll correctly.</span></span>

## <a name="mitigation"></a><span data-ttu-id="bb603-111">Minderung</span><span class="sxs-lookup"><span data-stu-id="bb603-111">Mitigation</span></span>

<span data-ttu-id="bb603-112">Anwendungsentwickler sollten das Bild Lauf Delta in Mausrad-Nachrichten betrachten und ihre apps entsprechend ändern. in der Zwischenzeit kann eine Anwendung jedoch die Schiebe radnachrichten mit hoher Genauigkeit (Delta = 1) abwählen und sich für das Empfangen von Schiebe radnachrichten mit hoher Genauigkeit (Delta = 40) oder Standard-Scrollrad-Nachrichten entscheiden (Delta = 120).</span><span class="sxs-lookup"><span data-stu-id="bb603-112">Application developers should look at the scroll delta in mouse scroll wheel messages and modify their apps accordingly; however, in the interim an application may opt-out of ultra-high precision scroll wheel messages (delta = 1)and elect to receive high precision scroll wheel messages (delta = 40) or standard scroll wheel messages (delta = 120).</span></span>

## <a name="solution"></a><span data-ttu-id="bb603-113">Lösung</span><span class="sxs-lookup"><span data-stu-id="bb603-113">Solution</span></span>

<span data-ttu-id="bb603-114">Wenn die Anwendung in der Lage ist, Bild Lauf radnachrichten mit hoher Genauigkeit zu verarbeiten, muss nichts durchgeführt werden, da dies die von Windows Precision Touchpads gesendete Standardmeldung ist.</span><span class="sxs-lookup"><span data-stu-id="bb603-114">If the application is capable of handling ultra-high precision scroll wheel messages, nothing needs to be done as this is the default message sent by Windows Precision Touchpads.</span></span>

<span data-ttu-id="bb603-115">Wenn die Anwendung in der Lage ist, Nachrichten mit hoher Genauigkeit, aber nicht mit ultrahohem Genauigkeits Grad zu verarbeiten, fügen Sie dem Anwendungs Manifest Folgendes hinzu:</span><span class="sxs-lookup"><span data-stu-id="bb603-115">If the application is capable of handling high precision scroll wheel messages, but not ultra-high precision wheel messages, add the following to the application manifest:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <highResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">true</highResolutionScrollingAware>  
  </windowsSettings>  
</application>  
```



<span data-ttu-id="bb603-116">Wenn die Anwendung keine Bild Lauf radnachrichten mit hoher Genauigkeit oder mit extrem hoher Genauigkeit verarbeiten kann, fügen Sie dem Anwendungs Manifest Folgendes hinzu, um anzugeben, dass standardmäßige Scrollrad Meldungen gewünscht werden sollen:</span><span class="sxs-lookup"><span data-stu-id="bb603-116">If the application is not capable of handling either high precision scroll wheel messages or ultra-high precision wheel messages, add the following to the application manifest to indicate that standard scroll wheel messages are desired:</span></span>


```
<application xmlns="urn:schemas-microsoft-com:asm.v3">  
    <windowsSettings>  
      <ultraHighResolutionScrollingAware xmlns="http://schemas.microsoft.com/SMI/2013/WindowsSettings">false</ultraHighResolutionScrollingAware >  
  </windowsSettings>  
</application>  
```



 

 




