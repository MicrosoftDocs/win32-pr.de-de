---
description: Sie können Registrierungsschlüssel in die Systemregistrierung schreiben, nachdem alle ausgewählten Komponenten und die zugehörigen Dateien installiert wurden.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Ändern der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6ff79ce340b0487c179cb37e44dff9f42e4be8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348528"
---
# <a name="modifying-the-registry"></a>Ändern der Registrierung

Sie können Registrierungsschlüssel in die Systemregistrierung schreiben, nachdem alle ausgewählten Komponenten und die zugehörigen Dateien installiert wurden. Die Standard Aktionen im Zusammenhang mit der Änderung der Registrierung müssen nach den Standard Aktionen für die Datei Installation sequenziert werden, da Registrierungsschlüssel nicht geschrieben werden können, es sei denn, die entsprechende Komponente und Datei wurde erfolgreich installiert.

Die [RegisterClassInfo-Aktion](registerclassinfo-action.md) greift auf die [Klassen Tabelle](class-table.md) zu, um die com-Klassen Informationen der installierten Komponenten zu registrieren.

Mit der [RegisterExtensionInfo-Aktion](registerextensioninfo-action.md) werden die [Erweiterungs Tabelle](extension-table.md) und die [Verb Tabelle](verb-table.md) abgefragt, und die entsprechenden Erweiterungen und Befehls-Verb-Informationen werden mit dem Betriebssystem registriert.

Mit der [registerprogidinfo-Aktion](registerprogidinfo-action.md) wird die Registrierung von OLE-ProgID-Informationen beim Betriebssystem verwaltet.

Die [registermimeinfo-Aktion](registermimeinfo-action.md) verarbeitet die [MIME-Tabelle](mime-table.md) , um die Zuordnung zwischen einem MIME-Kontexttyp, der Dateinamenerweiterung und der CLSID zu registrieren.

Die [Aktion "beschreiteregistryvalues](writeregistryvalues-action.md) " verarbeitet die [Registrierungs Tabelle](registry-table.md) und schreibt die Schlüssel für alle Komponenten, die entweder lokal oder aus der Quelle installiert wurden. In der Registrierungs Tabelle können Schlüssel in die Registrierungs Strukturen der **HKEY- \_ Klassen \_ root**, **HKEY \_ Current \_ User**, **HKEY \_ local \_ Machine** und **HKEY \_ Users** geschrieben werden.

Mit der [Aktion removeregistryvalues](removeregistryvalues-action.md) werden die Schlüssel, die zum Löschen markiert wurden, in der Spalte Name der [Registrierungs Tabelle](registry-table.md) oder der [Tabelle removeregistry](removeregistry-table.md)entfernt.

Die [Aktion registertypelibraries](registertypelibraries-action.md) verarbeitet die [typelib-Tabelle](typelib-table.md) und registriert die installierten Typbibliotheken beim System.

 

 



