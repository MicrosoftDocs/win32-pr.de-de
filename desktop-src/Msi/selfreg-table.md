---
description: Die Tabelle SelfReg enthält Informationen zu Modulen, die selbst registriert werden müssen.
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: SelfReg-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d00b9f18755cf3284edfd1ba9476b12ba6343c816dbafe84ac3c3676f663f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625506"
---
# <a name="selfreg-table"></a>SelfReg-Tabelle

Die Tabelle SelfReg enthält Informationen zu Modulen, die selbst registriert werden müssen. Das Installationsprogramm ruft die [**DllRegisterServer-Funktion**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) während der Installation des Moduls auf. Sie ruft [**DllUnregisterServer während**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) der Deinstallation des Moduls auf. Das Installationsprogramm registriert exe-Dateien nicht selbst.

Die Tabelle SelfReg enthält die folgenden Spalten.



| Spalte | Typ                         | Key | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Datei\_ | [Identifier](identifier.md) | J   | N        |
| Kosten   | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Externer Schlüssel in der ersten Spalte der [Dateitabelle,](file-table.md) der das Modul angibt, das registriert werden muss.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Kosten
</dt> <dd>

Die Kosten für die Registrierung des Moduls in Bytes. Dies muss eine nicht negative Zahl sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Autoren von Installationspaketen wird dringend davon abgeraten, die Selbstregistrierung zu verwenden. Stattdessen sollten sie Module registrieren, indem sie eine oder mehrere Tabellen erstellen, die vom Installationsprogramm für diesen Zweck bereitgestellt werden. Weitere Informationen finden Sie unter [Registrierungstabellengruppe](registry-tables-group.md). Viele der Vorteile eines zentralen Installationsdiensts gehen bei der Selbstregistrierung verloren, da Routinen für die Selbstregistrierung dazu tendieren, kritische Konfigurationsinformationen auszublenden. Gründe für das Vermeiden der Selbstregistrierung sind:

-   Ein Rollback einer Installation mit selbst registrierten Modulen kann nicht sicher mit [**dllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) durchgeführt werden, da es keine Möglichkeit gibt, zu sagen, ob die selbst registrierten Schlüssel von einem anderen Feature oder einer anderen Anwendung verwendet werden.
-   Die Möglichkeit zur Verwendung von Ankündigungen wird verringert, wenn die Registrierung des Klassen- oder Erweiterungsservers innerhalb von Routinen für die Selbstregistrierung durchgeführt wird.
-   Das Installationsprogramm verarbeitet HKCR-Schlüssel in den Registrierungstabellen automatisch sowohl für Installationen pro Benutzer als auch pro Computer. [**DllRegisterServer-Routinen**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) unterstützen derzeit nicht das Konzept eines HKCR-Schlüssels pro Benutzer.
-   Wenn mehrere Benutzer eine selbst registrierte Anwendung auf demselben Computer verwenden, muss jeder Benutzer die Anwendung bei der ersten Ausführung installieren. Andernfalls kann das Installationsprogramm nicht einfach feststellen, dass die richtigen HKCU-Registrierungsschlüssel vorhanden sind.
-   Dem [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) kann der Zugriff auf Netzwerkressourcen wie Typbibliotheken verweigert werden, wenn eine Komponente sowohl als "run-from-source" angegeben als auch in der SelfReg-Tabelle aufgeführt ist. Dies kann dazu führen, dass die Installation der Komponente während einer Administratorinstallation fehlschlägt.
-   Selbstregistrierungs-DLLs sind anfälliger für Codierungsfehler, da der für [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) erforderliche neue Code für jede DLL häufig unterschiedlich ist. Verwenden Sie stattdessen die Registrierungstabellen in der Datenbank, um von vorhandenem Code zu profitieren, der vom Installationsprogramm bereitgestellt wird.
-   Selbstregistrierungs-DLLs können manchmal mit Hilfs-DLLs verknüpfen, die nicht vorhanden sind oder die falsche Version sind. Im Gegensatz dazu kann das Installationsprogramm die DLLs mithilfe der Registrierungstabellen ohne Abhängigkeit vom aktuellen Systemstatus registrieren.

> [!Note]  
> Sie können nicht die Reihenfolge angeben, in der das Installationsprogramm selbstregistrierungsbasierte DLLs mithilfe der [SelfRegModules-](selfregmodules-action.md) und [SelfUnRegModules-Aktionen](selfunregmodules-action.md) registriert oder die Registrierung aufheben soll. Weitere Informationen [finden Sie unter Angeben der Reihenfolge der Selbstregistrierung.](specifying-the-order-of-self-registration.md)

 

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 
