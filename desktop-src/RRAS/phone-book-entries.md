---
title: Phone-Book Einträge
description: Telefon Bucheinträge enthalten die Informationen, die zum Herstellen einer RAS-Verbindung erforderlich sind. Ein Benutzer oder Administrator kann das Dialogfeld DFÜ-Netzwerk verwenden, um Telefonbucheinträge zu erstellen, zu bearbeiten und zu wählen.
ms.assetid: 971d7020-f9fd-42d1-97c3-79ad6eba6964
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea62595504229dd5dd920385a92214156a7d112774cb3fefbaff3f1b5edc7cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789820"
---
# <a name="phone-book-entries"></a>Phone-Book Einträge

Telefon Bucheinträge enthalten die Informationen, die zum Herstellen einer RAS-Verbindung erforderlich sind. Ein Benutzer oder Administrator kann das Dialogfeld **DFÜ-Netzwerk** verwenden, um Telefonbucheinträge zu erstellen, zu bearbeiten und zu wählen.

Ab Windows NT Server 4.0 unterstützt das System die für Windows 95 beschriebenen Funktionen sowie eine Reihe zusätzlicher Funktionen, die eine Anwendung zum Arbeiten mit Telefonbüchern und Telefonbucheinträgen verwenden kann.

Die [**RasEntryDlg-Funktion**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) zeigt ein Eigenschaftenblatt an, das dem Benutzer das Erstellen, Bearbeiten oder Kopieren von Telefonbucheinträgen ermöglicht. Die Funktionen [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) und [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) rufen die **RasEntryDlg-Funktion** auf. Sie können die [**RasRenameEntry-Funktion**](/windows/desktop/api/Ras/nf-ras-rasrenameentrya) verwenden, um einen Telefonbucheintrag [**umzubenennen, oder rasDeleteEntry,**](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya) um einen Eintrag zu löschen. [**RasValidateEntryName**](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea) bestimmt, ob eine angegebene Zeichenfolge das richtige Format hat, das als Eintragsname verwendet werden soll.

Sie können [**die Eigenschaften RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) und [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) verwenden, um zusätzliche Informationen zu einem Telefonbucheintrag abzurufen und festzulegen. Diese Funktionen verwenden eine [**RASENTRY-Struktur.**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))

Die Funktionen [**RasGetCredentials**](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa) und [**RasSetCredentials**](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa) rufen die Benutzeranmeldeinformationen ab, die einem angegebenen RAS-Telefonbucheintrag zugeordnet sind, und legen sie fest. Diese Funktionen verwenden eine [**RASCREDENTIALS-Struktur.**](/previous-versions/windows/desktop/legacy/aa376730(v=vs.85))

Die [**RasGetCountryInfo-Funktion**](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa) ruft länder-/regionsspezifische Wählinformationen aus der Windows Telefonieliste der Länder ab. **RasGetCountryInfo** verwendet die [**RASCTRYINFO-Struktur.**](/previous-versions/windows/desktop/legacy/aa376731(v=vs.85))

**Windows 95: ** Unterstützt einen begrenzten Satz von Funktionen für die Arbeit mit Telefonbucheinträgen. Sie können die Funktionen [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) und [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) verwenden, um einen Telefonbucheintrag zu erstellen oder zu bearbeiten. Diese Funktionen zeigen ein Dialogfeld an, in dem der Benutzer Informationen zum Telefonbucheintrag angeben kann. Sie können die Funktionen [**RasGetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa) und [**RasSetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa) verwenden, um die Verbindungsparameter für einen Telefonbucheintrag festzulegen oder abzurufen. Die [**RasEnumEntries-Funktion**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) ruft ein Array von [**RASENTRYNAME-Strukturen**](/previous-versions/windows/desktop/legacy/aa377267(v=vs.85)) ab, die die Namen der Telefonbucheinträge enthalten.

 

 