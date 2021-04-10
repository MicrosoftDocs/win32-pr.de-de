---
description: HKLM \\ Software \\ Microsoft \\ MSSQLSERVER- \\ Client.
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041405"
---
# <a name="connectto"></a>ConnectTo

**HKLM \\ Software \\ Microsoft \\ MSSQLSERVER- \\ Client**

## <a name="description"></a>BESCHREIBUNG

Der **ConnectTo** -Unterschlüssel speichert Verbindungsinformationen für Windows-basierte Clients, die eine Verbindung mit Instanzen der Microsoft SQL Server Datenbank-Engine herstellen. Registrierungseinträge in diesem Unterschlüssel sind vom Datentyp reg \_ SZ, und ihre Werte geben die Net-Library an, die zum Herstellen einer Verbindung mit der Instanz verwendet werden sollen, sowie Netzwerk spezifische Parameter.

Die in diesem Unterschlüssel gespeicherten Verbindungsinformationen werden vom OLE DB Anbieter für SQL Server, dem SQL Server ODBC-Treiber oder dem SQL Server DB-Library Dynamic Link Library (dll) gelesen.

## <a name="change-method"></a>Methode ändern

Sie sollten die Einträge in diesem Unterschlüssel nicht mithilfe des Registrierungs-Editors ändern. Verwenden Sie das Netzwerk Hilfsprogramm SQL Server Client, um den Server Namen und die Verbindungsinformationen zu konfigurieren. Weitere Anweisungen finden Sie unter SQL Server Hilfe zum Client Netzwerk Hilfsprogramm.

## <a name="notes"></a>Notizen

-   Der Unterschlüssel **ConnectTo** wird vom OLE DB Anbieter für SQL Server, vom SQL Server ODBC-Treiber und von der SQL Server DB-Library dll verwendet. Einträge in diesem Unterschlüssel identifizieren, welche Net-Library diese Datenzugriffs-API-Komponenten aufrufen.
-   Net-Libraries sind SQL Server Komponenten, die die Datenzugriffs-API-Komponenten vor den Details der Verwendung verschiedener IPC-Methoden (Interprocess Communication) verwenden, um mit einem instanzess des SQL Server Datenbank-Engine zu kommunizieren.
-   Das nicht ordnungsgemäße Aktualisieren des **ConnectTo** -unter Schlüssels verhindert möglicherweise, dass Anwendungen eine Verbindung mit einer Instanz der SQL Server Datenbank-Engine herstellen.

 

 



