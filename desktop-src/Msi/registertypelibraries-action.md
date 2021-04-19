---
description: Mit der registertypelibraries-Aktion werden Typbibliotheken beim System registriert. Diese Aktion wird auf jede Datei angewendet, auf die in der TypeLib-Tabelle verwiesen wird, die für die Installation geplant ist.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Registertypelibraries-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353443"
---
# <a name="registertypelibraries-action"></a>Registertypelibraries-Aktion

Mit der registertypelibraries-Aktion werden Typbibliotheken beim System registriert. Diese Aktion wird auf jede Datei angewendet, auf die in der [typelib-Tabelle](typelib-table.md) verwiesen wird, die für die Installation geplant ist.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion registertypelibraries muss nach der Aktion [InstallFiles](installfiles-action.md) erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                   |
|-------|----------------------------------------------|
| \[1\] | [GUID](guid.md) der registrierten Typbibliothek. |



 

## <a name="remarks"></a>Bemerkungen

Die registertypelibraries-Aktion erfordert, dass die Typbibliotheks Sprache im Language-Feld der TypeLib-Tabelle ordnungsgemäß verfasst wird. Eine falsche Erstellung des sprach Felds kann bewirken, dass das Installationsprogramm eine ansonsten gültige Typbibliothek nicht registriert.

 

 



