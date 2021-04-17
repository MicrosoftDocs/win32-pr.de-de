---
title: Übersicht über das biometrische Framework
description: Systemeigene Unterstützung für biometrische Geräte ist in Windows integriert.
ms.assetid: 616ba95a-27a3-4eac-b802-5217954ed04e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f524437ba60f0ad5c1518225f91ff23c789a917
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473716"
---
# <a name="biometric-framework-overview"></a>Übersicht über das biometrische Framework

Jede Person verfügt über eindeutige Merkmale, die zur Identifikation verwendet werden können. In der Regel sind diese Merkmale physisch und enthalten Merkmale wie Fingerabdrücke, Sie können jedoch auch Verhaltensmerkmale wie z. b. Gait und Eingabe von Rhythmus einschließen. Der Begriff Biometrie umfasst beide Bedeutungen. Biometrische Informationen ersetzen immer mehr Kenn Wörter, um Benutzer zu identifizieren und zu überprüfen. Es ist sicherer und häufig für Benutzer und Administrator benutzerfreundlicher.

Sensoren werden zum Erfassen biometrischer Informationen verwendet. Die Informationen werden vom Sensor als biometrisches Beispiel aufgezeichnet. Ein einzelnes Beispiel enthält Daten, die ein einzelnes biometrisches Merkmal für eine einzelne Person darstellen. Zum Erstellen einer biometrischen Vorlage werden mehrere Stichproben durchlaufen, und die Vorlage wird sicher gespeichert. Später wird eine Stichprobe von einem unbekannten Benutzer mit den gespeicherten Vorlagen verglichen, um die Benutzeridentität einzurichten und zu überprüfen. Der Windows-biometrische Dienst, der Teil des Windows-Biometrieframework (WBF) ist, bietet die folgenden Funktionen. Diese Funktionen können mithilfe der API-des Windows-Biometrieframeworks genutzt werden.

-   Erfasst biometrische Merkmale, im eine Vorlage zu erstellen.
-   Speichert und ruft biometrische Vorlagen auf sichere Weise ab.
-   Ordnet jede Vorlage einem eindeutigen Bezeichner zu, z. b. einer GUID oder sid.

Sie können diese API auch zum Erweitern des Frameworks und Erstellen von biometrischen Sensor Adaptern, passenden Modulen und Speicherkomponenten verwenden. Weitere Informationen zum Erstellen von Sensor Adaptern, passenden Engines und Speicherkomponenten finden Sie unter [Erstellen von Adapter-Plug-ins](creating-adapter-plug-ins.md).

## <a name="core-platform-components"></a>Kern Platt Form Komponenten

### <a name="windows-biometric-driver-interface-wbdi"></a>Windows-Biometrietreiberschnittstelle (WBDI)

Wbdi ist eine Programmierschnittstelle, mit der ein biometrischer Treiber das biometrische Gerät über den Windows-biometrischen Dienst (WSB) verfügbar machen kann. Sie können einen wbdi-Treiber implementieren, indem Sie eine beliebige unterstützte Treibertechnologie verwenden, einschließlich der folgenden. Es wird jedoch empfohlen, nach Möglichkeit die Verwendung von "GDF" zu verwenden, um die Treiber Qualität und die Systemstabilität zu verbessern

-   Benutzermodustreiber-Framework (Umschalt)
-   Kernelmodustreiber-Framework (KMDF)
-   Windows-Treibermodell (WDM)

Ein wbdi-biometrischer Treiber muss auch die GUID der wbdi-Treiberschnittstelle und alle obligatorischen e/a-Steuerelemente (IOCTLs) unterstützen. Treiber Entwickler sollten die Dokumentation und den Beispielcode im Windows-Treiberkit (WDK) überprüfen.

### <a name="windows-biometric-service-wbs"></a>Windows-biometrischer Dienst (WSB)

Der Windows-biometrische Dienst verwaltet installierte biometrische Treiber und unterstützt die Windows-Biometrieframework-API, um Gerätezugriff auf Client Anwendungen bereitzustellen. WSB führt die folgenden Funktionen aus:

-   Sie schützt die Vertraulichkeit von Benutzern durch die Trennung von Client Anwendungen von biometrischen Daten.
-   Sie schützt biometrische Daten vor nicht privilegierten Client Anwendungen, indem es erfordert, dass Anwendungen mithilfe eindeutiger Bezeichner Zugriff auf Daten erhalten.
-   Er verwendet eine Softwarekomponente, die als [biometrische Einheit](/previous-versions//dd401512(v=vs.85)) bezeichnet wird, um die Funktionen eines bestimmten biometrischen Geräts über eine standardisierte Oberfläche verfügbar zu machen.
-   Sie verwaltet biometrische Einheiten, indem Sie Sie in System-, private oder nicht zugewiesene [Sensor Pools](sensor-pools.md)gruppieren.
-   Sie unterstützt die Verwendung von biometrischen Einheiten [Adaptern](/previous-versions//dd401508(v=vs.85)) für physische Geräte, die nicht in die Verarbeitungs-oder Speicherfunktionen integrieren.

### <a name="windows-biometric-framework-api"></a>Windows-Biometrieframework-API

Die Windows-Biometrieframework-API ermöglicht es Ihnen, Client Anwendungen zu erstellen, die mit dem Windows-biometrischen Dienst interagieren können, um die folgenden Aktionen auszuführen:

-   Identifizieren und überprüfen Sie die Benutzer.
-   Suchen Sie biometrische Geräte, und Fragen Sie Ihre Funktionen ab.
-   Verwalten von Sitzungen und Überwachen von Ereignissen.

## <a name="user-experience-components"></a>Benutzeroberflächen Komponenten

### <a name="discovery-points"></a>Ermittlungs Punkte

Endbenutzer können biometrische Geräte auf folgende Weise suchen:

-   Geben Sie die Wörter Biometrie, Fingerabdruck, Gesicht oder andere verwandte Ausdrücke in das Textfeld Suche starten ein, um die Systemsteuerung für biometrische Geräte zu starten. Die Ergebnisliste für biometrische Daten kann Elemente wie die folgenden für ein Windows 10-Abbild enthalten.
    -   Anmeldung per Fingerabdruck einrichten
    -   Einrichten der Gesichts Anmeldung

### <a name="supported-scenarios"></a>Unterstützte Szenarien

Die folgenden Szenarien werden unterstützt:

-   Benutzer können sich bei einem lokalen Computer, einer Arbeitsgruppe oder einer Domäne anmelden, indem Sie einen Fingerabdruckleser oder eine IR-Kamera mit Fokus auf der Vorderseite verwenden.
-   Ein Benutzer mit Administratorrechten kann Anwendungen über die Benutzerkontensteuerung (User Account Control, UAC) mithilfe eines Fingerabdrucks oder einer Oberfläche erhöhen.

## <a name="management-components"></a>Verwaltungs Komponenten

Ein biometrisches System kann mithilfe von Gruppenrichtlinie oder der Verwaltung mobiler Geräte (Mobile Device Management, MDM) verwaltet werden.

### <a name="biometric-system-management"></a>Biometrische System Verwaltung

Sie können biometrische Funktionen mithilfe von Gruppenrichtlinie oder MDM verwalten. Gruppenrichtlinie können weiter verwendet werden, um die folgenden Aktionen auszuführen:

-   Geben Sie den Timeout Zeitraum für die schnelle Benutzerumschaltung an, wenn dies vom ISV implementiert wird.
-   Verhindern der Installation biometrischer Geräte
-   Erzwingen des Entfernens von Treibern für biometrische Geräte.
-   Deaktivieren Sie den biometrischen Dienst.

 

 