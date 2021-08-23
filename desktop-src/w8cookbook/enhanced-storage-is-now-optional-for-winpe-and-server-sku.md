---
title: Erweiterter Speicher ist jetzt für WINPE und Server-SKU optional
description: Erweiterter Speicher ist jetzt für WINPE und Server-SKU optional
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3777d4df386b071166fcfa17a60654c62e039d9137f73deaf2d85d54e2519e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028848"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a>Erweiterter Speicher ist jetzt für WINPE und Server-SKU optional

## <a name="platforms"></a>Plattformen

**Clients** – Windows 8  
**Server** – Windows Server 2012  


## <a name="description"></a>BESCHREIBUNG

Erweiterter Speicher war immer auf Windows 7 USB-Geräten verfügbar. Mit der Veröffentlichung von Windows 8 ist es für alle Speichergeräte verfügbar. Auf clientbasierten Geräten ist sie standardmäßig aktiviert. auf Servergeräten ist dies optional und muss über Windows Preinstallation Environment (WinPE) bereitgestellt werden.

## <a name="manifestation"></a>Manifestation

Das Servergerät schlägt fehl, wenn erweiterter Speicher nicht aktiviert ist.

Startgeräte müssen über WinPE bereitgestellt werden, wobei dies aktiviert ist.

## <a name="solution"></a>Lösung

Da erweiterter Speicher für Laufzeitserver optional ist, müssen Entwickler ihn winPE für die Bereitstellung und Aktivierung dieser Laufwerke hinzufügen. Weitere Informationen finden Sie im Bereitstellungshandbuch.

Serveradministratoren müssen ihren Server dann explizit für die Verwendung von erweitertem Speicher konfigurieren.

 

 




