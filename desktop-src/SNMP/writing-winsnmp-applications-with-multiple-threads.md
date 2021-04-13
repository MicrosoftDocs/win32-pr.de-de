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
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>Schreiben von WinSNMP-Anwendungen mit mehreren Threads

Die Microsoft WinSNMP-Implementierung stellt sicher, dass die WinSNMP-Vorgänge eines Prozesses nicht die WinSNMP-Einstellungen eines anderen Prozesses ändern.

Eine WinSNMP-Anwendung mit mehreren Threads muss sicherstellen, dass WinSNMP-Vorgänge, mit denen Parameter auf Anwendungsebene festgelegt werden, Thread sicher sind. Die Funktionen, mit denen Parameter auf Anwendungsebene festgelegt werden, sind [**snmpsettranslatemode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) und [**snmpsetretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode). Diese Funktionen ändern Einstellungen für den Entitäts-und Kontext Übersetzungsmodus und den Modus für Neuübertragungen.

Weitere Informationen finden Sie unter [mehrere Threads](/windows/desktop/ProcThread/multiple-threads) und [Thread Sicherheit und Zugriffsrechte](/windows/desktop/ProcThread/thread-security-and-access-rights).

 

 