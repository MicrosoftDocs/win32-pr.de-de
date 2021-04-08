---
title: Öffnen und Schließen einer WinSNMP-Anwendung
description: Die WinSNMP-Anwendung muss die SnmpStartup-Funktion erfolgreich aufrufen, bevor Sie eine andere WinSNMP-Funktion aufruft.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f960a22a6155d3f3eeec770af361fac2c0eb036e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037288"
---
# <a name="opening-and-closing-a-winsnmp-application"></a><span data-ttu-id="f0441-103">Öffnen und Schließen einer WinSNMP-Anwendung</span><span class="sxs-lookup"><span data-stu-id="f0441-103">Opening and Closing a WinSNMP Application</span></span>

<span data-ttu-id="f0441-104">Die WinSNMP-Anwendung muss die [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) -Funktion erfolgreich aufrufen, bevor Sie eine andere WinSNMP-Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="f0441-104">The WinSNMP application must call the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function successfully before it calls any other WinSNMP function.</span></span> <span data-ttu-id="f0441-105">Die **SnmpStartup** -Funktion ermöglicht es der Microsoft WinSNMP-Implementierung, Initialisierungs Prozeduren auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f0441-105">The **SnmpStartup** function enables the Microsoft WinSNMP implementation to perform initialization procedures.</span></span> <span data-ttu-id="f0441-106">Die Funktion kehrt auch zur Anwendung der Version der WinSNMP-API zurück, die von der Implementierung unterstützt wird, der Ebene der unterstützten SNMP-Kommunikation und der standardmäßigen Übersetzungs-und Neuübertragungs Modi der Implementierung.</span><span class="sxs-lookup"><span data-stu-id="f0441-106">The function also returns to the application the version of the WinSNMP API that the implementation supports, the level of SNMP communications it supports, and the implementation's default translation and retransmission modes.</span></span>

<span data-ttu-id="f0441-107">Die Anwendung WinSNMP muss die Funktion [**snmpcleanup aufgerufen werden**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) , wenn die Anwendung die Dienste der Implementierung nicht mehr benötigt.</span><span class="sxs-lookup"><span data-stu-id="f0441-107">The WinSNMP application must call the [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) function when the application no longer requires the implementation's services.</span></span> <span data-ttu-id="f0441-108">Obwohl **snmpcleanup** es der Implementierung ermöglicht, alle der Anwendung zugeordneten Ressourcen freizugeben, wird empfohlen, dass die Anwendung zuerst die [**snmpclose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) -Funktion für jede geöffnete WinSNMP-Sitzung aufruft, um die Leistung der Implementierung zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="f0441-108">Even though **SnmpCleanup** enables the implementation to deallocate all resources allocated to the application, it is recommended that the application first call the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function once for each open WinSNMP session, to maximize the implementation's performance.</span></span> <span data-ttu-id="f0441-109">Die WinSNMP-Anwendung muss [**snmpcleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) als letzte WinSNMP-Funktion ausführen, bevor Sie beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f0441-109">The WinSNMP application must call [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) as the last WinSNMP function before it terminates.</span></span>

 

 




