---
description: 'Es gibt zwei grundlegende Arten von Netzwerkanwendungen: Transaktions- und Streaminganwendungen. Diese Anwendungstypen werden auch als interaktive Anwendungstypen bzw. Batchverarbeitungsanwendungstypen bezeichnet.'
ms.assetid: 85795cdd-5a4f-4199-98bd-b5ce2299338b
title: Transaktions- und Streaminganwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0e55a21ba552ed768b29b784a557633edfc5734ec266893ede04fded76e538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559496"
---
# <a name="transactional-versus-streaming-applications"></a>Transaktions- und Streaminganwendungen

Es gibt zwei grundlegende Arten von Netzwerkanwendungen: *Transaktions-* und *Streaminganwendungen.* Diese Anwendungstypen werden auch als *interaktive* Anwendungstypen bzw. *Batchverarbeitungsanwendungstypen* bezeichnet.

Transaktionsanwendungen sind Stop-and-Go-Anwendungen. Sie führen in der Regel Anforderungs-/Antwortvorgänge aus, die häufig sortiert werden. Beispiele für Transaktionsanwendungen sind synchrone RPC-Implementierungen (Remote Procedure Call) sowie einige HTTP- und dns-Implementierungen (Domain Name System).

Streaminganwendungen verschieben Daten. Um Streaminganwendungen mit einem parallelen Begriff zu beschreiben, halten sich Streaminganwendungen an eine Philosophie der Datenübertragung zwischen Denk- und Metal-Datenübertragungen, in der Regel mit wenig Bedenken hinsichtlich der Datenreihenfolge. Beispiele für Streaminganwendungen sind Netzwerksicherung und FTP (File Transfer Protocol).

Sobald der Anwendungstyp bestimmt ist, werden auch dessen Netzwerk- und Protokollmerkmale bestimmt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hochleistungsanwendungen für Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Leistungsdimensionen](performance-dimensions-2.md)
</dt> </dl>

 

 



