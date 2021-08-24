---
description: Die Aktion UnregisterFonts entfernt Registrierungsinformationen zu installierten Schriftarten aus dem System.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: UnregisterFonts-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ec15a7a431a03d678fb2fd8c39460ea40ebbcadf3efd0c24814c84e6042fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787000"
---
# <a name="unregisterfonts-action"></a>UnregisterFonts-Aktion

Die Aktion UnregisterFonts entfernt Registrierungsinformationen zu installierten Schriftarten aus dem System.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die [RemoveFiles-Aktion](removefiles-action.md) muss nach UnregisterFonts aufgerufen werden.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten |
|-------|----------------------------|
| \[1\] | Schriftartdatei.                 |



 

## <a name="remarks"></a>Hinweise

Die Aktion UnregisterFonts wird ausgeführt, wenn die in der Spalte Datei der Tabelle Schriftart angegebene Datei \_ zu einer komponente gehört, die deinstalliert [](font-table.md) wird.

 

 



