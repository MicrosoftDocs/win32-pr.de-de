---
description: Registrierungsschlüssel können in die Systemregistrierung geschrieben werden, nachdem alle ausgewählten Komponenten und die zugehörigen Dateien installiert wurden.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Ändern der Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f1bd6145811097fcaf74f0622ac35412891d6aa0007c4411099ade6afddd36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082860"
---
# <a name="modifying-the-registry"></a>Ändern der Registrierung

Registrierungsschlüssel können in die Systemregistrierung geschrieben werden, nachdem alle ausgewählten Komponenten und die zugehörigen Dateien installiert wurden. Die Standardaktionen im Zusammenhang mit dem Ändern der Registrierung müssen nach den Standardaktionen für die Dateiinstallation sequenziert werden, da Registrierungsschlüssel nur geschrieben werden können, wenn die entsprechende Komponente und Datei erfolgreich installiert wurden.

Die [RegisterClassInfo-Aktion](registerclassinfo-action.md) greift auf die [Klassentabelle](class-table.md) zu, um die COM-Klasseninformationen der installierten Komponenten zu registrieren.

Die [Aktion RegisterExtensionInfo](registerextensioninfo-action.md) fragt die [Erweiterungstabelle](extension-table.md) und die [Verbtabelle](verb-table.md) ab und registriert die entsprechenden Erweiterungen und Befehlsverbinformationen beim Betriebssystem.

Die [RegisterProgIdInfo-Aktion](registerprogidinfo-action.md) verwaltet die Registrierung von OLE ProgId-Informationen beim Betriebssystem.

Die [RegisterMIMEInfo-Aktion](registermimeinfo-action.md) verarbeitet die [MIME-Tabelle,](mime-table.md) um die Zuordnung zwischen einem MIME-Kontexttyp, der Dateinamenerweiterung und der CLSID zu registrieren.

Die [WriteRegistryValues-Aktion](writeregistryvalues-action.md) verarbeitet die [Registrierungstabelle](registry-table.md) und schreibt die Schlüssel für alle Komponenten, die entweder lokal installiert wurden oder aus der Quelle ausgeführt werden sollen. Die Registrierungstabelle ermöglicht das Schreiben von Schlüsseln in die Registrierungsstrukturen **"HKEY \_ CLASSES \_ ROOT",** **"HKEY \_ CURRENT \_ USER",** **"HKEY \_ LOCAL \_ MACHINE"** und **"HKEY \_ USERS".**

Die [RemoveRegistryValues-Aktion](removeregistryvalues-action.md) entfernt die Schlüssel, die in der Spalte Name der Registrierungstabelle oder der [RemoveRegistry-Tabelle](removeregistry-table.md)als gelöscht markiert wurden. [](registry-table.md)

Die [RegisterTypeLibraries-Aktion](registertypelibraries-action.md) verarbeitet die [TypeLib-Tabelle](typelib-table.md) und registriert die installierten Typbibliotheken beim System.

 

 



