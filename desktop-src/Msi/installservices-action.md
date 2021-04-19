---
description: Die Aktion "installservices" registriert einen Dienst für das System. Durch diese Aktion wird die Tabelle "ServiceInstall" abgefragt.
ms.assetid: bb394cdb-1310-44fb-b7e1-2ffbb976d438
title: Installservices-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5964deb08f811e391418211efc6f774261bd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350108"
---
# <a name="installservices-action"></a>Installservices-Aktion

Die Aktion "installservices" registriert einen Dienst für das System. Durch diese Aktion wird die [Tabelle "ServiceInstall](serviceinstall-table.md)" abgefragt.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Dienst Aktion muss in der folgenden Reihenfolge verwendet werden.

[Stop Services](stopservices-action.md)

[Delta Service Services](deleteservices-action.md)

Folgende Aktionen sind möglich: " [InstallFiles](installfiles-action.md)", " [RemoveFiles](removefiles-action.md)", " [duplicatefiles](duplicatefiles-action.md)", " [muvefiles](movefiles-action.md)", " [PATCHFILES](patchfiles-action.md)" und " [RemoveDuplicateFiles](removeduplicatefiles-action.md) ".

Installdienste

[Startdienste](startservices-action.md)

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Für diese Aktion ist es erforderlich, dass der Benutzer ein Administrator ist oder über erweiterte Berechtigungen mit der Berechtigung zum Installieren von Diensten verfügt oder dass die Anwendung Teil einer verwalteten Installation ist.

 

 



