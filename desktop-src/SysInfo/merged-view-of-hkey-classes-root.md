---
description: Die RegOpenUserClassesRoot-Funktion stellt eine zusammengeführte Ansicht für Prozesse wie Dienste zur Verfügung, die andere Clients als den interaktiven Benutzer verwenden.
ms.assetid: 3815d487-2d58-4ba8-85d2-cae6a642a791
title: Zusammengeführte Ansicht HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52b48be32ec524cdac42808d7f4efddfc78854b56133e647d6f5a9b06ae88bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885418"
---
# <a name="merged-view-of-hkey_classes_root"></a>Zusammengeführte Ansicht von HKEY \_ CLASSES \_ ROOT

Die [**RegOpenUserClassesRoot-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) stellt eine zusammengeführte Ansicht für Prozesse wie Dienste zur Verfügung, die andere Clients als den interaktiven Benutzer verwenden. In diesem Fall bietet der **HKEY \_ CLASSES \_ ROOT-Schlüssel** eine Ansicht der Registrierung, in der die Informationen aus **HKEY \_ LOCAL MACHINE \_ Software \\ \\ Classes** mit den Informationen aus **HKEY CURRENT USER Software \_ Classes zusammengeführt \_ \\ \\ werden.**

Das System verwendet die folgenden Regeln, um Informationen aus den beiden Quellen zusammen zu führen:

-   Die zusammengeführte Ansicht enthält alle Unterschlüssel des **Schlüssels HKEY \_ CURRENT USER Software \_ \\ \\ Classes.**
-   Die zusammengeführte Ansicht enthält alle unmittelbaren Unterschlüssel des **HKEY \_ LOCAL MACHINE Software \_ \\ Classes-Schlüssels, \\** die die Unterschlüssel von **HKEY CURRENT USER \_ Software Classes \_ nicht \\ duplizieren. \\**
-   Am Ende dieses Themas finden Sie eine Liste der Unterschlüssel, die sich sowohl in den **HKEY \_ LOCAL \_ \\ MACHINE-Softwareklassen \\** als auch in **den HKEY CURRENT USER Software \_ Classes \_ \\ \\ befinden.** Die unmittelbaren Unterschlüssel dieser Schlüssel aus der **HKEY \_ LOCAL \_ MACHINE-Struktur** sind nur in der zusammengeführten Ansicht enthalten, wenn sie keine Duplikate von unmittelbaren Unterschlüsseln aus der **HKEY \_ CURRENT \_ USER-Struktur** sind. Die zusammengeführte Sicht enthält nicht den **HKEY \_ LOCAL \_ MACHINE-Inhalt** doppelter Unterschlüssel.

Wenn eine Anwendung mit Administratorrechten ausgeführt wird und die Benutzerkontensteuerung deaktiviert ist, ignoriert die COM-Runtime die BENUTZERSPEZIFISCHE COM-Konfiguration und greifen nur auf die COMPUTER-spezifische COM-Konfiguration zu. Anwendungen, die Administratorrechte erfordern, sollten abhängige COM-Objekte während der Installation im COM-Konfigurationsspeicher pro Computer registrieren (**HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes**). Weitere Informationen finden Sie unter [AC: UAC: COM Per-User Configuration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 und Windows XP/2000:** Anwendungen können abhängige COM-Objekte entweder im COMPUTER- oder benutzerspezifischen COM-Konfigurationsspeicher registrieren (**HKEY \_ LOCAL \_ \\ MACHINE-Softwareklassen \\** oder **HKEY \_ CURRENT USER \_ Software \\ \\ Classes**).

Das folgende Beispiel zeigt eine Reihe von Unterschlüsseln unter den **Schlüsseln HKEY \_ LOCAL \_ MACHINE** und **HKEY \_ CURRENT \_ USER** sowie die resultierende zusammengeführte Ansicht von **HKEY CLASSES \_ \_ ROOT**.

**HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE-Klassen**    **CLSID**       *2*       *4*          **inprocserver32**          **localserver32**       *7*

**HKEY \_ CURRENT \_ USER \\ Software \\ Classes**    **CLSID**       *1*       *4*          **localserver**       *6*       *10*          **localserver**

**HKEY \_ CLASSES \_ ROOT****CLSID***1 2**4***inprocserver32****localserver localserver32***6**7**10***localserver**                                                                                      

Die folgenden Unterschlüssel befinden sich sowohl in **den HKEY \_ LOCAL \_ \\ MACHINE-Softwareklassen \\** als auch in **den HKEY CURRENT \_ \_ \\ USER-Softwareklassen. \\** In der **HKEY \_ LOCAL \_ MACHINE-Struktur** sind die unmittelbaren Unterschlüssel dieser Schlüssel nur dann in der zusammengeführten Ansicht enthalten, wenn sie keine Duplikate von unmittelbaren Unterschlüsseln aus der **HKEY \_ CURRENT \_ USER-Struktur** sind. Die zusammengeführte Sicht enthält nicht den **HKEY \_ LOCAL \_ MACHINE-Inhalt** doppelter Unterschlüssel.

**\***  
**\*\\shellex**  
**\*\\shellex \\ ContextMenuHandlers**  
**\*\\shellex \\ PropertySheetHandlers**  
**AppID**  
**Clsid**  
**Komponentenkategorien**  
**Laufwerk**  
**\\Laufwerkshellex**  
**Drive \\ shellex \\ ContextMenuHandlers**  
**Drive \\ shellex \\ PropertySheetHandlers**  
**FileType**  
**Ordner**  
**\\Ordnershellex**  
**\\Ordnershellex \\ ColumnHandler**  
**\\Ordnershellex \\ ContextMenuHandlers**  
**\\Ordnershellex \\ ExtShellFolderViews**  
**Folder \\ shellex \\ PropertySheetHandlers**  
**\\Installer-Komponenten**  
**\\Installerfeatures**  
**\\Installer-Produkte**  
**Interface**  
**Mime**  
**\\Mime-Datenbank**  
**Mime \\ Database \\ Charset**  
**Mime \\ Database \\ Codepage**  
**\\ \\ Mime-Datenbankinhaltstyp**  
**Typelib**  


 

 
