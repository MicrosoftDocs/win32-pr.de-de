---
description: Nachdem ein Entwickler die entsprechenden ICEs für die Überprüfung ausgewählt hat, muss er die benutzerdefinierten Aktionen in einer ICE-Datenbank zusammen sammeln.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Erstellen einer ICE-Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e078517f8942454320e3f743d7379bbfeb22a7c44afe635a8276568a56c27f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926990"
---
# <a name="building-an-ice-database"></a>Erstellen einer ICE-Datenbank

Nachdem ein Entwickler die entsprechenden [ICEs](internal-consistency-evaluators-ices.md) für die Überprüfung ausgewählt hat, muss er die benutzerdefinierten Aktionen in einer ICE-Datenbank zusammen sammeln. Eine CUB-Datei ist eine Standarddatenbank .msi, die nur ICEs und die erforderlichen Tabellen enthält. Eine CUB-Datei kann nicht installiert werden und wird nur zum Speichern und Bereitstellen des Zugriffs auf benutzerdefinierte ICE-Aktionen verwendet.

Eine CUB-Datei enthält die folgenden Datenbanktabellen.



| Tabelle                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Binär (Binary)](binary-table.md)             | Die Skriptdateien, DLLs und EXEs der ICE-Aktionen, auf die in der Tabelle CustomAction verwiesen wird.                                                                                                                                                                 |
| [CustomAction](customaction-table.md) | Jeder Datensatz in dieser Tabelle entspricht einer benutzerdefinierten ICE-Aktion, die in der CUB-Datei enthalten ist.                                                                                                                                                                                   |
| \_ICESequence                          | In dieser Tabelle sind die ICE-Aktionen aufgeführt, die in der CUB-Datei in ihrer Ausführungssequenz enthalten sind. Die in dieser Tabelle aufgeführten benutzerdefinierten ICE-Aktionen werden durch Aufrufen von [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea)oder einzeln mit [**msiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)ausgeführt. |
| [\_Überprüfung](-validation-table.md)  | Diese Tabelle enthält die CUB-Dateieinträge, die mit der Tabelle Validation zusammengeführt werden \_ sollen.                                                                                                                                                                               |
| \_Sonderfunktionen                              | Alle speziellen Verarbeitungstabellen, die für bestimmte benutzerdefinierte ICE-Aktionen erforderlich sind, müssen in der CUB-Datei enthalten sein. Der Name dieser Tabellen muss einen führenden Unterstrich aufweisen.                                                                                                        |



 

Weitere Informationen finden Sie unter [CUB-Beispieldatei.](sample--cub-file.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines ICE](building-an-ice.md)
</dt> </dl>

 

 



