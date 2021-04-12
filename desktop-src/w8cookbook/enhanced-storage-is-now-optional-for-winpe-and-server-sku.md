---
title: Erweiterter Speicher ist jetzt für die WinPE-und Server-SKU optional.
description: Erweiterter Speicher ist jetzt für die WinPE-und Server-SKU optional.
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7601ee35e6d4be35a39874dd85650f051c1c718
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104316598"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a>Erweiterter Speicher ist jetzt für die WinPE-und Server-SKU optional.

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Erweiterter Speicher war immer auf Windows 7-USB-Geräten verfügbar. Mit der Veröffentlichung von Windows 8 ist es für alle Speichergeräte verfügbar. In Client basierten Geräten ist es standardmäßig aktiviert. auf Server Geräten ist es optional und muss über Windows Preinstallation Environment (WinPE) bereitgestellt werden.

## <a name="manifestation"></a>Ausstrahlung

Das Server Gerät schlägt fehl, wenn der erweiterte Speicher nicht aktiviert ist.

Start Geräte müssen mithilfe von WinPE bereitgestellt werden, wenn diese Option aktiviert ist.

## <a name="solution"></a>Lösung

Da der erweiterte Speicher für den Lauf Zeitserver optional ist, müssen Entwickler ihn zur Bereitstellung und Aktivierung dieser Laufwerke zu WinPE hinzufügen. Weitere Informationen finden Sie im Bereitstellungs Handbuch.

Server Administratoren müssen dann Ihren Server explizit für die Verwendung von erweitertem Speicher konfigurieren.

 

 




