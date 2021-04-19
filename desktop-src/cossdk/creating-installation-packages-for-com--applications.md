---
description: Installationspakete für COM+-Anwendungen werden erstellt.
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Installationspakete für COM+-Anwendungen werden erstellt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ec34852ab405d965fa1ad8f8fb5892616d1347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346641"
---
# <a name="creating-installation-packages-for-com-applications"></a>Installationspakete für COM+-Anwendungen werden erstellt.

Mit dem Verwaltungs Programmkomponenten Dienste oder der com+-Verwaltungs Bibliothek können Sie Installationspakete für COM+-Anwendungen und Anwendungs Proxys erstellen.

Com+ generiert Windows Installer Installationspakete, die in einer einzigen Datei alle erforderlichen Komponenten zum Installieren einer COM+-Anwendung auf einem anderen Computer enthalten.

Beim Exportieren einer COM+-Anwendung bestimmt das Verwaltungs Programmkomponenten Dienste den Satz von Klassen, Komponenten und deren Attributen der Anwendung sowie Attribute auf Anwendungsebene. Aus diesen Informationen generiert das Verwaltungs Programmkomponenten Dienste eine einzelne MSI-Datei, die Folgendes enthält:

-   Windows Installer Tabellen mit com-Registrierungsinformationen (Weitere Informationen finden Sie in der Windows Installer Dokumentation).
-   Eine APL-Datei, die die Attribute der Anwendung enthält. (Hierbei handelt es sich um eine interne Datei; das Format dieser Datei ist nicht dokumentiert.)
-   DLLs und Typbibliotheken, die die Schnittstellen beschreiben, die von den Klassen der com+-Anwendung implementiert werden.

Neben der MSI-Datei generiert das Verwaltungs Programmkomponenten Dienste eine CAB-Datei. Diese Datei dient als Wrapper für die MSI-Datei und ermöglicht dem Entwickler die Bereitstellung der com+-Anwendung über Microsoft Internet Explorer.

> [!Note]  
> Beim Exportieren einer COM+-Anwendung verpackt das Verwaltungs Programmkomponenten Dienste nur die com+-Standardteile der Anwendung. Es werden z. b. keine abhängigen DLL-Dateien oder Datendateien paketieren. Vor der Installation der com+-Anwendung müssen die abhängigen DLL-Dateien zuerst auf einem Computer installiert werden. Alternativ können Sie das Windows Installer Authoring Tool verwenden, um diese abhängigen Dateien der MSI-Datei hinzuzufügen, die vom Verwaltungs Programmkomponenten Dienste generiert wird. (Ausführliche Informationen finden Sie in der Windows Installer-Dokumentation.)

 

## <a name="installing-com-applications-on-other-computers"></a>Installieren von com+-Anwendungen auf anderen Computern

Die vom Verwaltungs Programmkomponenten Dienste generierte Windows Installer Datei (. msi) kann verwendet werden, um die COM+-Anwendung auf einem anderen Computer zu installieren. Die MSI-Datei, die eine COM+-Anwendung enthält, kann nur auf Computern installiert werden, die com+-Dienste unterstützen. Ausführliche Verfahren zum Bereitstellen von com+-Anwendungen finden Sie unter "Installieren von com+-Anwendungen" in der Hilfe zur Verwaltung von Komponenten Diensten.

Wenn die MSI-Datei nicht mit einem Windows Installer Authoring Tool geändert wird, werden mithilfe der Windows Installer installierte COM+-Anwendungen in der Systemsteuerung Software angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Proxys](deploying-application-proxies.md)
</dt> <dt>

[Der com+-Katalog](the-com--catalog.md)
</dt> </dl>

 

 



