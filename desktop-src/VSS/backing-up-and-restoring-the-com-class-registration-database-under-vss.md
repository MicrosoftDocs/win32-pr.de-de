---
description: Der Component Object Model (com) ist ein binärer Standard zum Schreiben von Komponenten Software in einer verteilten Computerumgebung.
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: Sichern und Wiederherstellen der com+-Klassen Registrierungsdatenbank unter VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae21489330693f0ce0d23b8639507121b9b00302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362981"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a>Sichern und Wiederherstellen der com+-Klassen Registrierungsdatenbank unter VSS

Der Component Object Model (com) ist ein binärer Standard zum Schreiben von Komponenten Software in einer verteilten Computerumgebung.

In der ursprünglichen Win32-Implementierung wurden die Komponenten Bezeichner (GUIDs) und ein anderer com-Zustand in der Registrierung unter **HKEY \_ Classes \_ root \\ CLSID** gespeichert.

Die aktuelle Generierung der Component Object Model com+ bietet eine Registrierungs unabhängige Datenbank zum Speichern von Komponenten Registrierungsinformationen: der com+-Klassen Registrierungsdatenbank.

Die com+-Klassen Registrierungsdatenbank unterstützt eine VSS Writer, mit der Anforderer die Registrierungsdatenbank mithilfe von Daten sichern kann, die auf einem schattenkopierten Volume gespeichert sind.

Zum Wiederherstellen der COM+-Registrierungsdatenbank muss ein Anforderer die [icomadmincatalog:: restoreregdb](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) -Methode abrufen.

Weitere Informationen zum Registrierungs-Writer für die com+-Registrierung finden Sie unter [in-Box-VSS-](in-box-vss-writers.md)Writer.

 

 
