---
description: Das Erstellen eines Dialog Felds in Windows Installer ähnelt dem Prozess der programmgesteuerten Erstellung eines Dialog Felds mithilfe einer Microsoft Windows-API-Dialogfeld Vorlage.
ms.assetid: c46f6b7b-e78c-4dd8-a4ff-7da5465391f9
title: Dialog Feld Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884c85f06bc06588084311aee370700d5b2a5290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346338"
---
# <a name="dialog-box-overview"></a>Dialog Feld Übersicht

Das Erstellen eines Dialog Felds in Windows Installer ähnelt dem Prozess der programmgesteuerten Erstellung eines Dialog Felds mithilfe einer Microsoft Windows-API-Dialogfeld Vorlage. Während eine Windows-Dialogfeld Vorlage in einer null-terminierten –-Zeichenfolge gespeichert wird, speichert Windows Installer die Dialogfeld Parameter in der Dialogfeld Tabelle. Die Dialog Feld Tabelle enthält eine Spalte Attribute, die analog zu Fenster Stilen in der Microsoft Windows-API für die Benutzeroberfläche ist. Die Anzahl der Dialogfeld Stil-Bits in Windows Installer ist jedoch ein reduzierter und spezieller Satz.

Um das Dialogfeld mithilfe der API der Windows-Benutzeroberfläche physisch zu erstellen, wird [**Dialogbox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) aufgerufen und übergibt einen Zeiger auf die Vorlage. In Windows Installer wird das Dialogfeld während der Ausführung einer der drei UI-Sequenz Tabellen erstellt.

Windows Installer enthält keine Standardbenutzer Oberfläche, die Paket Autoren für Ihre Pakete verwenden können. Sie enthält einen begrenzten Satz von Standard Dialogfeldern, die Fehler-und Informationsmeldungen anzeigen. Diese werden jedoch nur angezeigt, wenn Windows Installer die Dialog-und UI-Sequenz Tabellen abfragt und feststellt, dass keine benutzerdefinierten Dialogfelder verfügbar sind.

Das Installer SDK enthält eine minimale Datenbank mit dem Namen Uisample.msi, die die Tabellen für die Benutzeroberfläche und die Ausführungssequenz sowie eine vollständige Benutzeroberfläche enthält Diese Datenbank kann problemlos angepasst und mit einem beliebigen Paket zusammengeführt werden.

Einige Standard Aktionen und interne Windows Installer Fehlerbedingungen geben einen bestimmten Satz von Benutzeroberflächen Daten zurück und benötigen daher ein Dialogfeld mit einer bestimmten Gruppe von Steuerelementen, um diese Daten zu unterstützen. Windows Installer überprüft zwei separate Speicherorte für die Bezeichner für diese Dialogfelder.

-   Windows Installer enthält einen Satz von eingebetteten Dialogfeld Namen. Die benutzerdefinierte Aktion fragt die Dialog Tabelle nach diesen reservierten Namen ab.
-   In jeder der drei UI-Sequenz Tabellen werden Dialog Namen mit der Sequenznummer-1,-2 oder-3 als Reaktion auf beenden, vom Benutzer angeforderte Beendigung und schwerwiegende Fehlermeldungen aus Windows Installer angezeigt.

Eine komplette Liste der Namen der reservierten Primärschlüssel Dialogfelder finden Sie in den [Dialogfeldern](dialog-boxes.md). Beachten Sie, dass der Name des Primärschlüssel-Dialog Felds nur vom Installationsprogramm reserviert wird und in Windows Installer keine bestimmte Implementierung des Dialog Felds vorhanden ist. Paket Autoren müssen weiterhin alle Felder in der Datenbank auffüllen, die die Attribute und Steuerelemente dieser reservierten Dialogfelder angeben.

 

 
