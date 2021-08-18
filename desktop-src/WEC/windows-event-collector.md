---
title: Windows-Ereignissammlung
description: Sie können das Empfangen und Speichern von Ereignissen auf einem lokalen Computer (Ereignissammler) abonnieren, die von einem Remotecomputer (Ereignisquelle) weitergeleitet werden.
ms.assetid: 7725e06d-4df1-4b3e-9f2f-2b8bdd805cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efa767ecb80960fc3461380435ea1d44992656d7c67df990574f7155ee976fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997880"
---
# <a name="windows-event-collector"></a>Windows-Ereignissammlung

Sie können das Empfangen und Speichern von Ereignissen auf einem lokalen Computer (Ereignissammler) abonnieren, die von einem Remotecomputer (Ereignisquelle) weitergeleitet werden. Die [Windows Event Collector-Funktionen](windows-event-collector-functions.md) unterstützen das Abonnieren von Ereignissen mithilfe des WS-Management Protokolls. Weitere Informationen zur WS-Verwaltung finden Sie unter [Informationen Windows Remoteverwaltung.](/windows/desktop/WinRM/about-windows-remote-management)

## <a name="event-forwarding-and-event-collection-architecture"></a>Ereignisweiterleitung und Ereignissammlungsarchitektur

Mit der Ereignissammlung können Administratoren Ereignisse von Remotecomputern abrufen und in einem lokalen Ereignisprotokoll auf dem Collectorcomputer speichern. Der Zielprotokollpfad für die Ereignisse ist eine Eigenschaft des Abonnements. Alle Daten im weitergeleiteten Ereignis werden im Ereignisprotokoll des Collectorcomputers gespeichert (keine der Informationen geht verloren). Dem Ereignis werden auch zusätzliche Informationen zur Ereignisweiterleitung hinzugefügt. Weitere Informationen zum Aktivieren eines Computers zum Empfangen von gesammelten Ereignissen oder Weiterleiten von Ereignissen finden Sie unter [Konfigurieren von Computern zum Weiterleiten und Sammeln von Ereignissen.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))

## <a name="subscriptions"></a>Abonnements

In der folgenden Liste werden die Typen von Ereignisabonnements beschrieben:

-   Von der Quelle initiierte Abonnements: Ermöglicht es Ihnen, ein Ereignisabonnement auf einem Ereignissammlercomputer zu definieren, ohne die Ereignisquellcomputer zu definieren. Anschließend können mehrere Remoteereignisquellcomputer (mithilfe einer Gruppenrichtlinieneinstellung) eingerichtet werden, um Ereignisse an den Ereignissammlercomputer weiterzuleiten. Weitere Informationen finden Sie unter [Einrichten eines quellinitiiertes Abonnement.](setting-up-a-source-initiated-subscription.md) Dieser Abonnementtyp ist nützlich, wenn Sie nicht wissen oder nicht alle Ereignisquellencomputer angeben möchten, die Ereignisse weiterleiten.
-   Vom Collector initiierte Abonnements: Ermöglicht ihnen das Erstellen eines Ereignisabonnements, wenn Sie alle Ereignisquellcomputer kennen, die Ereignisse weiterleiten. Sie geben alle Ereignisquellen zum Zeitpunkt der Erstellung des Abonnements an. Weitere Informationen finden Sie unter [Erstellen eines collector-initiierten Abonnements.](creating-an-event-collector-subscription.md)

## <a name="windows-event-collector-functions"></a>Windows Ereignissammlerfunktionen

Weitere Informationen und Codebeispiele, die die Event Collector-Funktionen verwenden, finden Sie unter [Verwenden von Windows Event Collector.](using-windows-event-collector.md)

Weitere Informationen zu den Funktionen, die zum Sammeln und Weiterleiten von Ereignissen verwendet werden, finden Sie unter [Windows Event Collector-Funktionen.](windows-event-collector-functions.md)

 

 