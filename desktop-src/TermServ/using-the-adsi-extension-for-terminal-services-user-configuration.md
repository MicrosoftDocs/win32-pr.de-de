---
title: Verwenden der ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration
description: Die Verwaltung Remotedesktopdienste-spezifischen Benutzereigenschaften ist mithilfe der Methoden möglich, die von der Erweiterung Active Directory Service Interfaces (ADSI) implementiert werden, die mit der Dynamic Link Library Tsuserex.dll gepackt ist.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste mithilfe der ADSI-Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe63a725531c21b64ed0ac10abdeb4f710465532ab95f7c416c88f6142f1d55e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423690"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a>Verwenden der ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration

Die Active Directory-Dienstschnittstellenerweiterung (ACTIVE Directory Service Interfaces, ADSI) für Remotedesktopdienste Benutzerkonfiguration ist eine Bibliothek, die mit der Dynamic Link Library Tsuserex.dll gepackt ist. Die Verwaltung Remotedesktopdienste spezifischen Benutzereigenschaften ist mithilfe der von der Erweiterung implementierten Methoden möglich. Die Methoden ermöglichen die Konfiguration der Eigenschaften, die in der Erweiterungsschnittstelle für Remotedesktopdienste Benutzer verfügbar sind.

Die ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration unterstützt die Untersuchung und Bearbeitung Remotedesktopdienste in der Verzeichnisdienstdatenbank gespeicherten Benutzereigenschaften. Die Erweiterung unterstützt auch die Konfiguration von Benutzereigenschaften, die in Active Directory über die LDAP-API (Lightweight Directory Access Protocol) gespeichert werden.

Der Anbieter implementiert die folgenden Methoden:

-   [**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get). Diese Methode sucht in einer Instanz der -Klasse nach einer bestimmten Eigenschaft oder einem Bestimmten Satz von Eigenschaften.
-   [**IADs::P ut**](/windows/desktop/api/iads/nf-iads-iads-put). Diese Methode konfiguriert eine bestimmte Eigenschaft oder einen Bestimmten Satz von Eigenschaften für eine Instanz der -Klasse.

Eine Liste der spezifischen Remotedesktopdienste Benutzereigenschaften, die Sie konfigurieren können, finden Sie in der Referenz zur [ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration.](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md)

Weitere Informationen zum Zugreifen auf und Ändern von Attributen mit ADSI finden Sie unter [Zugreifen auf und Bearbeiten von Daten mit ADSI.](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi)

Weitere Informationen zur Verwendung von ADSI-Benennungskonventionen und AdsPath-Zeichenfolgen finden Sie in der Dokumentation zum [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform Software Development Kit (SDK) zu den einzelnen [ADSI-Dienstanbietern.](/windows/desktop/ADSI/adsi-system-providers)

 

 