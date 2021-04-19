---
description: .
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Offline-Registrierungs Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a473bde729a0047a56d7ad0fdec1c0e3133ea103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345425"
---
# <a name="offline-registry-library"></a>Offline-Registrierungs Bibliothek

## <a name="purpose"></a>Zweck

Die Offline Registrierungs Bibliothek (Offreg.dll) wird verwendet, um eine Registrierungs Struktur außerhalb der aktiven Systemregistrierung zu ändern. Diese Bibliothek ist für Registrierungs Aktualisierungs Szenarien wie die Wartung eines Betriebssystem Abbilds vorgesehen. Die Bibliothek unterstützt Registrierungs Struktur Formate ab Windows Vista.

## <a name="developer-audience"></a>Entwicklergruppe

Diese Technologie ist für Originalgerätehersteller (OEMs), Antiviren-und antischadsoftwarehersteller und andere Anwendungsentwickler gedacht, die in der Lage sein müssen, Registrierungs-Hive-Dateien zu analysieren, ohne Sie in die aktive Registrierung zu laden.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Offline Registrierungs Bibliothek wird als binäre verteilbare dll (Dynamic-Link Library) bereitgestellt. Diese Bibliothek wird unter den folgenden Versionen von Windows ausgeführt:

<dl> Windows Server 2016  
Windows 10  
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

Offreg.dll wird im Windows-Treiberkit (WDK) für Windows 10 und frühere Versionen des Windows-Betriebssystems bereitgestellt.

Weitere Informationen zum Abrufen des WDK finden Sie unter Abrufen [des WDK und der WLK](/windows-hardware/drivers/download-the-wdk) , oder besuchen Sie die Website für [MSDN-Abonnements](https://msdn.microsoft.com/subscriptions/default.aspx) .

## <a name="in-this-section"></a>In diesem Abschnitt

-   [**Informationen zur Offline Registrierungs Bibliothek**](about-the-offline-registry-library.md)
-   [**Funktionen der Offline-Registrierungs Bibliothek**](offline-registry-library-functions.md)

 

 
