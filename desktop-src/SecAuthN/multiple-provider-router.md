---
description: Der Multiple Provider Router (MPR) verarbeitet die Kommunikation zwischen dem Windows Betriebssystem und den installierten Netzwerkanbietern. Sie ermöglicht Windows, dem Benutzer ein integriertes Netzwerk zu präsentieren.
ms.assetid: 3f473273-f696-45f7-afbf-fd55f974ba48
title: Router mit mehreren Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788a6b5dc7ec2db1f75d4bdf7d04df4127e90670b7f798682423dac4567a6fe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786578"
---
# <a name="multiple-provider-router"></a>Router mit mehreren Anbieter

Der [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) verarbeitet die Kommunikation zwischen dem Windows Betriebssystem und den installierten Netzwerkanbietern. Sie ermöglicht Windows, dem Benutzer ein integriertes Netzwerk zu präsentieren.

Wenn der MPR gestartet wird, überprüft er die Registrierung, um zu bestimmen, welche Netzwerkanbieter auf dem System installiert sind und in welcher Reihenfolge sie durchfängt werden sollen. Es lädt alle registrierten Netzwerkanbieter-DLLs und verwendet sie, um nachfolgende WNET-Aufrufe zu verarbeiten, die von der Benutzeroberfläche oder anderen Anwendungen vorgenommen werden.

Weitere Informationen zu WNet-Funktionen finden Sie unter [Windows Netzwerk](../wnet/windows-networking-wnet-.md).

 

 
