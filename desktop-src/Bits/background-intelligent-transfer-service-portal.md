---
title: Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
description: Mit dem intelligenten Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS) werden Dateien zwischen einem Client und einem Server übertragen (Downloads oder Uploads). Dabei werden Statusinformationen zu den Übertragungsvorgängen angezeigt.
ms.assetid: ce91f87c-8273-4a1c-99e0-ef55e2a50334
keywords:
- Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
- Background Intelligent Transfer Service, Startseite
- Bits (siehe Background Intelligent Transfer Service)
- Herunterladen von Dateien Bits
- Hintergrunddatei-Übertragungs Bits
- Hochladen von Dateien in Bits
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: a531821665490735b391ab2714f5b37146c6bc1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948988"
---
# <a name="background-intelligent-transfer-service"></a>Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)

## <a name="purpose"></a>Zweck

Background Intelligent Transfer Service (Bits) wird von Programmierern und Systemadministratoren verwendet, um Dateien aus HTTP-Webservern und SMB-Dateifreigaben herunterzuladen oder in diese hochzuladen. Bits übernimmt die Kosten für die Übertragung sowie die Netzwerk Auslastung, sodass die Vordergrund Arbeit des Benutzers so wenig wie möglich wirkt. Bits übernimmt auch nach einem Neustart das Übertragen von Netzwerk Überläufen, das Anhalten und Fortsetzen von Übertragungen. Bits umfasst PowerShell-Cmdlets zum Erstellen und Verwalten von Übertragungen sowie das Befehlszeilenprogramm BITSAdmin.

> [!Note]  
> Bits können von Windows verwendet werden, um Updates auf Ihr lokales System herunterzuladen. Wenn Sie ein Endbenutzer sind, der nach Methoden zur Problembehandlung bei der Bits-Installation sucht, finden Sie weitere Informationen unter [Beheben von Windows Update Problemen](https://support.microsoft.com/help/10164/fix-windows-update-errors). 
 

## <a name="where-applicable"></a>Anwendungsbereich

Verwenden Sie Bits für Anwendungen, die Folgendes erfordern:

-   Herunterladen von oder Hochladen von Dateien auf einen HTTP-oder Rest-Webserver oder einen SMB-Dateiserver.
-   Automatisches fortsetzen von Dateiübertragungen nach dem Trennen des Netzwerks und Neustarts des Computers.
-   Bewahren Sie die Reaktionsfähigkeit anderer Netzwerkanwendungen auf.
-   Berücksichtigen Sie die Netzwerkkosten, z. b. roamingnetzwerke
-   Optionales arbeiten mit [BranchCache](/windows-server/networking/branchcache/branchcache) zur Optimierung des WAN-Verkehrs (Wide Area Network)

## <a name="developer-audience"></a>Entwicklergruppe

Bits ist eine für C-und C++-Entwickler entwickelte com-Schnittstelle, die auch von .NET-Entwicklern verwendet werden kann. UWP-Entwickler sollten die [Windows. Networking. backgroundtransfer](/uwp/api/Windows.Networking.BackgroundTransfer) -API und nicht die Bits-API verwenden.

## <a name="bits-versions"></a>Bits-Versionen

[Den](what-s-new.md)vollständigen Versionsverlauf und Informationen zum früheren Betriebssystem finden Sie unter Neuigkeiten.


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                           | BESCHREIBUNG                                                                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu BITS](about-bits.md)<br/>                         | Allgemeine Informationen zu Bits.<br/>                                                                                                                                      |
| [Verwenden von Bits](using-bits.md)<br/>                         | Verfahrens Leit Faden zum Entwickeln von BITS-Clients, die Dateien zwischen einem Client und einem Server übertragen.<br/>                                                                        |
| [BITS-Referenz](bits-reference.md)<br/>                 | Referenzinformationen für die Bits-Programmierschnittstellen. Enthält außerdem Informationen zu Beispielen, Tools, Servereinstellungen für Uploadaufträge und das uploadprotokoll.<br/> |
| [Bewährte Methoden](best-practices-when-using-bits.md)<br/> | Beim Entwerfen einer Anwendung, die Bits verwendet, zu berücksichtigende Informationen.<br/>                                                                                                |



 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Im folgenden finden Sie weitere Ressourcen.


|             |                                                                                                                                                 |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| .Net-Referenz-dll   | Informationen zur Verwendung von Bits aus .NET mithilfe von Verweis-DLLs finden Sie unter [Aufrufen von Bits aus .NET mithilfe von Verweis-DLLs](/windows/desktop/Bits/bits-dot-net) .      |
| .Net-Wrapper   | Für andere .net-Wrapper für Bits können Sie [nuget](https://www.nuget.org/packages?q=Tags%3A%22BITS%22) nach Projekten durchsuchen, die mit dem Bits-Tag markiert sind.        |



 

 

