---
description: Der Distributed Transaction Coordinator (DTC) ermöglicht verteilte Transaktionen oder Transaktionen, die über mehrere Ressourcen-Manager auf einem oder mehreren Systemen gesteuert werden. KTM und DTC arbeiten zusammen, um dies zu erreichen.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Interoperabilität mit anderen Windows-Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3aeac3d920b408a9a18c32eab83cf747525e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373138"
---
# <a name="interoperability-with-other-windows-features"></a>Interoperabilität mit anderen Windows-Features

Der [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) ermöglicht *verteilte Transaktionen* oder Transaktionen, die über mehrere Ressourcen-Manager auf einem oder mehreren Systemen gesteuert werden. KTM und DTC arbeiten zusammen, um dies zu erreichen.

Com+ macht ein deklaratives Modell für die transaktionale Programmierung verfügbar. Das heißt, der Programmierer deklariert den Umfang, in dem ein Objekt Transaktionen nutzen kann, und die com+-Laufzeit verwaltet die Transaktionen im Auftrag des Objekts. Beispielsweise kann ein Objekt so deklariert werden, dass es nur dann an einer Transaktion teilnimmt, wenn bereits eine Transaktion vorhanden ist, eine Transaktion erforderlich ist (wenn Sie noch nicht vorhanden ist), damit eine neue Transaktion erforderlich ist (eine wird unabhängig davon erstellt, ob bereits eine vorhanden ist) oder nicht transaktional ist. Diese deklarativ verwalteten Transaktionen werden automatisch für Datenbankverbindungen verwendet, die von COM+-Objekten erstellt werden, die im Kontext einer Transaktion ausgeführt werden.

 

 
