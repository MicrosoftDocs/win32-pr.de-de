---
description: Die ServiceControl-Tabelle wird zum Steuern installierter oder nicht installierter Dienste verwendet. Beachten Sie, dass Dienste, die sich auf das vorhanden sein einer Assembly im globalen Assemblycache (GAC) verlassen, nicht mithilfe der Tabellen ServiceInstall und ServiceControl installiert oder gestartet werden können.
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: ServiceControl-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2abd123e937673694dffd53773a16fcbd704c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757626"
---
# <a name="servicecontrol-table"></a>ServiceControl-Tabelle

Die ServiceControl-Tabelle wird zum Steuern installierter oder nicht installierter Dienste verwendet.

> [!Note]  
> Dienste, die sich auf das vorhanden sein einer [Assembly](assemblies.md) im globalen Assemblycache (GAC) stützen, können nicht mit den Tabellen [ServiceInstall](serviceinstall-table.md) und ServiceControl installiert oder gestartet werden. Wenn Sie einen Dienst starten müssen, der von einer Assembly im GAC abhängt, müssen Sie eine benutzerdefinierte Aktion verwenden, die nach der [InstallFinalize-Aktion](installfinalize-action.md) oder einer [benutzerdefinierten Commit-Aktion](commit-custom-actions.md)sequenziert ist. Informationen zum Installieren von Assemblys im GAC finden Sie unter Installieren von Assemblys [im globalen Assemblycache](installation-of-assemblies-to-the-global-assembly-cache.md).

 

Die ServiceControl-Tabelle weist die folgenden Spalten auf.



| Spalte         | Typ                         | Schlüssel | Nullwerte zulässig |
|----------------|------------------------------|-----|----------|
| ServiceControl | [Bezeichner](identifier.md) | J   | N        |
| Name           | [Großformatige](formatted.md)   | N   | N        |
| Ereignis          | [Integer](integer.md)       | N   | N        |
| Argumente      | [Großformatige](formatted.md)   | N   | J        |
| Warten           | [Integer](integer.md)       | N   | J        |
| Komponente\_    | [Bezeichner](identifier.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl
</dt> <dd>

Dies ist der Primärschlüssel dieser Tabelle.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Diese Spalte ist die Zeichenfolge, die den Dienst benennt. Diese Spalte kann verwendet werden, um einen Dienst zu steuern, der nicht installiert ist.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Veranstalter
</dt> <dd>

Diese Spalte enthält die Vorgänge, die für den benannten Dienst durchgeführt werden sollen. Beachten Sie, dass beim Beenden eines Diensts alle Dienste, die von diesem Dienst abhängen, ebenfalls angehalten werden. Wenn Sie einen Dienst löschen, der ausgeführt wird, beendet der Installer den Dienst.

Die Werte in diesem Feld sind Bitfelder, die zu einem einzelnen Wert zusammengefasst werden können, der mehrere Vorgänge darstellt.

Die folgenden Werte werden nur während einer-Installation verwendet.



| Konstante                           | Hexadezimal | Decimal | BESCHREIBUNG                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbservicecontroleventstart**  | 0x001       | 1       | Startet den Dienst während der [Start Services-Aktion](startservices-action.md).    |
| **msidbservicecontroleventhalte**   | 0x002       | 2       | Beendet den Dienst während der [Stop Services-Aktion](stopservices-action.md).       |
| (none)                             | 0x004       | 4       | <reserved>                                                                   |
| **msidbservicecontroleventdelete** | 0x008       | 8       | Löscht den Dienst während der [Delta](deleteservices-action.md)Service-Aktion. |



 

Die folgenden Werte werden nur während einer Deinstallation verwendet.



| Konstante                                    | Hexadezimal | Decimal | BESCHREIBUNG                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| **msidbservicecontroleventuninstallstart**  | 0x010       | 16      | Startet den Dienst während der [Start Services-Aktion](startservices-action.md).    |
| **msidbservicecontroleventuninstallstopps**   | 0x020       | 32      | Beendet den Dienst während der [Stop Services-Aktion](stopservices-action.md).       |
| (none)                                      | 0x040       | 64      | <reserved>                                                                   |
| **msidbservicecontroleventuninstalldelete** | 0x080       | 128     | Löscht den Dienst während der [Delta](deleteservices-action.md)Service-Aktion. |



 

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentation
</dt> <dd>

Eine Liste von Argumenten zum Starten von Diensten. Die Argumente sind durch Null Zeichen voneinander getrennt \[ ~ \] . Die Liste der Argumente 1, 2 und 3 wird z. b. wie folgt aufgelistet: 1 \[ ~ \] 2 \[ ~ \] .

</dd> <dt>

<span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Warte
</dt> <dd>

Wenn Sie dieses Feld auf Null setzen oder den Wert 1 eingeben, wartet das Installationsprogramm maximal 30 Sekunden, bis der Dienst beendet ist, bevor der Vorgang fortgesetzt wird. Der Warte Vorgang kann verwendet werden, um zusätzliche Zeit für das Zurückgeben eines Fehler Fehlers durch ein kritisches Ereignis zuzulassen. Der Wert 0 (null) bedeutet, dass nur gewartet werden soll, bis der Dienststeuerungs-Manager (SCM) meldet, dass sich dieser Dienst in einem ausstehenden Zustand befindet, bevor die Installation fortgesetzt wird.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_
</dt> <dd>

Externer Schlüssel für Spalte einer der [Komponenten Tabellen](component-table.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Aktionen " [Start Services](startservices-action.md)", " [Stop Services](stopservices-action.md)" und " [Delta Service](deleteservices-action.md) " in [*Sequenz Tabellen*](s-gly.md) verarbeiten die Informationen in dieser Tabelle. Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

Verwenden Sie die Spalte Name, um Dienste zu starten, zu verhindern oder zu löschen, die durch die-Installation ersetzt werden oder von einem neuen Dienst abhängen, der installiert wird. Wenn Sie z. b. MyService in die ServiceControl-Spalte eingeben, kann dieser Dienst in der Component-Spalte mit MyComponent verknüpft werden \_ . Wenn das Bitfeld in der Ereignis Spalte für Start bei der Installation von festgelegt wird, startet das Installationsprogramm MyService, wenn MyComponent installiert wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



