---
description: Windows Sockets 2 bietet einen erweiterten Satz von Vorgängen, die für das Herstellen einer Socketverbindung Coincident auftreten können. Die Dienstanbieter Anforderungen für die Implementierung dieser Features werden im folgenden beschrieben.
ms.assetid: fbc7055e-ea25-4d17-8039-f0fef300353c
title: Erweiterte Funktionalität zur Verbindungszeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33c6d7ee928fe7e97f535363e9e842285eef7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129200"
---
# <a name="enhanced-functionality-at-connect-time"></a>Erweiterte Funktionalität zur Verbindungszeit

Windows Sockets 2 bietet einen erweiterten Satz von Vorgängen, die für das Herstellen einer Socketverbindung Coincident auftreten können. Die Dienstanbieter Anforderungen für die Implementierung dieser Features werden im folgenden beschrieben.

## <a name="conditional-acceptance"></a>Bedingte Annahme

Wie bereits beschrieben, ruft [**wspaccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) eine vom Client bereitgestellte Bedingungs Funktion auf, die Eingabeparameter verwendet, um Informationen über die ausstehende Verbindungsanforderung bereitzustellen. Diese Informationen können vom Client verwendet werden, um eine Verbindungsanforderung auf der Grundlage von Aufruferinformationen wie Aufrufer-ID, QoS usw. anzunehmen oder abzulehnen. Wenn die Bedingungs Funktion "CF Accept" zurückgibt \_ , wird ein neuer Socket mit denselben Eigenschaften wie der Abhör Socket erstellt, und ein Handle für den neuen Socket wird zurückgegeben. Wenn die Bedingungs Funktion CF ablehnen zurückgibt \_ , sollte die Verbindungsanforderung abgelehnt werden. Wenn die Bedingungs Funktion CF-zurückstellen zurückgibt \_ , kann die Annahme/Ablehnung-Entscheidung nicht sofort erfolgen, und der Dienstanbieter muss die Verbindungsanforderung für die Warteschlangen Warteschlange belassen. Der Client muss **wspaccept** erneut anrufen, wenn er bereit ist, eine Entscheidung zu treffen, und anordnen, dass die Bedingungs Funktion entweder CF \_ Accept oder CF ablehnen zurückgibt \_ . Während eine verzögerte Verbindungsanforderung am Anfang der Warteschlange für Rückstand liegt, gibt der Dienstanbieter keine weiteren Hinweise für ausstehende Verbindungsanforderungen aus.

## <a name="exchanging-user-data-at-connect-time"></a>Austauschen von Benutzerdaten zum Verbindungs Zeitpunkt

Einige Protokolle ermöglichen das Austauschen einer kleinen Menge von Benutzerdaten zur Verbindungszeit. Wenn solche Daten vom Verbindungs Host empfangen wurden, werden Sie in einen Dienstanbieter Puffer eingefügt, und ein Zeiger auf diesen Puffer zusammen mit einem Längen Wert wird über Eingabeparameter für die [**wspaccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) -Bedingungs Funktion an den Winsock-SPI-Client übermittelt. Wenn der Winsock-SPI-Client Antwortdaten aufweist, um zum Verbindungs Host zurückzukehren, kann er diesen in einen Puffer kopieren, der vom Dienstanbieter bereitgestellt wird. Ein Zeiger auf diesen Puffer und eine ganze Zahl, die angibt, dass die Puffergröße auch als Eingabeparameter für die Bedingungs Funktion bereitgestellt wird (sofern vom Protokoll unterstützt).

## <a name="establishing-socket-groups"></a>Einrichten von socketgruppen

Die Verwendung von socketgruppen ist reserviert.

 

 



