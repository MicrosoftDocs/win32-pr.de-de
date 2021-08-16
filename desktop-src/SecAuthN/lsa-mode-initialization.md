---
description: Wenn das Computersystem gestartet wird, lädt die lokale Sicherheitsautorität (LSA) automatisch alle registrierten SSP/AP-DLLs (Security Support Provider/Authentication Package) in den Prozessbereich. Die folgenden Abbildungen zeigen den Initialisierungsprozess.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: Initialisierung des LSA-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4c55397e5970b8401e1429eba7d92a034e76ce0c999950131167580ded7e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922128"
---
# <a name="lsa-mode-initialization"></a>Initialisierung des LSA-Modus

Wenn das Computersystem gestartet wird, lädt die [*lokale Sicherheitsautorität*](../secgloss/l-gly.md) (LSA) automatisch alle registrierten SSP/AP-DLLs [*(Security Support Provider*](../secgloss/s-gly.md)Authentication / [*Package)*](../secgloss/a-gly.md) in den Prozessbereich. Die folgenden Abbildungen zeigen den Initialisierungsprozess.

> [!Note]  
> "Kerberos" stellt [](../secgloss/k-gly.md) den Microsoft Kerberos-SSP/AP dar, und "My SSP/AP" stellt einen benutzerdefinierten SSP/AP dar, der zwei benutzerdefinierte Sicherheitspakete enthält.

 

![Initialisierung des lsa-Modus](images/lsamode1.png)

Beim Start ruft der LSA die [**SpLsaModeInitialize-Funktion**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) in jedem SSP/AP auf, um Zeiger auf die Funktionen abzurufen, die von den einzelnen [*Sicherheitspaketen*](../secgloss/s-gly.md) in der DLL implementiert werden. Die Funktionszeiger werden an die LSA in einem Array von [**SECPKG \_ FUNCTION \_ TABLE-Strukturen**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) übergeben.

![der lsa ruft splsamodeinitialize auf, um Funktionszeiger abzurufen.](images/lsamode2.png)

Nach dem Empfang der [**SECPKG \_ FUNCTION \_ TABLE-Strukturen**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) ruft der LSA die [**SpInitialize-Funktion**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) jedes Sicherheitspakets auf. Der LSA verwendet diesen Funktionsaufruf, um jedem Sicherheitspaket eine [**LSA \_ SECPKG \_ FUNCTION \_ TABLE-Struktur**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) zu übergeben, die Zeiger auf die LSA-Unterstützungsfunktionen enthält, die für Sicherheitspakete verfügbar sind. Zusätzlich zum Speichern der Zeiger auf die LSA-Unterstützungsfunktionen sollten benutzerdefinierte Sicherheitspakete ihre Implementierung der **SpInitialize-Funktion** verwenden, um eine initialisierungsbezogene Verarbeitung durchzuführen.

Eine Liste der LSA-Unterstützungsfunktionen, die für LSA-Modussicherheitspakete verfügbar sind, finden Sie unter [LSA-Funktionen, die von SSP/APs aufgerufen werden.](authentication-functions.md)

Informationen zum Registrieren einer SSP/AP-DLL finden Sie unter [Registrieren von SSP-/AP-DLLs.](registering-ssp-ap-dlls.md)

 

 
