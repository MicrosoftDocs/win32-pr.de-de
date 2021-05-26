---
title: Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
description: Mit dem intelligenten Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS) werden Dateien zwischen einem Client und einem Server übertragen (Downloads oder Uploads). Dabei werden Statusinformationen zu den Übertragungsvorgängen angezeigt.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
- Background Intelligent Transfer Service, Startseite
- BITS (siehe Background Intelligent Transfer Service)
- Herunterladen von Dateien BITS
- Bits für die Hintergrunddateiübertragung
- Hochladen von Dateien mit BITS
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 9483e297e8b48ad6466846c7eceb8d53b57d3278
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424210"
---
# <a name="background-intelligent-transfer-service"></a>Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)

## <a name="purpose"></a>Zweck

Background Intelligent Transfer Service (BITS) wird von Programmierern und Systemadministratoren verwendet, um Dateien von HTTP-Webservern und SMB-Dateifreigaben herunterzuladen oder auf diese hochzuladen. BITS berücksichtigt die Kosten der Übertragung sowie die Netzwerknutzung, sodass die Vordergrundarbeit des Benutzers so wenig Auswirkungen wie möglich hat. BITS verarbeitet auch Netzwerküberlagerungen, wobei Übertragungen auch nach einem Neustart angehalten und automatisch fortgesetzt werden. BITS enthält PowerShell-Cmdlets zum Erstellen und Verwalten von Übertragungen sowie das Befehlszeilenprogramm BitsAdmin.

> [!Note]  
> BITS kann von Windows verwendet werden, um Updates auf Ihr lokales System herunterzuladen. Wenn Sie ein Endbenutzer sind, der nach Möglichkeiten zur Problembehandlung ihrer BITS-Installation sucht, finden Sie weitere Informationen unter [Beheben Windows Update Probleme.](https://support.microsoft.com/help/10164/fix-windows-update-errors) 
 

## <a name="where-applicable"></a>Anwendungsbereich

Verwenden Sie BITS für Anwendungen, die:

-   Laden Sie Dateien von einem HTTP-, REST-Webserver oder SMB-Dateiserver herunter, oder laden Sie sie hoch.
-   Automatisches Fortsetzen von Dateiübertragungen, nachdem die Netzwerkverbindung getrennt und der Computer neu gestartet wurde.
-   Beibehalten der Reaktionsfähigkeit anderer Netzwerkanwendungen.
-   Berücksichtigen Sie die Netzwerkkosten für z. B. Roamingnetzwerke.
-   Arbeiten Sie optional mit [BranchCache,](/windows-server/networking/branchcache/branchcache) um WAN-Datenverkehr (Wide Area Network) zu optimieren.

## <a name="developer-audience"></a>Entwicklergruppe

BITS ist eine COM-Schnittstelle für C- und C++-Entwickler, die auch von .NET-Entwicklern verwendet werden kann. UWP-Entwickler sollten die [Windows.Networking.BackgroundTransfer-API](/uwp/api/Windows.Networking.BackgroundTransfer) und nicht die BITS-API verwenden.

## <a name="bits-versions"></a>BITS-Versionen

Den vollständigen Versionsverlauf und Informationen zu früheren Betriebssystemen finden Sie unter [Neues.](what-s-new.md)


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                           | BESCHREIBUNG                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu BITS](about-bits.md)<br/>                         | Allgemeine Informationen zu BITS.<br/>                                                                                                                                      |
| [Verwenden von BITS](using-bits.md)<br/>                         | Anleitung zum Entwickeln von BITS-Clients, die Dateien zwischen einem Client und einem Server übertragen.<br/>                                                                        |
| [BITS-Referenz](bits-reference.md)<br/>                 | Referenzinformationen für die BITS-Programmierschnittstellen. Enthält auch Informationen zu Beispielen, Tools, Servereinstellungen für Uploadaufträge und das Uploadprotokoll.<br/> |
| [Bewährte Methoden](best-practices-when-using-bits.md)<br/> | Informationen, die beim Entwerfen einer Anwendung zu berücksichtigen sind, die BITS verwendet.<br/>                                                                                                |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Im Folgenden finden Sie weitere Ressourcen.


|    Ressource         |    BESCHREIBUNG                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| .NET-Referenz-DLL   | Informationen zur Verwendung von BITS aus .NET mithilfe von Verweis-DLLs finden Sie unter Aufrufen von BITS aus [.NET mithilfe von Verweis-DLLs.](/windows/desktop/Bits/bits-dot-net)      |
| .NET Wrapper   | Für andere .NET-Wrapper für BITS können Sie [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) nach Projekten suchen, die mit dem BITS-Tag gekennzeichnet sind.        |



 

 

