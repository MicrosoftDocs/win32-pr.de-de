---
title: Übersicht über das biometrische Framework
description: Native Unterstützung für biometrische Geräte ist in die Windows.
ms.assetid: 616ba95a-27a3-4eac-b802-5217954ed04e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72b7bb6eab6a062b4dae51f729641607bcadc05dc7b0c50d12f6d59d729ae9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622700"
---
# <a name="biometric-framework-overview"></a>Übersicht über das biometrische Framework

Jede Person verfügt über eindeutige Merkmale, die für die Identifizierung verwendet werden können. In der Regel sind diese Merkmale physisch und umfassen Merkmale wie Fingerabdrücke, aber sie können auch Verhaltensmerkmale wie z. B. Heiterkeit und Typisierungsrhythmus enthalten. Der Begriff Biometrie umfasst beide Bedeutungen. Biometrische Informationen ersetzen zunehmend Kennwörter, um Benutzer zu identifizieren und zu überprüfen. Sie ist sicherer und häufig benutzer- und administratorfreundlicher.

Sensoren werden verwendet, um biometrische Informationen zu erfassen. Die Informationen werden vom Sensor als biometrische Stichprobe erfasst. Ein einzelnes Beispiel enthält Daten, die ein einzelnes biometrisches Merkmal für eine Person darstellt. Mehrere Stichproben werden gemittelt, um eine biometrische Vorlage zu erstellen, und die Vorlage wird sicher gespeichert. Später wird ein Beispiel eines unbekannten Benutzers mit den gespeicherten Vorlagen verglichen, um die Benutzeridentität zu erstellen und zu überprüfen. Der Windows Biometriedienst, der Teil des Windows Biometric Framework (WBF) ist, bietet die folgenden Funktionen. Diese Funktionen können mithilfe der API-des Windows-Biometrieframeworks genutzt werden.

-   Erfasst biometrische Merkmale, im eine Vorlage zu erstellen.
-   Sicheres Speichern und Abrufen biometrischer Vorlagen.
-   Karten jede Vorlage in einen eindeutigen Bezeichner, z. B. eine GUID oder SID.

Sie können diese API auch verwenden, um das Framework zu erweitern und biometrische Sensoradapter, passende Engines und Speicherkomponenten zu erstellen. Weitere Informationen zum Erstellen von Sensoradaptern, übereinstimmenden Engines und Speicherkomponenten finden Sie unter [Erstellen von Adapter-Plug-Ins.](creating-adapter-plug-ins.md)

## <a name="core-platform-components"></a>Kernplattformkomponenten

### <a name="windows-biometric-driver-interface-wbdi"></a>Windows-Biometrietreiberschnittstelle (WBDI)

WBDI ist eine Programmierschnittstelle, die ein biometrischer Treiber verwenden kann, um das biometrische Gerät über den Windows Biometric Service (WBS) verfügbar zu machen. Sie können einen WBDI-Treiber implementieren, indem Sie jede unterstützte Treibertechnologie verwenden, einschließlich der folgenden. Es wird jedoch empfohlen, UMDF nach Möglichkeit zu verwenden, um die Qualität des Treibers und die Systemstabilität zu verbessern.

-   User Mode Driver Framework (UMDF)
-   Kernelmodus-Treiberframework (KMDF)
-   Windows Treibermodell (WDM)

Ein biometrischer WBDI-Treiber muss auch die Schnittstellen-GUID des WBDI-Treibers und alle obligatorischen E/A-Steuerelemente (IOCTLs) unterstützen. Treiberentwickler sollten die Dokumentation und den Beispielcode im Windows Driver Kit (WDK) lesen.

### <a name="windows-biometric-service-wbs"></a>Windows Biometrischer Dienst (Biometric Service, WBS)

Der Windows Biometric Service verwaltet installierte biometrische Treiber und unterstützt die Windows Biometric Framework-API, um Gerätezugriff auf Clientanwendungen zu ermöglichen. WBS führt die folgenden Funktionen aus:

-   Sie schützt die Vertraulichkeit der Benutzer, indem Clientanwendungen von biometrischen Daten getrennt werden.
-   Sie schützt biometrische Daten vor nicht privilegierten Clientanwendungen, indem sie erfordert, dass Anwendungen mithilfe eindeutiger Bezeichner Zugriff auf Daten erhalten.
-   Es verwendet eine Softwarekomponente, die als [biometrische Einheit](/previous-versions//dd401512(v=vs.85)) bezeichnet wird, um die Funktionen eines bestimmten biometrischen Geräts über eine standardisierte Schnittstelle verfügbar zu machen.
-   Sie verwaltet biometrische Einheiten, indem sie in System-, private oder nicht zugewiesene [Sensorpools gruppiert werden.](sensor-pools.md)
-   Es unterstützt die Verwendung biometrischer Komponentenadapter für physische Geräte, die keine [Onboardverarbeitungs-](/previous-versions//dd401508(v=vs.85)) oder Speicherfunktionen haben.

### <a name="windows-biometric-framework-api"></a>Windows-Biometrieframework-API

Mit Windows Biometrieframework-API können Sie Clientanwendungen erstellen, die mit dem Windows Biometric Service interagieren können, um die folgenden Aktionen durchzuführen:

-   Identifizieren und Überprüfen von Benutzern.
-   Suchen Sie nach biometrischen Geräten, und fragen Sie ihre Funktionen ab.
-   Verwalten von Sitzungen und Überwachen von Ereignissen.

## <a name="user-experience-components"></a>Benutzeroberflächenkomponenten

### <a name="discovery-points"></a>Ermittlungspunkte

Endbenutzer können biometrische Geräte auf eine der folgenden Arten finden:

-   Geben Sie die Wörter Biometrie, Fingerabdruck, Gesicht oder andere verwandte Ausdrücke in das Textfeld Suche starten ein, um die Systemsteuerung für biometrische Geräte zu starten. Die Ergebnisliste für biometrische Daten kann Elemente wie die folgenden auf einem Windows 10 enthalten.
    -   Einrichten der Anmeldung per Fingerabdruck
    -   Einrichten der Gesichtserkennungs-Anmeldung

### <a name="supported-scenarios"></a>Unterstützte Szenarien

Die folgenden Szenarien werden unterstützt:

-   Benutzer können sich mit einem Fingerabdruckleser oder einer IR-Kamera mit Fokus auf dem Gesicht bei einem lokalen Computer, einer Arbeitsgruppe oder einer Domäne anmelden.
-   Ein Benutzer mit Administratorrechten kann Anwendungen mithilfe der Benutzerkontensteuerung (User Account Control, UAC) mithilfe eines Fingerabdrucks oder Gesichts erhöhen.

## <a name="management-components"></a>Verwaltungskomponenten

Ein biometrisches System kann mithilfe Gruppenrichtlinie verwaltung mobiler Geräte (Mobile Device Management, MDM) verwaltet werden.

### <a name="biometric-system-management"></a>Biometrische Systemverwaltung

Sie können biometrische Funktionen mithilfe von Gruppenrichtlinie MDM verwalten. Gruppenrichtlinie können weiter verwendet werden, um die folgenden Aktionen durchzuführen:

-   Geben Sie den Timeoutzeitraum für einen schnellen Benutzerwechsel an, wenn er vom ISV implementiert wird.
-   Verhindern sie die Installation biometrischer Geräte.
-   Erzwingen Sie das Entfernen von Treibern für biometrische Geräte.
-   Deaktivieren Sie den biometrischen Dienst.

 

 