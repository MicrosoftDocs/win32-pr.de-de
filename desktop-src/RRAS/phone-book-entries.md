---
title: Phone-Book Einträge
description: Telefonbucheinträge enthalten die Informationen, die zum Herstellen einer RAS-Verbindung erforderlich sind. Ein Benutzer oder Administrator kann das Dialogfeld "Einwählnetzwerk" verwenden, um Telefonbucheinträge zu erstellen, zu bearbeiten und zu wählen.
ms.assetid: 971d7020-f9fd-42d1-97c3-79ad6eba6964
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cc01e66b5877c90b81610a5d8cf151b7cb7bd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102134"
---
# <a name="phone-book-entries"></a>Phone-Book Einträge

Telefonbucheinträge enthalten die Informationen, die zum Herstellen einer RAS-Verbindung erforderlich sind. Ein Benutzer oder Administrator kann das Dialogfeld " **Einwählnetzwerk** " verwenden, um Telefonbucheinträge zu erstellen, zu bearbeiten und zu wählen.

Ab Windows NT Server 4,0 unterstützt das System die Funktionen, die für Windows 95 beschrieben werden, sowie eine Reihe zusätzlicher Funktionen, die eine Anwendung verwenden kann, um mit Telefonbüchern und Telefonbucheinträgen zu arbeiten.

Die Funktion " [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) " zeigt ein Eigenschaften Blatt an, das es dem Benutzer ermöglicht, Telefonbucheinträge zu erstellen, zu bearbeiten oder zu kopieren. Die Funktionen " [**rascreatephonebookentry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) " und " [**raseditphonebookentry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) " aufrufen die " **RasEntryDlg** "-Funktion. Sie können die Funktion " [**rasrenameentry**](/windows/desktop/api/Ras/nf-ras-rasrenameentrya) " verwenden, um einen Telefonbucheintrag umzubenennen, oder " [**rasdeleteentry**](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya) ", um einen Eintrag zu löschen. Der " [**rasvalidateentryname**](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea) " bestimmt, ob eine angegebene Zeichenfolge das richtige Format hat, das als Eingabe Name verwendet werden soll.

Sie können die Eigenschaften " [**rasgetentryproperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) " und " [**rassetentryproperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) " verwenden, um zusätzliche Informationen zu einem Telefonbucheintrag zu erhalten und festzulegen. Diese Funktionen verwenden eine [**rasentry**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) -Struktur.

Mit den Funktionen " [**rasgetanmeldeinformationen**](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa) " und " [**rassetanmelde**](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa) Informationen" werden die einem angegebenen RAS-Telefonbucheintrag zugeordneten Anmelde Informationen abgerufen und festgelegt Diese Funktionen verwenden eine [**rascreden-**](/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)) Struktur.

Die Funktion " [**rasgetcountryinfo**](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa) " ruft Länder-/Regions spezifische Informationen aus der Windows-telefonieliste von Ländern ab. **Rasgetcountryinfo** verwendet die [**rasctryinfo**](/previous-versions/windows/desktop/legacy/aa376731(v=vs.85)) -Struktur.

**Windows 95:  ** Unterstützt eine begrenzte Anzahl von Funktionen zum Arbeiten mit Telefonbucheinträgen. Sie können die Funktionen " [**rascreatephonebookentry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) " und " [**raseditphonebookentry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) " verwenden, um einen Telefonbucheintrag zu erstellen oder zu bearbeiten. Diese Funktionen zeigen ein Dialogfeld an, in dem der Benutzerinformationen über den Telefonbucheintrag angeben kann. Sie können die Funktionen " [**rasgetentrydialparameams**](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa) " und " [**rassetentrydialparameams**](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa) " verwenden, um die Verbindungsparameter für einen Telefonbucheintrag festzulegen oder abzurufen. Die Funktion " [**rasenenumentries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) " Ruft ein Array von " [**rasentryname**](/previous-versions/windows/desktop/legacy/aa377267(v=vs.85)) "-Strukturen ab, die die Namen der Telefonbucheinträge enthalten.

 

 