---
description: Mit der Aktion installsfpcatalogfile werden die von Windows Me für den Windows-Datei Schutz verwendeten Kataloge installiert.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Installsfpcatalogfile-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343234"
---
# <a name="installsfpcatalogfile-action"></a>Installsfpcatalogfile-Aktion

Mit der Aktion installsfpcatalogfile werden die von Windows Me für den Windows-Datei Schutz verwendeten Kataloge installiert. Installsfpcatalogfile fragt die [Komponenten Tabelle](component-table.md), die [Dateitabelle](file-table.md), die [filesfpcatalog-Tabelle](filesfpcatalog-table.md) und die [sfpcatalog-Tabelle](sfpcatalog-table.md)ab. Kataloge werden installiert, wenn Sie einer Datei in einer-Komponente zugeordnet sind, die für die lokale Installation festgelegt ist, oder wenn Sie einer Datei zugeordnet sind, die in einer lokal installierten Komponente repariert wird.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion installsfpcatalogfile muss vor " [InstallFiles](installfiles-action.md) " und nach " [costfinalize](costfinalize-action.md)" sequenziert werden.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Der Name des zu installierenden Katalogs.                          |
| \[2\] | Der Name des Katalogs, von dem die Installation dieses Katalogs abhängig ist. |



 

## <a name="remarks"></a>Bemerkungen

Ein Katalog, der von einem anderen Katalog abhängig ist, der nach dem übergeordneten Katalog installiert ist.

 

 



