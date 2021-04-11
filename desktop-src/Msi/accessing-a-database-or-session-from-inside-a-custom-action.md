---
description: Über eine benutzerdefinierte Aktion, die nicht die aktuelle Installationssitzung ist, kann nicht auf eine installersitzung zugegriffen werden.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Zugreifen auf eine Datenbank oder eine Sitzung innerhalb einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959557"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a>Zugreifen auf eine Datenbank oder eine Sitzung innerhalb einer benutzerdefinierten Aktion

Über eine benutzerdefinierte Aktion, die nicht die aktuelle Installationssitzung ist, kann nicht auf eine installersitzung zugegriffen werden. Benutzerdefinierte Aktionen können nur mit der aktiven Datenbank der Sitzung und ohne andere Datenbanken arbeiten. Die folgenden Windows Installer- [Datenbankfunktionen](database-functions.md) dürfen nicht von einer benutzerdefinierten Aktion aufgerufen werden, da Sie ein Handle für eine Datenbank erfordern, bei der es sich nicht um die Datenbank der aktuellen Installationssitzung handelt:

[**Msidatabasemerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[**Msikreatetransformsummaryinfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[**Msidatabaseapplytransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[**Msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[**Msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[**Msidatabasegeneratetransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[**Msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[**Msienableuipreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[**Msigetdatabasestate**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf die aktuelle Installer-Sitzung innerhalb einer benutzerdefinierten Aktion](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



