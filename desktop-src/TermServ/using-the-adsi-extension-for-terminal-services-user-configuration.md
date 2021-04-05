---
title: Verwenden der ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration
description: Die Verwaltung Remotedesktopdienste spezifischer Benutzereigenschaften ist möglich, indem die von der ADSI-Erweiterung (Active Directory Service Interfaces) implementierten Methoden verwendet werden, die mit der Dynamic Link Library-Tsuserex.dll verpackt werden.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste mit der ADSI-Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f115fecf1cce5c518e93206402f76e077109611
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949046"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a>Verwenden der ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration

Die ADSI-Erweiterung (Active Directory Service Interfaces) für Remotedesktopdienste Benutzerkonfiguration ist eine Bibliothek, die mit der Tsuserex.dll der Dynamic Link Library verpackt ist. Die Verwaltung Remotedesktopdienste spezifischer Benutzereigenschaften ist mithilfe der von der Erweiterung implementierten Methoden möglich. Die-Methoden ermöglichen das Konfigurieren der Eigenschaften, die in der Erweiterungsschnittstelle für Remotedesktopdienste Benutzer verfügbar sind.

Die ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration unterstützt die Prüfung und Bearbeitung von Remotedesktopdienste Benutzereigenschaften, die in der Verzeichnisdienst-Datenbank gespeichert sind. Die Erweiterung unterstützt auch die Konfiguration von Benutzereigenschaften, die in der Active Directory gespeichert sind, über die LDAP-API (Lightweight Directory Access Protocol).

Der Anbieter implementiert die folgenden Methoden:

-   [**IADs:: Get**](/windows/desktop/api/iads/nf-iads-iads-get). Diese Methode sucht eine bestimmte Eigenschaft oder einen Satz von Eigenschaften für eine Instanz der-Klasse.
-   [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put). Diese Methode konfiguriert eine bestimmte Eigenschaft oder einen Satz von Eigenschaften für eine Instanz der-Klasse.

Eine Liste der spezifischen Remotedesktopdienste Benutzereigenschaften, die Sie konfigurieren können, finden Sie in der [Referenz zur ADSI-Erweiterung für Remotedesktopdienste Benutzerkonfiguration](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) .

Weitere Informationen zum Zugreifen auf und Ändern von Attributen mit ADSI finden Sie unter Zugreifen auf und Bearbeiten von [Daten mit ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).

Weitere Informationen zur Verwendung von ADSI-Benennungs Konventionen und ADsPath-Zeichen folgen finden Sie in den Informationen zu einzelnen [ADSI-Dienstanbietern](/windows/desktop/ADSI/adsi-system-providers) in der Dokumentation zum [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) Platform Software Development Kit (SDK).

 

 