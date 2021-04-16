---
description: Wenn das Computersystem gestartet wird, werden von der lokalen Sicherheits Autorität (Local Security Authority, LSA) automatisch alle registrierten Security Support Provider-/Authentifizierungspaket-DLLs (SSP/AP) in den Prozessbereich geladen. Die folgenden Abbildungen zeigen den Initialisierungs Prozess.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: LSA-ModusInitialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4212a584d290e67c6465488c8398604db2c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529741"
---
# <a name="lsa-mode-initialization"></a>LSA-ModusInitialisierung

Wenn das Computersystem gestartet wird, lädt die [*Lokale Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA [](../secgloss/s-gly.md)) automatisch alle registrierten / SSP/AP-DLLs (Security Support Provider [*Authentication Package*](../secgloss/a-gly.md) ) in den Prozessbereich. Die folgenden Abbildungen zeigen den Initialisierungs Prozess.

> [!Note]  
> "Kerberos" stellt den Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP dar, und "My SSP/AP" stellt einen benutzerdefinierten SSP/AP dar, der zwei benutzerdefinierte Sicherheitspakete enthält.

 

![LSA-ModusInitialisierung](images/lsamode1.png)

Beim Start Ruft die LSA die Funktion " [**splsamodeinitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) " in jedem SSP/AP auf, um Zeiger auf die Funktionen zu erhalten, die von den einzelnen [*Sicherheitspaketen*](../secgloss/s-gly.md) in der dll implementiert werden. Die Funktionszeiger werden an die LSA in einem Array von Tabellenstrukturen der [**secpkg- \_ Funktion \_**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) übergeben.

![der LSA ruft "splsamodeinitialize" auf, um Funktionszeiger zu erhalten.](images/lsamode2.png)

Nachdem der Satz von Tabellenstrukturen der [**secpkg- \_ Funktion \_**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) empfangen wurde, ruft die LSA die [**spinitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) -Funktion jedes Sicherheitspakets auf. Der LSA verwendet diesen Funktions aufrufsbefehl, um jedes Sicherheitspaket an eine [**LSA \_ secpkg- \_ Funktions \_ Tabellen**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) Struktur zu übergeben, die Zeiger auf die LSA-Unterstützungsfunktionen enthält, die für Sicherheitspakete verfügbar sind. Zusätzlich zum Speichern der Zeiger auf die LSA-Unterstützungsfunktionen sollten benutzerdefinierte Sicherheitspakete Ihre Implementierung der **spinitialize** -Funktion verwenden, um eine Initialisierungs bezogene Verarbeitung auszuführen.

Eine Liste der LSA-Unterstützungsfunktionen, die für Sicherheitspakete im LSA-Modus verfügbar sind, finden Sie unter [LSA-Funktionen, die von SSP/APS aufgerufen](authentication-functions.md)werden.

Informationen zum Registrieren einer SSP/AP-dll finden Sie unter [Registrieren von SSP/AP-DLLs](registering-ssp-ap-dlls.md).

 

 
