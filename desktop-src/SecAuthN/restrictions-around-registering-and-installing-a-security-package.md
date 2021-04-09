---
description: Aktionen von Sicherheitspaketen, die in Windows nicht unterstützt werden.
ms.assetid: E2BF8041-DF2F-4282-A3CC-A15FF2D7F4A2
title: Einschränkungen bei der Registrierung und Installation eines Sicherheitspakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd10cd8e2e98d4dccfc3a6230c3daecaeb8fec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749609"
---
# <a name="restrictions-around-registering-and-installing-a-security-package"></a>Einschränkungen bei der Registrierung und Installation eines Sicherheitspakets

Das entfernen, ersetzen oder Umpacken von Posteingang-Sicherheitspaketen (z. b. Kerberos oder NTLM) wird in Windows nicht unterstützt, und ab dem 10. Januar 2017 wird dies verhindert. Sicherheitspakete von Drittanbietern (SSPs/APS) können hinzugefügt werden. Windows unterstützt jedoch nicht das Entfernen vorkonfigurierter SSPs/APS. Insbesondere wird die Bearbeitung der Registrierungs Einstellung für das **HKLM- \\ System \\ CurrentControlSet \\ Control \\ LSA \\ osconfig \\ Security Packages** nie unterstützt.

Ab Windows 8.1 können Kunden, die zusätzliche Funktionen bereitstellen möchten, ihre Sicherheitspakete mithilfe der Registrierungs Einstellung **HKLM \\ System \\ CurrentControlSet \\ Control \\ LSA \\ Security Packages** (Registrieren von [SSP/AP-DLLs](registering-ssp-ap-dlls.md)) und der zugehörigen Registrierungs Einstellung **SecurityProviders** ([schreiben und Installieren eines Sicherheits Unterstützungs Anbieters](writing-and-installing-a-security-support-provider.md)) hinzufügen, falls zutreffend. Der Zweck von [Sicherheitspaketen](../secgloss/s-gly.md#_security_security_package_gly) besteht darin, neue *Sicherheitsprotokolle* zu implementieren, die in Form eines Security Support Provider (SSP) oder eines [Authentifizierungs Pakets](../secgloss/a-gly.md#_security_authentication_package_gly) (AP) vorliegen können. Der Zweck eines SSP besteht darin, *authentifizierte Verbindungs*-, *Nachrichten Integritäts*-und *Nachrichten Verschlüsselungsdienste* bereitzustellen, die im System nicht bereits unterstützt werden, während ein Zugriffspunkt verwendet wird, um eine neue *Authentifizierungs Logik* hinzuzufügen, mit der bestimmt wird, ob sich ein Benutzer anmelden kann.

Microsoft ist in die Kunden Sicherheit investiert und versucht sicherzustellen, dass kritische Prozesse wie SSPs und APS nicht einfach aus dem System entfernt werden können. Daher wurde die Registrierungs Einstellung für das **HKLM- \\ System \\ CurrentControlSet \\ Control \\ LSA \\ osconfig \\ Security Packages** auf Windows 8.1 eingeschränkt, um Änderungen zu verhindern. Um Sicherheitspakete von Drittanbietern zu vereinfachen, wurde das **HKLM \\ System \\ CurrentControlSet \\ Control \\ LSA \\ Security Packages** als festgelegte Einstellung für benutzerdefinierte SSPs/APS festgelegt. Es wird ferner empfohlen, dass sämtliche Funktionen in benutzerdefinierten SSPs/APS, die außerhalb des Bereichs der von Microsoft definierten Sicherheitspakete liegen, aus solchen benutzerdefinierten SSPs/APS entfernt werden, und dass die Posteingang-Sicherheitspakete von keinem Produkt entfernt werden.

 

 
