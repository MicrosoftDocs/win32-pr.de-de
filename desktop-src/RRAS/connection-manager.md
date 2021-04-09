---
title: Verbindungs-Manager
description: Kunden, die benutzerdefinierte dzer mithilfe der RAS-Dienst-API entwickeln möchten, können den Microsoft-Verbindungs-Manager und das Verbindungs-Manager-Verwaltungskit untersuchen.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038620"
---
# <a name="connection-manager"></a>Verbindungs-Manager

Kunden, die benutzerdefinierte dzer mithilfe der RAS-Dienst-API entwickeln möchten, können den Microsoft-Verbindungs-Manager und das Verbindungs-Manager-Verwaltungskit untersuchen. Der Verbindungs-Manager ist der verwaltete RAS-Client von Microsoft. Dadurch kann ein Administrator ein Remote Zugriffs-Konfigurations Paket erstellen, das an die Remote Benutzer des Administrators verteilt wird. Weitere Informationen zum Verbindungs-Manager und zum Verbindungs-Manager-Verwaltungskit finden Sie in der Online Hilfe für Microsoft Windows 2000 Server und spätere Betriebssysteme.

Sie finden den Quellcode für eine benutzerdefinierte Aktion für einen Verbindungs-Manager im Complete Platform Software Development Kit (SDK). Das Platform SDK kann auf der Microsoft- [Website](https://msdn.microsoft.com/windowsserver/bb980924.aspx)heruntergeladen werden. Nach der Installation lautet der Pfad zum Beispielcode "% Install path% \\ Microsoft SDK \\ Samples \\ netds \\ RAS \\ ConnectionManager", wobei "% Install path%" das Basis Installationsverzeichnis des Platform SDK (z. b. "C: \\ Program Files") angibt.

Benutzerdefinierte Aktionen ermöglichen es dem RAS-Client, bestimmte Aktionen an verschiedenen Punkten im Verbindungsprozess auszuführen. Die im Beispiel gezeigte benutzerdefinierte Aktion passt automatisch die Proxy Serverkonfiguration für eine Verbindung basierend auf der Server Adresse der Verbindung an. Kunden können dieses Beispiel als Ausgangspunkt für das Erstellen eigener benutzerdefinierter Aktionen verwenden.

 

 




