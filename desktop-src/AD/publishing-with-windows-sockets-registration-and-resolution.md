---
title: Veröffentlichung mit Windows Sockets-Registrierungs & Auflösung
description: Windows Sockets-Dienste können die APIs für die Registrierung und Auflösung (RNR) verwenden, um Dienste zu veröffentlichen und mit RNR veröffentlichte Dienste zu suchen.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Windows Sockets-Registrierung und-Auflösung, Veröffentlichung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2019
ms.locfileid: "104472092"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a>Veröffentlichung mit Windows Sockets-Registrierungs & Auflösung

Windows Sockets-Dienste können die APIs für die Registrierung und Auflösung (RNR) verwenden, um Dienste zu veröffentlichen und mit RNR veröffentlichte Dienste zu suchen. Die RNR-Veröffentlichung erfolgt in zwei Schritten. Im ersten Schritt wird eine Dienstklasse installiert, die eine GUID mit einem Namen für den Dienst verknüpft. Die Dienstklasse kann Dienst spezifische Konfigurationsdaten enthalten. Dienste können sich dann selbst als Instanzen der Dienstklasse veröffentlichen. Bei der Veröffentlichung können Clients den Verzeichnisdienst nach Instanzen einer bestimmten Klasse Abfragen, indem Sie die RNR-APIs verwenden und eine Instanz auswählen, an die eine Bindung erfolgen soll. Wenn eine Klasse nicht mehr benötigt wird, kann Sie entfernt werden.

 

 




