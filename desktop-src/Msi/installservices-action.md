---
description: Die Aktion InstallServices registriert einen Dienst für das System. Diese Aktion fragt die ServiceInstall-Tabelle ab.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: InstallServices-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e37ea0a80050d6e9ab624ff878a352f96bbc0854fd64d6a1f563f277f1ea6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787020"
---
# <a name="installservices-action"></a>InstallServices-Aktion

Die Aktion InstallServices registriert einen Dienst für das System. Diese Aktion fragt die [ServiceInstall-Tabelle](serviceinstall-table.md)ab.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die Dienstaktion muss in der folgenden Sequenz verwendet werden.

[StopServices](stopservices-action.md)

[DeleteServices](deleteservices-action.md)

Eine der folgenden Aktionen: [InstallFiles,](installfiles-action.md) [RemoveFiles,](removefiles-action.md) [DuplicateFiles,](duplicatefiles-action.md) [MoveFiles,](movefiles-action.md) [PatchFiles](patchfiles-action.md)und [RemoveDuplicateFiles.](removeduplicatefiles-action.md)

InstallServices

[StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>ActionData-Nachrichten

Es sind keine ActionData-Meldungen vorhanden.

## <a name="remarks"></a>Hinweise

Diese Aktion erfordert, dass der Benutzer Administrator ist oder über erhöhte Berechtigungen mit der Berechtigung zum Installieren von Diensten verfügt oder dass die Anwendung Teil einer verwalteten Installation ist.

 

 



