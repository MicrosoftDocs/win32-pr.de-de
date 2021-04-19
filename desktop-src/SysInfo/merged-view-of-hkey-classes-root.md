---
description: Die regopenuserclassesroot-Funktion bietet eine zusammengeführte Ansicht für Prozesse, z. b. Dienste, die mit anderen Clients als dem interaktiven Benutzer in Zusammenhang stehen.
ms.assetid: 3815d487-2d58-4ba8-85d2-cae6a642a791
title: Zusammengeführte Ansicht von HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8597db976922db9ca348488b0092c41ba7c7489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366164"
---
# <a name="merged-view-of-hkey_classes_root"></a>Zusammengeführte Ansicht von HKEY- \_ Klassen Stamm \_

Die [**regopenuserclassesroot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) -Funktion bietet eine zusammengeführte Ansicht für Prozesse, z. b. Dienste, die mit anderen Clients als dem interaktiven Benutzer in Zusammenhang stehen. In diesem Fall bietet der Stamm Schlüssel der **HKEY- \_ \_ Klassen** eine Ansicht der Registrierung, mit der die Informationen aus den **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** mit den Informationen aus **aktuellen HKEY- \_ \_ Benutzer \\ Software \\ Klassen** zusammengeführt werden.

Das System verwendet die folgenden Regeln zum Zusammenführen von Informationen aus den beiden Quellen:

-   Die zusammengeführte Ansicht enthält alle untergeordneten Schlüssel des Schlüssels **HKEY \_ Current \_ User \\ Software \\ Classes** .
-   Die zusammengeführte Ansicht enthält alle unmittelbaren Unterschlüssel des Schlüssels der Schlüssel für **lokale HKEY- \_ \_ \\ \\ Computer** , die nicht die untergeordneten Schlüssel der **aktuellen HKEY- \_ \_ Benutzer \\ Software \\ Klassen** duplizieren.
-   Am Ende dieses Themas finden Sie eine Liste der Unterschlüssel, die sowohl in **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** als auch in **HKEY \_ Current \_ User- \\ Software \\ Klassen** enthalten sind. Die unmittelbaren Unterschlüssel dieser Schlüssel aus der HKEY-Struktur des **\_ lokalen \_** Computers sind nur in der zusammengeführten Ansicht enthalten, wenn es sich nicht um Duplikate von unmittelbaren unter Schlüsseln aus der **aktuellen HKEY- \_ \_ Benutzer** Struktur handelt. Die zusammengeführte Ansicht enthält nicht den **lokalen HKEY- \_ \_ Computer** Inhalt doppelter Unterschlüssel.

Wenn eine Anwendung mit Administratorrechten ausgeführt wird und die Benutzerkontensteuerung deaktiviert ist, ignoriert die com-Laufzeit die com-Konfiguration pro Benutzer und greift nur auf die com-Konfiguration pro Computer zu. Anwendungen, für die Administratorrechte erforderlich sind, sollten abhängige com-Objekte während der Installation im com-Konfigurations Speicher pro Computer (**HKEY \_ local \_ Machine \\ Software \\ Classes**) registrieren. Weitere Informationen finden Sie unter [AC: UAC: com-Per-User Konfiguration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 und Windows XP/2000:** Anwendungen können abhängige com-Objekte entweder für den pro-Computer-oder benutzerspezifischen com-Konfigurations Speicher (**HKEY \_ local \_ Machine \\ Software \\ Classes** oder **HKEY \_ Current \_ User \\ Software \\ Classes**) registrieren.

Das folgende Beispiel zeigt eine Reihe von unter Schlüsseln unter den aktuellen HKEY-Computern und **HKEY- \_ \_ Benutzer** Schlüsseln sowie die resultierende zusammengeführte Ansicht der **HKEY- \_ Klassen \_ root**. **\_ \_**

**HKEY \_ \_ \\ Software \\ Klassen für lokale Computer**    **CLSID**       *2*       *4*          **InProcServer32**          **LocalServer32**       *7*

**HKEY \_ Aktuelle \_ Benutzer \\ Software \\ Klassen**    **CLSID**       *1*       *4*          **LocalServer**       *6*       *10*          **LocalServer**

**HKEY \_ Klassen \_** Stamm-**CLSID***1**2**4***InProcServer32****LocalServer****LocalServer32***6**7**10***LocalServer**                                                                                      

Die folgenden Unterschlüssel finden Sie in den **HKEY \_ - \_ \\ Software \\ Klassen für lokale Computer** und in **HKEY- \_ \_ \\ Software \\ Klassen für aktuelle Benutzer**. Aus der **HKEY \_ \_** -Struktur des lokalen Computers sind die unmittelbaren Unterschlüssel dieser Schlüssel nur dann in der zusammengeführten Ansicht enthalten, wenn es sich nicht um Duplikate von unmittelbaren unter Schlüsseln aus der **aktuellen HKEY- \_ \_ Benutzer** Struktur handelt. Die zusammengeführte Ansicht enthält nicht den **lokalen HKEY- \_ \_ Computer** Inhalt doppelter Unterschlüssel.

**\**_ _*\*\\ shellex**  
**\*\\shellex \\ ContextMenuHandlers**  
**\*\\shellex \\ propertysheethandlers**  
**AppID**  
**CLSID**  
**Komponentenkategorien**  
**Laufwerk**  
**\\Shellex-Laufwerk**  
**\\Shellex \\ ContextMenuHandlers**  
**\\Shellex \\ propertysheethandlers**  
**FileType**  
**Ordner**  
**Ordner \\ shellex**  
**Ordner \\ shellex \\ columnhandler**  
**Ordner \\ shellex \\ ContextMenuHandlers**  
**Ordner \\ shellex \\ extshellfolderviews**  
**Ordner \\ shellex \\ propertysheethandlers**  
**Installer- \\ Komponenten**  
**Installer- \\ Funktionen**  
**Installer- \\ Produkte**  
**Interface**  
**Medi**  
**MIME- \\ Datenbank**  
**Charset der MIME- \\ Datenbank \\**  
**Codepage der MIME- \\ Datenbank \\**  
**MIME- \\ Daten Bank \\ Inhaltstyp**  
**Export der Typbibliothek**  


 

 
