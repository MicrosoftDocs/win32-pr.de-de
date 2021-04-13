---
title: Schreiben von WinSNMP-Anwendungen mit mehreren Threads
description: Die Microsoft WinSNMP-Implementierung stellt sicher, dass die WinSNMP-Vorgänge eines Prozesses nicht die WinSNMP-Einstellungen eines anderen Prozesses ändern.
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb6b7991968c5c5efafa898758c3c60cad1abb2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390623"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a><span data-ttu-id="0a24b-103">Schreiben von WinSNMP-Anwendungen mit mehreren Threads</span><span class="sxs-lookup"><span data-stu-id="0a24b-103">Writing WinSNMP Applications with Multiple Threads</span></span>

<span data-ttu-id="0a24b-104">Die Microsoft WinSNMP-Implementierung stellt sicher, dass die WinSNMP-Vorgänge eines Prozesses nicht die WinSNMP-Einstellungen eines anderen Prozesses ändern.</span><span class="sxs-lookup"><span data-stu-id="0a24b-104">The Microsoft WinSNMP implementation ensures that the WinSNMP operations of one process do not modify the WinSNMP settings of another process.</span></span>

<span data-ttu-id="0a24b-105">Eine WinSNMP-Anwendung mit mehreren Threads muss sicherstellen, dass WinSNMP-Vorgänge, mit denen Parameter auf Anwendungsebene festgelegt werden, Thread sicher sind.</span><span class="sxs-lookup"><span data-stu-id="0a24b-105">A WinSNMP application with multiple threads must ensure that WinSNMP operations that set application-level parameters are thread-safe.</span></span> <span data-ttu-id="0a24b-106">Die Funktionen, mit denen Parameter auf Anwendungsebene festgelegt werden, sind [**snmpsettranslatemode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) und [**snmpsetretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode).</span><span class="sxs-lookup"><span data-stu-id="0a24b-106">The functions that set application-level parameters are [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) and [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode).</span></span> <span data-ttu-id="0a24b-107">Diese Funktionen ändern Einstellungen für den Entitäts-und Kontext Übersetzungsmodus und den Modus für Neuübertragungen.</span><span class="sxs-lookup"><span data-stu-id="0a24b-107">These functions modify settings for the entity and context translation mode and the retransmission mode.</span></span>

<span data-ttu-id="0a24b-108">Weitere Informationen finden Sie unter [mehrere Threads](/windows/desktop/ProcThread/multiple-threads) und [Thread Sicherheit und Zugriffsrechte](/windows/desktop/ProcThread/thread-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="0a24b-108">For more information, see [Multiple Threads](/windows/desktop/ProcThread/multiple-threads) and [Thread Security and Access Rights](/windows/desktop/ProcThread/thread-security-and-access-rights).</span></span>

 

 