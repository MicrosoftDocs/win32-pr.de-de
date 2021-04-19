---
title: Windows-Ereignissammlung
description: Sie können das empfangen und Speichern von Ereignissen auf einem lokalen Computer (Ereignis Sammler) abonnieren, die von einem Remote Computer (Ereignis Quelle) weitergeleitet werden.
ms.assetid: 7725e06d-4df1-4b3e-9f2f-2b8bdd805cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c4ef9e0cb647236daa55771222f25b7e0e370ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341525"
---
# <a name="windows-event-collector"></a>Windows-Ereignissammlung

Sie können das empfangen und Speichern von Ereignissen auf einem lokalen Computer (Ereignis Sammler) abonnieren, die von einem Remote Computer (Ereignis Quelle) weitergeleitet werden. Die [Windows-Ereignis Sammler Funktionen](windows-event-collector-functions.md) unterstützen das Abonnieren von Ereignissen mithilfe des WS-Management Protokolls. Weitere Informationen zur WS-Verwaltung finden Sie unter [Informationen zu Windows-Remoteverwaltung](/windows/desktop/WinRM/about-windows-remote-management).

## <a name="event-forwarding-and-event-collection-architecture"></a>Architektur der Ereignis Weiterleitung und Ereignis Sammlung

Mithilfe der Ereignis Sammlung können Administratoren Ereignisse von Remote Computern erhalten und in einem lokalen Ereignisprotokoll auf dem Collector-Computer speichern. Der Ziel Protokoll Pfad für die Ereignisse ist eine Eigenschaft des Abonnements. Alle Daten im weitergeleiteten Ereignis werden im Ereignisprotokoll des Sammlungs Computers gespeichert (keine der Informationen geht verloren). Weitere Informationen zur Ereignis Weiterleitung werden dem Ereignis ebenfalls hinzugefügt. Weitere Informationen zum Aktivieren eines Computers für das Empfangen von gesammelten Ereignissen oder zum Weiterleiten von Ereignissen finden Sie unter [Konfigurieren von Computern zum Weiterleiten und sammeln](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))von Ereignissen.

## <a name="subscriptions"></a>Abonnements

In der folgenden Liste werden die Arten von Ereignis Abonnements beschrieben:

-   Von der Quelle initiierte Abonnements: Hiermit können Sie ein Ereignis Abonnement auf einem Ereignis Sammler Computer definieren, ohne die Ereignis Quellcomputer zu definieren. Mehrere Remote Ereignis Quellcomputer können dann (mithilfe einer Gruppenrichtlinien Einstellung) zum Weiterleiten von Ereignissen an den Ereignis Sammler Computer eingerichtet werden. Weitere Informationen finden Sie unter [Einrichten eines von der Quelle initiierten Abonnements](setting-up-a-source-initiated-subscription.md). Dieser Abonnementtyp ist nützlich, wenn Sie nicht wissen oder nicht alle Ereignis Quellen angeben möchten, die Ereignisse weiterleiten.
-   Vom Collector initiierte Abonnements: ermöglicht Ihnen das Erstellen eines Ereignis Abonnements, wenn Sie alle Ereignis Quellcomputer kennen, die Ereignisse weiterleiten. Sie geben alle Ereignis Quellen zum Zeitpunkt der Erstellung des Abonnements an. Weitere Informationen finden Sie unter [Erstellen eines vom Collector initiierten Abonnements](creating-an-event-collector-subscription.md).

## <a name="windows-event-collector-functions"></a>Funktionen der Windows-Ereignis Sammlung

Weitere Informationen und Codebeispiele, in denen die Funktionen des Ereignis Sammlers verwendet werden, finden [Sie unter Verwenden der Windows-Ereignis](using-windows-event-collector.md)Sammlung.

Weitere Informationen zu den Funktionen, die zum Erfassen und Weiterleiten von Ereignissen verwendet werden, finden Sie unter [Windows-Ereignis Sammler Funktionen](windows-event-collector-functions.md).

 

 