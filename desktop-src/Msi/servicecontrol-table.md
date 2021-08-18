---
description: Die ServiceControl-Tabelle wird verwendet, um installierte oder deinstallierte Dienste zu steuern. Hinweis Dienste, die auf dem Vorhandensein einer Assembly im globalen Assemblycache (GAC) basieren, können nicht mithilfe der Tabellen ServiceInstall und ServiceControl installiert oder gestartet werden.
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: ServiceControl-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b8531fb70c1887d77ae9b09bf3fe7e59de0c7878dfac44707df942e838f4f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039980"
---
# <a name="servicecontrol-table"></a>ServiceControl-Tabelle

Die ServiceControl-Tabelle wird verwendet, um installierte oder deinstallierte Dienste zu steuern.

> [!Note]  
> Dienste, die auf dem [](assemblies.md) Vorhandensein einer Assembly im globalen Assemblycache (GAC) basieren, können nicht mithilfe der [Tabellen ServiceInstall](serviceinstall-table.md) und ServiceControl installiert oder gestartet werden. Wenn Sie einen Dienst starten müssen, der von einer Assembly im GAC abhängt, müssen Sie eine benutzerdefinierte Aktion verwenden, die nach der [InstallFinalize-Aktion](installfinalize-action.md) oder einer benutzerdefinierten Commitaktion [sequenziert ist.](commit-custom-actions.md) Informationen zum Installieren von Assemblys im GAC finden Sie unter [Installation von Assemblys im globalen Assemblycache.](installation-of-assemblies-to-the-global-assembly-cache.md)

 

Die ServiceControl-Tabelle enthält die folgenden Spalten.



| Spalte         | Typ                         | Key | Nullwerte zulässig |
|----------------|------------------------------|-----|----------|
| ServiceControl | [Identifier](identifier.md) | J   | N        |
| Name           | [Formatiert](formatted.md)   | N   | N        |
| Ereignis          | [Integer](integer.md)       | N   | N        |
| Argumente      | [Formatiert](formatted.md)   | N   | J        |
| Warten           | [Integer](integer.md)       | N   | J        |
| Komponente\_    | [Identifier](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl
</dt> <dd>

Dies ist der Primärschlüssel dieser Tabelle.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Diese Spalte ist die Zeichenfolge, die den Dienst bezeichnet. Diese Spalte kann verwendet werden, um einen Dienst zu steuern, der nicht installiert ist.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ereignis
</dt> <dd>

Diese Spalte enthält die Vorgänge, die für den benannten Dienst ausgeführt werden sollen. Beachten Sie, dass beim Beenden eines Diensts auch alle Dienste beendet werden, die von diesem Dienst abhängen. Beim Löschen eines ausgeführten Diensts beendet das Installationsprogramm den Dienst.

Die Werte in diesem Feld sind Bitfelder, die zu einem einzelnen Wert kombiniert werden können, der mehrere Vorgänge darstellt.

Die folgenden Werte werden nur während einer Installation verwendet.



| Konstante                           | Hexadezimal | Decimal | BESCHREIBUNG                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventStart**  | 0x001       | 1       | Startet den Dienst während der [StartServices-Aktion](startservices-action.md).    |
| **msidbServiceControlEventStop**   | 0x002       | 2       | Beendet den Dienst während der [StopServices-Aktion.](stopservices-action.md)       |
| (none)                             | 0x004       | 4       | <reserved>                                                                   |
| **msidbServiceControlEventDelete** | 0x008       | 8       | Löscht den Dienst während der [DeleteServices-Aktion](deleteservices-action.md). |



 

Die folgenden Werte werden nur während einer Deinstallation verwendet.



| Konstante                                    | Hexadezimal | Decimal | BESCHREIBUNG                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbServiceControlEventUninstallStart**  | 0x010       | 16      | Startet den Dienst während der [StartServices-Aktion](startservices-action.md).    |
| **msidbServiceControlEventUninstallStop**   | 0x020       | 32      | Beendet den Dienst während der [StopServices-Aktion.](stopservices-action.md)       |
| (none)                                      | 0x040       | 64      | <reserved>                                                                   |
| **msidbServiceControlEventUninstallDelete** | 0x080       | 128     | Löscht den Dienst während der [DeleteServices-Aktion](deleteservices-action.md). |



 

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumente
</dt> <dd>

Eine Liste von Argumenten zum Starten von Diensten. Die Argumente werden durch NULL-Zeichen \[ ~ \] getrennt. Die Liste der Argumente One, Two und Three wird beispielsweise als One \[ ~ \] Two \[ ~ \] Three aufgelistet.

</dd> <dt>

<span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Warte
</dt> <dd>

Wenn sie dieses Feld null lassen oder den Wert 1 eingeben, wartet das Installationsprogramm maximal 30 Sekunden, bis der Dienst abgeschlossen ist, bevor der Vorgang abgeschlossen wird. Die Wartezeit kann verwendet werden, um zusätzliche Zeit für die Rückgabe eines Fehlerfehlers durch ein kritisches Ereignis zu ermöglichen. Der Wert 0 in diesem Feld bedeutet, nur zu warten, bis der Dienststeuerungs-Manager (Service Control Manager, SCM) meldet, dass sich dieser Dienst in einem ausstehenden Zustand befindet, bevor die Installation fortgesetzt wird.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Komponente\_
</dt> <dd>

Externer Schlüssel zu Spalte 1 der [Komponententabelle.](component-table.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [Aktionen StartServices,](startservices-action.md) [StopServices](stopservices-action.md)und [DeleteServices](deleteservices-action.md) in [*Sequenztabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle. Informationen zur Verwendung von *Sequenztabellen finden* Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

Verwenden Sie die Spalte Name, um Dienste zu starten, zu beenden oder zu löschen, die durch die Installation ersetzt werden oder von einem neuen Dienst abhängig sind, der installiert wird. Wenn Sie beispielsweise MyService in die Spalte ServiceControl eingeben, kann dieser Dienst mit MyComponent in der Spalte Komponente \_ verknüpfen. Wenn das Bitfeld in der Spalte Ereignis für den Start während der Installation festgelegt ist, startet das Installationsprogramm MyService bei der Installation von MyComponent.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



