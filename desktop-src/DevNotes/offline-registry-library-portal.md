---
description: Offlineregistrierungsbibliothek
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Offlineregistrierungsbibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1aa5acdd7904516608413ff973e60e81c296c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089248"
---
# <a name="offline-registry-library"></a>Offlineregistrierungsbibliothek

## <a name="purpose"></a>Zweck

Die Offlineregistrierungsbibliothek (Offreg.dll) wird verwendet, um eine Registrierungsstruktur außerhalb der aktiven Systemregistrierung zu ändern. Diese Bibliothek ist für Registrierungsupdateszenarien wie die Wartung eines Betriebssystemimages vorgesehen. Die Bibliothek unterstützt Registrierungsstrukturformate ab Windows Vista.

## <a name="developer-audience"></a>Entwicklergruppe

Diese Technologie ist für Originalgerätehersteller (OEMs), Anbieter von Antiviren- und Antischadsoftware sowie für andere Anwendungsentwickler vorgesehen, die Registrierungsstrukturdateien analysieren müssen, ohne sie in die aktive Registrierung laden zu müssen.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Offlineregistrierungsbibliothek wird als binäre verteilbare Dll (Dynamic Link Library) bereitgestellt. Diese Bibliothek wird unter den folgenden Versionen von Windows ausgeführt:

<dl> Windows Server 2016  
Windows 10  
Windows 8.1  
Windows Server 2012 R2  
Windows 8  
Windows Server 2012  
Windows 7  
Windows Server 2008 R2  
WindowsServer 2008  
Windows Vista  
</dl>

Anwendungen sollten mithilfe dynamischer Verknüpfungen mit Offreg.dll verknüpft werden.

Offreg.dll wird im Windows-Treiberkit (WDK) für Windows 10 und frühere Versionen des Windows-Betriebssystems bereitgestellt.

Informationen zum Abrufen des WDK finden Sie unter [How to Get the WDK and the WLK (Abrufen des WDK und des WLK)](/windows-hardware/drivers/download-the-wdk) oder auf der [MSDN-Abonnementwebsite.](https://msdn.microsoft.com/subscriptions/default.aspx)

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**Informationen zur Offlineregistrierungsbibliothek**](about-the-offline-registry-library.md)
-   [**Funktionen der Offlineregistrierungsbibliothek**](offline-registry-library-functions.md)

 

 
