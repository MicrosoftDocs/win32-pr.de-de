---
title: Veröffentlichen mit Windows Sockets Registration & Resolution
description: Windows Sockets-Dienste können die Registrierungs- und Auflösungs-APIs (RnR) verwenden, um Dienste zu veröffentlichen und mit RnR veröffentlichte Dienste zu suchen.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Windows Sockets Registration and Resolution AD , Publishing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a071a37d1d017e4c034f3eaab175889fdfcd1789d9f48aeac2c2943dfc8b4f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184924"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a>Veröffentlichen mit Windows Sockets Registration & Resolution

Windows Sockets-Dienste können die Registrierungs- und Auflösungs-APIs (RnR) verwenden, um Dienste zu veröffentlichen und mit RnR veröffentlichte Dienste zu suchen. Die RnR-Veröffentlichung erfolgt in zwei Schritten. Im ersten Schritt wird eine Dienstklasse installiert, die eine GUID einem Namen für den Dienst zugeordnet. Die Dienstklasse kann dienstspezifische Konfigurationsdaten enthalten. Dienste können sich dann selbst als Instanzen der Dienstklasse veröffentlichen. Nach der Veröffentlichung können Clients den Verzeichnisdienst mithilfe der RnR-APIs nach Instanzen einer bestimmten Klasse abfragen und eine Instanz auswählen, an die eine Bindung erfolgen soll. Wenn eine Klasse nicht mehr benötigt wird, kann sie entfernt werden.

 

 




