---
description: Die Tabelle selfreg enthält Informationen zu Modulen, die selbst registriert werden müssen.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: Selfreg-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5895b1d23369a7c121547fed841731b5d3e76ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760146"
---
# <a name="selfreg-table"></a>Selfreg-Tabelle

Die Tabelle selfreg enthält Informationen zu Modulen, die selbst registriert werden müssen. Der Installer Ruft die [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) -Funktion während der Installation des Moduls auf. [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) wird während der Installation des Moduls aufgerufen. EXE-Dateien werden vom Installationsprogramm nicht selbst registriert.

Die Tabelle selfreg weist die folgenden Spalten auf.



| Spalte | Typ                         | Schlüssel | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Datei\_ | [Bezeichner](identifier.md) | J   | N        |
| „Cost“ (Kosten)   | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Externer Schlüssel in die erste Spalte der [Dateitabelle](file-table.md) , die das Modul angibt, das registriert werden muss.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Preis
</dt> <dd>

Die Kosten für die Registrierung des Moduls in Bytes. Dabei muss es sich um eine nicht negative Zahl handeln.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Autoren von Installationspaketen werden dringend von der Verwendung der Selbstregistrierung abgeraten. Stattdessen sollten Sie Module registrieren, indem Sie eine oder mehrere Tabellen erstellen, die für diesen Zweck vom Installationsprogramm bereitgestellt werden. Weitere Informationen finden Sie unter [Gruppe "Registrierungs Tabellen](registry-tables-group.md)". Viele der Vorteile eines zentralen Installations Diensts gehen bei der Selbstregistrierung verloren, da in der Regel selbst Registrierungs Routinen wichtige Konfigurationsinformationen ausgeblendet werden. Gründe für die Vermeidung der Selbstregistrierung:

-   Das Rollback einer Installation mit selbst registrierten Modulen kann nicht sicher mithilfe von " [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) " durchgeführt werden, da es keine Möglichkeit gibt, zu sagen, ob die selbst registrierten Schlüssel von einem anderen Feature oder einer Anwendung verwendet werden.
-   Die Möglichkeit zur Verwendung von Ankündigungen wird verringert, wenn die Registrierung der Klassen-oder Erweiterungs Server in selbst Registrierungs Routinen erfolgt.
-   Der Installer verarbeitet automatisch HKCR-Schlüssel in den Registrierungs Tabellen für Benutzer-oder Computer spezifische Installationen. [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) -Routinen unterstützen derzeit nicht das Konzept eines benutzerspezifischen HKCR-Schlüssels.
-   Wenn mehrere Benutzer eine selbst registrierte Anwendung auf dem gleichen Computer verwenden, muss jeder Benutzer die Anwendung beim ersten Ausführen installieren. Andernfalls kann das Installationsprogramm nicht einfach ermitteln, ob die richtigen HKCU-Registrierungsschlüssel vorhanden sind.
-   Dem [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) kann der Zugriff auf Netzwerkressourcen, z. b. Typbibliotheken, verweigert werden, wenn eine Komponente sowohl als "aus der Quelle ausführen" angegeben ist als auch in der Tabelle "selfreg" aufgeführt ist. Dies kann dazu führen, dass bei der Installation der Komponente während einer administrativen Installation ein Fehler auftritt.
-   Selbst registrierte DLLs sind anfälliger für Codierungsfehler, da der für [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) erforderliche neue Code für jede DLL häufig anders ist. Verwenden Sie stattdessen die Registrierungs Tabellen in der-Datenbank, um den vorhandenen Code zu nutzen, der vom Installationsprogramm bereitgestellt wird.
-   Selbst registrierte DLLs können manchmal mit zusätzlichen DLLs verknüpft werden, die nicht vorhanden sind oder die falsche Version sind. Im Gegensatz dazu kann das Installationsprogramm die DLLs unter Verwendung der Registrierungs Tabellen registrieren, ohne dass vom aktuellen Status des Systems abhängig ist.

> [!Note]  
> Sie können nicht die Reihenfolge angeben, in der der Installer mithilfe der [SelfRegModules](selfregmodules-action.md) -und [selfunregmodules](selfunregmodules-action.md) -Aktionen selbst registrierte DLLs registriert bzw. die Registrierung aufheben. Siehe [angeben der Reihenfolge der Selbstregistrierung](specifying-the-order-of-self-registration.md).

 

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 
