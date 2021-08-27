---
description: Sie können nicht über eine benutzerdefinierte Aktion, bei der es sich nicht um die aktuelle Installationssitzung handelt, auf eine Installationssitzung zugreifen.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Zugreifen auf eine Datenbank oder Sitzung innerhalb einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c653d14bc2fdb361469389c4ee053e5d98b65f8c8265516c4e2c3bd4fc4c96d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046060"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a>Zugreifen auf eine Datenbank oder Sitzung innerhalb einer benutzerdefinierten Aktion

Sie können nicht über eine benutzerdefinierte Aktion, bei der es sich nicht um die aktuelle Installationssitzung handelt, auf eine Installationssitzung zugreifen. Benutzerdefinierte Aktionen sind darauf beschränkt, nur mit der aktiven Datenbank der Sitzung und keiner anderen Datenbank zu arbeiten. Die folgenden Windows Installer [Database Functions](database-functions.md) dürfen nicht von einer benutzerdefinierten Aktion aufgerufen werden, da sie ein Handle für eine Datenbank erfordern, die nicht die Datenbank der aktuellen Installationssitzung ist:

[**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf die aktuelle Installersitzung innerhalb einer benutzerdefinierten Aktion](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



