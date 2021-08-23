---
description: Offlineregistrierungsbibliothek
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Offlineregistrierungsbibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed71e617c838d2f12196dd205a9a84dca9d0f9c8e6b27fcf5790bed65d19c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076104"
---
# <a name="offline-registry-library"></a>Offlineregistrierungsbibliothek

## <a name="purpose"></a>Zweck

Die Offlineregistrierungsbibliothek (Offreg.dll) wird verwendet, um eine Registrierungsstruktur außerhalb der aktiven Systemregistrierung zu ändern. Diese Bibliothek ist für Registrierungsupdateszenarien wie die Wartung eines Betriebssystemimages vorgesehen. Die Bibliothek unterstützt Registrierungsstrukturformate ab Windows Vista.

## <a name="developer-audience"></a>Entwicklergruppe

Diese Technologie ist für Originalgerätehersteller (OEMs), Anbieter von Antiviren- und Antischadsoftware sowie für andere Anwendungsentwickler vorgesehen, die Registrierungsstrukturdateien analysieren müssen, ohne sie in die aktive Registrierung laden zu müssen.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Offlineregistrierungsbibliothek wird als binäre verteilbare Dll (Dynamic Link Library) bereitgestellt. Diese Bibliothek wird in den folgenden Versionen von Windows ausgeführt:

<dl> Windows Server 2016  
Windows 10  
Windows 8.1  
Windows Server 2012 R2  
Windows 8  
Windows Server 2012  
Windows 7  
Windows Server 2008 R2  
WindowsServer 2008  
Windows Vista  
</dl>

Anwendungen sollten mithilfe dynamischer Verknüpfungen mit Offreg.dll verknüpft werden.

Offreg.dll wird im Windows Driver Kit (WDK) für Windows 10 und frühere Versionen des Windows Betriebssystems bereitgestellt.

Informationen zum Abrufen des WDK finden Sie unter [How to Get the WDK and the WLK (Abrufen des WDK und des WLK)](/windows-hardware/drivers/download-the-wdk) oder auf der [Msdn-Abonnementwebsite.](https://msdn.microsoft.com/subscriptions/default.aspx)

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**Informationen zur Offlineregistrierungsbibliothek**](about-the-offline-registry-library.md)
-   [**Funktionen der Offlineregistrierungsbibliothek**](offline-registry-library-functions.md)

 

 
