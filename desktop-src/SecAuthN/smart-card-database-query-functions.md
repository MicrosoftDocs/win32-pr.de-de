---
description: Fragen Sie die Smartcard-Datenbank ab. Sie können eine Liste von Smartcards bereitstellen, die von einem bestimmten Benutzer bereitgestellt werden, die Schnittstellen und den primären Dienstanbieter einer bestimmten Karte, die für das System definierten Lesergruppen und die Leser innerhalb einer Gruppe von Lesergruppen.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Smartcard-Datenbankabfrage Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217458"
---
# <a name="smart-card-database-query-functions"></a>Smartcard-Datenbankabfrage Funktionen

Mit den folgenden Funktionen wird die [*Smartcard-Datenbank*](../secgloss/s-gly.md)abgefragt. Sie können eine Liste von Smartcards bereitstellen, die von einem bestimmten Benutzer bereitgestellt werden, die Schnittstellen und den [*primären Dienstanbieter*](../secgloss/p-gly.md) einer bestimmten Karte, die für das System definierten [*Lesergruppen*](../secgloss/r-gly.md) und die [*Leser*](../secgloss/r-gly.md) innerhalb einer Gruppe von Lesergruppen.

Wenn Sie diese Funktionen verwenden, können Sie die gesamte smartcarddatenbank Abfragen, oder Sie können die Suche eingrenzen, indem Sie den [*Resource Manager-Kontext*](../secgloss/r-gly.md)festlegen. Der Resource Manager-Kontext wird durch Aufrufen von [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) festgelegt, bevor eine Abfragefunktion aufgerufen wird.

> [!Note]  
> Ohne einen angegebenen Kontext sind einige Informationen möglicherweise aufgrund von Sicherheitseinschränkungen noch nicht zugänglich.

 



| Thema                                                  | BESCHREIBUNG                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Scardgetproviderid"**](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | Ruft den Bezeichner (GUID) des [*primären Dienstanbieters*](../secgloss/p-gly.md) für die angegebene Karte ab. |
| [**Scardlistcards**](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | Abrufen einer Liste von Karten, die bereits von einem bestimmten Benutzer in das System eingefügt wurden.                                                                                                     |
| [**Scardlistinterfaces**](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | Abrufen der Bezeichner (GUIDs) der Schnittstellen, die von einer angegebenen Karte bereitgestellt werden.                                                                                                         |
| [**Scardlistreadergroups**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | Rufen Sie eine Liste der Lesergruppen ab, die bereits im System eingeführt wurden.                                                                                                 |
| [**SCardListReaders**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | Ruft die Liste der Leser innerhalb einer Gruppe benannter Lesergruppen ab.                                                                                                                    |



 

 

 
