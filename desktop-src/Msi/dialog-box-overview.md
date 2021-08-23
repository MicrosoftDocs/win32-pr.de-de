---
description: Das Erstellen eines Dialogfelds in Windows Installer ähnelt dem programmgesteuerten Erstellen eines Dialogfelds mithilfe einer Dialogfeldvorlage für die Microsoft Windows-API.
ms.assetid: c46f6b7b-e78c-4dd8-a4ff-7da5465391f9
title: Übersicht über das Dialogfeld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a17963148100d8f0d99a6fdb9e043654e089880b81ade0a943b92b4bfcd35f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764170"
---
# <a name="dialog-box-overview"></a>Übersicht über das Dialogfeld

Das Erstellen eines Dialogfelds in Windows Installer ähnelt dem programmgesteuerten Erstellen eines Dialogfelds mithilfe einer Dialogfeldvorlage für die Microsoft Windows-API. Während eine Windows Dialogfeldvorlage in einer null-Terminzeichenfolge gespeichert wird, speichert Windows Installer die Dialogfeldparameter in der Tabelle Dialog. Die Tabelle Dialog enthält eine Attributspalte, die den Fensterstilen in der Microsoft Windows-Benutzeroberfläche entspricht. Die Anzahl der Dialogformatbits in Windows Installer ist jedoch ein reduzierter und spezialisierter Satz.

Zum physischen Erstellen des Dialogfelds mithilfe der Windows-Api für die Benutzeroberfläche wird [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) aufgerufen und übergibt einen Zeiger auf die Vorlage. In Windows Installer wird das Dialogfeld während der Ausführung einer der drei Ui-Sequenztabellen erstellt.

Windows Das Installationsprogramm enthält keine Standardbenutzeroberfläche, die Paketautoren für ihre Pakete verwenden können. Sie enthält eine begrenzte Anzahl von Standarddialogfeldern, die Fehler- und Informationsmeldungen anzeigen. Diese werden jedoch nur angezeigt, wenn Windows Installer die Tabellen Dialog und UI Sequence abfragt und feststellt, dass keine benutzerdefinierten Dialogfelder verfügbar sind.

Das Installationsprogramm-SDK enthält eine minimale Datenbank mit dem Namen Uisample.msi, die aufgefüllte Ui- und Ausführungssequenztabellen sowie eine vollständige Benutzeroberfläche enthält. Diese Datenbank kann problemlos angepasst und mit einem beliebigen Paket zusammengeführt werden.

Einige Standardaktionen und interne Windows Installer-Fehlerbedingungen geben einen bestimmten Satz von Benutzeroberflächendaten zurück und erfordern daher ein Dialogfeld mit einem bestimmten Satz von Steuerelementen, um diese Daten aufzunehmen. Windows Das Installationsprogramm überprüft zwei separate Speicherorte auf die Bezeichner für diese Dialogfelder.

-   Windows Das Installationsprogramm enthält einen Satz eingebetteter Dialogfeldnamen. Die benutzerdefinierte Aktion fragt die Tabelle Dialog nach diesen reservierten Namen ab.
-   In jeder der drei Ui-Sequenztabellen werden Dialognamen mit der Sequenznummer -1,-2 oder -3 als Antwort auf das Beenden, vom Benutzer angeforderte Beendigung und schwerwiegende Fehlermeldungen von Windows Installer angezeigt.

Eine vollständige Liste der Namen reservierter Primärschlüsseldialogfelder ist in [den Dialogfeldern](dialog-boxes.md)verfügbar. Beachten Sie, dass der Name des Primärschlüsseldialogfelds nur vom Installationsprogramm reserviert wird und es keine spezifische Implementierung des Dialogfelds innerhalb Windows Installers gibt. Paketautoren müssen weiterhin alle Felder in der Datenbank auffüllen, die die Attribute und Steuerelemente dieser reservierten Dialogfelder angeben.

 

 
