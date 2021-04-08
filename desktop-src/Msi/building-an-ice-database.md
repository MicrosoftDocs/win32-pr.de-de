---
description: Nachdem Sie die entsprechenden ICES für die Validierung ausgewählt haben, muss ein Entwickler die benutzerdefinierten Aktionen in einer Ice-Datenbank zusammenfassen.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Aufbauen einer Ice-Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51043aa9b3c1591fa3262492c117aba35f23d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864427"
---
# <a name="building-an-ice-database"></a>Aufbauen einer Ice-Datenbank

Nachdem Sie die entsprechenden [ICES](internal-consistency-evaluators-ices.md) für die Validierung ausgewählt haben, muss ein Entwickler die benutzerdefinierten Aktionen in einer Ice-Datenbank zusammenfassen. Eine CUB-Datei ist eine MSI-Standarddatenbank, die nur die ICES und die erforderlichen Tabellen enthält. Eine CUB-Datei kann nicht installiert werden und wird nur zum Speichern und Bereitstellen des Zugriffs auf benutzerdefinierte Ice-Aktionen verwendet.

Eine CUB-Datei enthält die folgenden Datenbanktabellen.



| Tabelle                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Binär (Binary)](binary-table.md)             | Die Skriptdateien, DLLs und EXEs der ICE-Zoll-Aktionen, auf die in der Tabelle "CustomAction" verwiesen wird.                                                                                                                                                                 |
| [CustomAction](customaction-table.md) | Jeder Datensatz in dieser Tabelle entspricht einer benutzerdefinierten Ice-Aktion, die in der CUB-Datei enthalten ist.                                                                                                                                                                                   |
| \_Icesequence                          | In dieser Tabelle sind die Ice-Zoll-Aktionen aufgeführt, die in der CUB-Datei in ihrer Ausführungssequenz enthalten sind. Die in dieser Tabelle aufgeführten benutzerdefinierten Eis Aktionen werden durch Aufrufen von " [**msisequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)" oder einzeln mithilfe von " [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)" ausgeführt. |
| [\_Überprüfen](-validation-table.md)  | Diese Tabelle enthält die CUB-Datei Einträge, die in der Validierungs Tabelle zusammengeführt werden sollen \_ .                                                                                                                                                                               |
| \_Sonderfunktionen                              | Alle speziellen Verarbeitungs Tabellen, die für bestimmte benutzerdefinierte Ice-Aktionen erforderlich sind, müssen in der CUB-Datei enthalten sein. Der Name dieser Tabellen muss einen führenden Unterstrich aufweisen.                                                                                                        |



 

Weitere Informationen finden Sie unter [Sample. CUB-Datei](sample--cub-file.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufbauen eines Eis](building-an-ice.md)
</dt> </dl>

 

 



