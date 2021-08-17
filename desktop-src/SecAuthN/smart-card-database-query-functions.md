---
description: Fragen Sie die Smartcard-Datenbank ab. Sie können eine Liste der Smartcards bereitstellen, die von einem bestimmten Benutzer, den Schnittstellen und dem primären Dienstanbieter einer bestimmten Karte, den für das System definierten Lesergruppen und den Lesern innerhalb einer Gruppe von Lesergruppen bereitgestellt werden.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Smartcard-Datenbankabfragefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54050ad6e6b5b4d7e8c91f7cdefab683274d153050100545c9e1ed5452c47cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917796"
---
# <a name="smart-card-database-query-functions"></a>Smartcard-Datenbankabfragefunktionen

Die folgenden Funktionen fragen die [*Smartcard-Datenbank*](../secgloss/s-gly.md)ab. Sie können eine Liste der Smartcards bereitstellen, die von einem bestimmten Benutzer, den Schnittstellen und dem [*primären Dienstanbieter*](../secgloss/p-gly.md) einer bestimmten Karte, den für das System definierten [*Lesergruppen*](../secgloss/r-gly.md) und den [*Lesern*](../secgloss/r-gly.md) innerhalb einer Gruppe von Lesergruppen bereitgestellt werden.

Wenn Sie diese Funktionen verwenden, können Sie die gesamte Smartcard-Datenbank abfragen oder die Suche einschränken, indem Sie den [*Resource Manager-Kontext*](../secgloss/r-gly.md)festlegen. Der Ressourcen-Manager-Kontext wird durch Aufrufen von [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) festgelegt, bevor eine Abfragefunktion aufgerufen wird.

> [!Note]  
> Ohne angegebenen Kontext kann aufgrund von Sicherheitseinschränkungen weiterhin auf einige Informationen zugegriffen werden.

 



| Thema                                                  | BESCHREIBUNG                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardGetProviderId**](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | Rufen Sie den Bezeichner (GUID) des [*primären Dienstanbieters*](../secgloss/p-gly.md) für die angegebene Karte ab. |
| [**SCardListCards**](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | Rufen Sie eine Liste von Karten ab, die zuvor von einem bestimmten Benutzer in das System eingeführt wurden.                                                                                                     |
| [**SCardListInterfaces**](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | Rufen Sie die Bezeichner (GUIDs) der Schnittstellen ab, die von einer angegebenen Karte bereitgestellt werden.                                                                                                         |
| [**SCardListReaderGroups**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | Rufen Sie eine Liste von Lesergruppen ab, die zuvor in das System eingeführt wurden.                                                                                                 |
| [**SCardListReaders**](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | Ruft die Liste der Leser innerhalb einer Gruppe benannter Readergruppen ab.                                                                                                                    |



 

 

 
