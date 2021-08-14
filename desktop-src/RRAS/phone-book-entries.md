---
title: Phone-Book Einträge
description: Telefon-Book-Einträge enthalten die Informationen, die zum Herstellen einer RAS-Verbindung erforderlich sind. Ein Benutzer oder Administrator kann das Dialogfeld DFÜ-Netzwerk, um Telefonbucheinträge zu erstellen, zu bearbeiten und zu wählen.
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

Telefon-Book-Einträge enthalten die Informationen, die zum Herstellen einer RAS-Verbindung erforderlich sind. Ein Benutzer oder Administrator kann das Dialogfeld **DFÜ-Netzwerk,** um Telefonbucheinträge zu erstellen, zu bearbeiten und zu wählen.

Ab Windows NT Server 4.0 unterstützt das System die für Windows 95 beschriebenen Funktionen sowie eine Reihe zusätzlicher Funktionen, die eine Anwendung zum Arbeiten mit Telefonbüchern und Telefonbucheinträgen verwenden kann.

Die [**RasEntryDlg-Funktion**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) zeigt ein Eigenschaftenblatt an, das es dem Benutzer ermöglicht, Telefonbucheinträge zu erstellen, zu bearbeiten oder zu kopieren. Die [**Funktionen RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) und [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) rufen die **RasEntryDlg-Funktion** auf. Sie können die [**RasRenameEntry-Funktion**](/windows/desktop/api/Ras/nf-ras-rasrenameentrya) verwenden, um einen Telefonbucheintrag umzubenennen, oder [**RasDeleteEntry,**](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya) um einen Eintrag zu löschen. [**RasValidateEntryName**](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea) bestimmt, ob eine angegebene Zeichenfolge das richtige Format hat, das als Eintragsname verwendet werden soll.

Sie können [**rasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) und [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) verwenden, um zusätzliche Informationen zu einem Telefonbucheintrag zu erhalten und fest zu legen. Diese Funktionen verwenden eine [**RASENTRY-Struktur.**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85))

Die [**Funktionen RasGetCredentials**](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa) und [**RasSetCredentials**](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa) erhalten und legen die Benutzeranmeldeinformationen fest, die einem angegebenen RAS-Telefonbucheintrag zugeordnet sind. Diese Funktionen verwenden eine [**RASCREDENTIALS-Struktur.**](/previous-versions/windows/desktop/legacy/aa376730(v=vs.85))

Die [**RasGetCountryInfo-Funktion**](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa) ruft länder-/regionspezifische Wählinformationen aus der Windows Telefonieliste der Länder ab. **RasGetCountryInfo verwendet** die [**RASCTRYINFO-Struktur.**](/previous-versions/windows/desktop/legacy/aa376731(v=vs.85))

**Windows 95: ** Unterstützt einen begrenzten Satz von Funktionen für die Arbeit mit Telefonbucheinträgen. Sie können die Funktionen [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) und [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) verwenden, um einen Telefonbucheintrag zu erstellen oder zu bearbeiten. Diese Funktionen zeigen ein Dialogfeld an, in dem der Benutzer Informationen zum Telefonbucheintrag angeben kann. Mithilfe der [**Funktionen RasGetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa) und [**RasSetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa) können Sie die Verbindungsparameter für einen Telefonbucheintrag festlegen oder abrufen. Die [**RasEnumEntries-Funktion**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) ruft ein Array von [**RASENTRYNAME-Strukturen**](/previous-versions/windows/desktop/legacy/aa377267(v=vs.85)) ab, die die Telefonbucheintragsnamen enthalten.

 

 