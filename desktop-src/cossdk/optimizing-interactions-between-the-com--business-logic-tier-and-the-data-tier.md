---
description: Die Datenebene enthält häufig überwiegend statische Informationen&\# 8212; Informationen, die auf permanenten Medien beibehalten werden.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Optimieren von Aufrufen zwischen der com+-Geschäftslogik und den Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345434"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a>Optimieren von Interaktionen zwischen der com+-Geschäftslogik Ebene und der Datenebene

Die Datenebene enthält häufig überwiegend statische Informationen – Informationen, die auf permanenten Medien beibehalten werden. Da diese Ebene Informationen umfasst, die überwiegend statisch sind, ist eine gründliche Analyse von möglichen Engpässen erforderlich. Neben der offensichtlichen Möglichkeit von Verbindungs Engpässen können auch Hotspots durch häufig verwendete Datensätze, ineffiziente Datenzugriffs Methoden und die Notwendigkeit, den Zugriff auf Legacy Systeme zu koordinieren, verursacht werden.

## <a name="connecting-to-the-data-tier"></a>Herstellen einer Verbindung mit der Datenebene

Zwei Aspekte spielen eine wichtige Rolle beim Entwerfen einer Datenebene für eine COM+-Anwendung: Verbindungspooling und [com+-Just-in-time (JIT)-Aktivierung](com--just-in-time-activation.md)und die Verwendung von DSNs. Komponenten, die Verbindungen mit der Datenebene herstellen, sollten das [com+-Objekt Pooling](com--object-pooling.md) verwenden, das für die Komponente festgelegt ist.

Verwenden Sie beim Erstellen von DSNs für die Komponente angegebene objektkonstruktorzeichenfolgen, anstatt einen Datei-DSN zu erstellen. Datei-DSNs sind langsamer als eine Verbindung mithilfe einer Objektkonstruktorzeichenfolge. Objektkonstruktorzeichenfolgen können auf dem Eigenschaften Blatt der Komponente angegeben werden. Weitere Informationen finden Sie unter [com+-objektkonstruktorzeichenfolgen](com--object-constructor-strings.md).

Wenn Sie Komponenten verwenden, um auf eine SQL Server Datenbank zuzugreifen, verwenden Sie das COM+-Objekt Pooling anstelle von SQL-Verbindungspooling.

Wenn die Komponente ADO zum Abrufen mehrerer Recordsets verwendet, richten Sie mehrere Verbindungen für die Komponente ein. Wenn ADO mehrere Recordsets abruft, werden mehrere Verbindungen im Hintergrund erstellt, wenn Sie nicht erstellt werden. Wenn Sie Sie erstellen, können Sie Sie in einem Pool zusammenführen und mehr Kontrolle über die Anzahl der verwendeten Verbindungen erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Optimieren von Interaktionen zwischen der com+-Geschäftslogik Ebene und der Präsentationsebene](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



