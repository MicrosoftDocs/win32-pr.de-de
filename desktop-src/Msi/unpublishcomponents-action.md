---
description: Mit der unpublishcomponents-Aktion wird die nicht Ankündigung der in der Tabelle PublishComponent aufgeführten Komponenten verwaltet.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Unpublishcomponents-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104394038"
---
# <a name="unpublishcomponents-action"></a>Unpublishcomponents-Aktion

Mit der unpublishcomponents-Aktion wird die nicht Ankündigung der in der Tabelle PublishComponent aufgeführten Komponenten verwaltet. Dabei handelt es sich um Komponenten, bei denen möglicherweise von anderen Produkten ein Fehler aufgetreten ist. Diese Aktion entfernt Informationen zu veröffentlichten Komponenten aus der [PublishComponent-Tabelle](publishcomponent-table.md) , für die die entsprechende Funktion zurzeit für die Deinstallation ausgewählt ist.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Es gibt keine Sequenz Einschränkungen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID, die die Komponenten-ID eines angekündigten Features darstellt. |
| \[2\] | Qualifizierer der Komponenten-ID.                               |



 

