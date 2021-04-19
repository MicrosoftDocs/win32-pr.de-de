---
description: Eine Liste möglicher Gründe, aus denen ein Windows Installer der Installation nicht alle Dateien einer Anwendung entfernen konnte.
ms.assetid: 0a856f0f-a829-478e-a83b-dade7b05b4f2
title: Entfernen von gestrandeten Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5eeceb45c2139d146c32bdf9917e41885688df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348088"
---
# <a name="removing-stranded-files"></a>Entfernen von gestrandeten Dateien

Wenn eine Datei, die auf dem Computer des Benutzers entfernt worden sein soll, nach dem Ausführen einer Deinstallation weiterhin installiert ist, entfernt das Installationsprogramm möglicherweise die Komponente, die die Datei enthält, aus einem oder mehreren der folgenden Gründe:

-   Das msidbcomponentattributespermanent-Bit wurde für die Komponente in der Attribut-Spalte der [Komponenten Tabelle](component-table.md)festgelegt.
-   Für die Komponente in der ComponentID-Spalte der Component-Tabelle wurde kein Wert eingegeben.
-   Die Komponente wird von einer anderen Anwendung oder einem anderen Feature verwendet, das noch installiert ist.
-   In der Bedingungs Tabelle ist [eine Bedingung angegeben](condition-table.md) , die eine Funktion während der Installation aktiviert und die Funktion während der Neuinstallation deaktiviert.
-   Die Schlüsseldatei für die Komponente enthält einen früheren Verweis Zähler unter **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.
-   Die Komponente wird im Ordner "System" installiert, und jede Datei in der Komponente enthält einen früheren Verweis Zähler unter " **HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**".
-   Der Windows Installer entfernt keine Dateien oder Registrierungsschlüssel, die durch [Windows-Ressourcenschutz](../wfp/windows-resource-protection-portal.md) (WRP) geschützt sind. Weitere Informationen finden Sie unter [Verwenden von Windows Installer und Windows-Ressourcenschutz](windows-resource-protection-on-windows-vista.md). Unter Windows Server 2003, Windows XP und Windows 2000 entfernt das Installationsprogramm keine Dateien, die durch den Windows-Datei Schutz (WFP) geschützt sind. Wenn die Schlüssel Pfad Datei oder der Registrierungsschlüssel einer Komponente durch WFP oder WRP geschützt ist, entfernt das Installationsprogramm die Komponente nicht.
    > [!Note]  
    > Da Windows Installer keine von WRP geschützten Ressourcen installiert, aktualisiert oder entfernt, sollten Sie geschützte Ressourcen nicht in ein Installationspaket einschließen. Verwenden Sie stattdessen nur die [unterstützten Mechanismen für die Ressourcen Ersetzung](../wfp/supported-file-replacement-mechanisms.md) , die im Abschnitt [Windows-Ressourcenschutz](../wfp/windows-resource-protection-portal.md) beschrieben werden.

     

 

 
