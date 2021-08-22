---
description: Der Distributed Transaction Coordinator (DTC) ermöglicht verteilte Transaktionen oder Transaktionen, die von mehreren Ressourcen-Managern auf einem oder mehreren Systemen kontrolliert werden. KTM und DTC arbeiten eng zusammen, um dies zu erreichen.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Interoperabilität mit anderen Windows Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18595140676539c6e5acaa5fc62835ac279215d068834e3e56dffe50d01e0e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119265070"
---
# <a name="interoperability-with-other-windows-features"></a>Interoperabilität mit anderen Windows Funktionen

Der [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) ermöglicht verteilte Transaktionen oder Transaktionen, die unter der Kontrolle mehrerer Ressourcen-Manager auf einem oder mehreren Systemen stehen. KTM und DTC arbeiten eng zusammen, um dies zu erreichen.

COM+ macht ein deklaratives Modell für die Transaktionsprogrammierung verfügbar. Anders ausgedrückt: Der Programmierer deklariert das Ausmaß, in dem ein Objekt Transaktionen nutzen kann, und die COM+-Laufzeit verwaltet die Transaktionen im Namen des Objekts. Beispielsweise kann ein Objekt so deklariert werden, dass es nur dann an einer Transaktion teilzunehmen kann, wenn bereits eine vorhanden ist, eine Transaktion erforderlich ist (eine wird erstellt, wenn sie noch nicht vorhanden ist), eine neue Transaktion erforderlich ist (eine wird unabhängig davon erstellt, ob bereits eine vorhanden ist) oder keine Transaktion. Diese deklarativ verwalteten Transaktionen werden automatisch für Datenbankverbindungen verwendet, die von COM+-Objekten erstellt werden, die im Kontext einer Transaktion ausgeführt werden.

 

 
