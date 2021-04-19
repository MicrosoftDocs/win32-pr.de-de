---
description: Die unregisterfonts-Aktion entfernt Registrierungsinformationen zu installierten Schriftarten aus dem System.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Unregisterfonts-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359600"
---
# <a name="unregisterfonts-action"></a>Unregisterfonts-Aktion

Die unregisterfonts-Aktion entfernt Registrierungsinformationen zu installierten Schriftarten aus dem System.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die [RemoveFiles](removefiles-action.md) -Aktion muss nach ' unregisterfonts ' aufgerufen werden.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten |
|-------|----------------------------|
| \[1\] | Schriftart Datei.                 |



 

## <a name="remarks"></a>Bemerkungen

Die unregisterfonts-Aktion wird ausgeführt, wenn die Datei, die in der Datei \_ Spalte der [Schriftart Tabelle](font-table.md) angegeben ist, zu einer Komponente gehört, die deinstalliert wird.

 

 



