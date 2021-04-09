---
description: Bietet einen Überblick über die Änderungen an den in Windows 8 eingeführten Windows-Steuerelementen.
ms.assetid: 7EB33215-8F8B-4EA4-87E6-A98F0D014548
title: Neuerungen bei der Sicherheit der Windows 8-Familie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2123ec7f0d9c3af66528c6c203a3e8ea64bd0384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864772"
---
# <a name="whats-new-in-windows-8-family-safety"></a>Neuerungen bei der Sicherheit der Windows 8-Familie

## <a name="overview-of-parental-controls-changes-for-windows-8"></a>Übersicht über Änderungen der Jugend Steuerungs Änderungen für Windows 8

Der Zweck dieses Dokuments besteht darin, einen Überblick über die Änderungen an den Windows-Steuerelementen in Windows 8 zu geben und Lösungen für die Lösung von Jugend Steuerungslösungen von Drittanbietern zu ermöglichen, diese Änderungen zu nutzen. In diesem Dokument wird davon ausgegangen, dass die Leser mit Jugendschutz für Windows 7 und Windows Vista vertraut sind und nur Änderungen an dieser Funktionalität in Windows 8 widerspiegeln, die für die Entwicklung von Jugendschutz Lösungen von Drittanbietern relevant sind.

## <a name="key-design-decisions-for-windows-8-parental-controlfamily-safety-changes"></a>Wichtige Entwurfsentscheidungen für Windows 8 Jugendschutz-/familiensicherheitssicherheits-Änderungen

Änderungen an den in Windows 8 eingeführten Jugendschutz Maßnahmen setzen das übergeordnete Ziel der Einführung von Featureverbesserungen fort und fördern gleichzeitig das gleichzeitige entwickeln von Lösungen der Jugend Steuerungslösungen von Drittanbietern mit der in-Box-Funktionalität. Die Änderungen sind:

-   Verwendung der Microsoft-Familien Sicherheit zur Bereitstellung von Remote Verwaltung und Remote Aktivitäts Überwachung.
-   Integration der Webfilterung als Teil der in-Box-Einschränkungen von Microsoft und die Möglichkeit, Aktivitätsberichte auf einem Computer mit Windows 8 anzuzeigen.
-   Das Feature "Jugendschutz" in der Systemsteuerung wurde in die Familien Sicherheit umbenannt und wird in diesem Dokument als solche bezeichnet.
-   Die in-Box-Zeitbeschränkungen wurden durch die Möglichkeit zur Steuerung der Gesamtzeit pro Tag, mit der der Computer verwendet werden kann (Zeitkontingent), zusätzlich zur Steuerung der Zeiten, in denen der Computer verwendet werden kann (nur wenige), verbessert. In früheren Versionen von Windows war nur noch ein paar verfügbar.
-   Die Sicherheitsfunktionen der Windows 8-Familie können während der standardmäßigen Kontoerstellung aktiviert werden.
-   Die Erweiterbarkeits Features von Windows Vista und Windows 7 werden weiterhin von der Windows 8-Familien Sicherheit unterstützt, einschließlich der Fähigkeit von Drittanbieter Lösungen, den Webinhalts Filter zu ersetzen oder die in-Box-Konfigurations Benutzeroberfläche zu ersetzen, während gleichzeitig die in-Box-Implementierung von Zeit, Anwendung, Spiel Einschränkungen und Webinhalts Filter zu finden ist.
-   Die Anbieter Aktivierung von Drittanbietern deaktiviert die Remote Verwaltung und die Berichterstellung von Sicherheitskontrollen der Windows 8-Familie über die Family Safety-Website.
-   Die Erweiterbarkeit von Drittanbietern für die Familien Sicherheit wird nur für Windows 8-Desktop Anwendungen unterstützt.

## <a name="family-safety-and-standard-account-creation-in-windows-8"></a>Familien Sicherheit und Standardkonto Erstellung in Windows 8

Als Teil der Standardkonto Erstellung in Windows 8 hat ein Administrator die Möglichkeit, die Überwachung des Kontos nach Familien Sicherheit zu aktivieren. Im folgenden finden Sie eine Liste der Funktionen und die Fähigkeit des Drittanbieter Anbieters, Sie zu steuern:

-   Auf dem letzten Bildschirm des Flows zum Erstellen des Windows 8-Standard Kontos wird einem Administrator ein Kontrollkästchen angezeigt, um die Familien Sicherheit für das neu erstellte Konto zu aktivieren.
-   Wenn dieses Kontrollkästchen aktiviert ist, wird die Familien Sicherheit für das Konto mit den folgenden Einstellungen aktiviert:
    -   Aktivitäts Berichterstellung für
    -   Alle Einschränkungen sind deaktiviert.
-   Wenn der Administrator eine Microsoft-Konto für die Anmeldung bei Windows verwendet hat, wird der Windows 8-Computer für die Remote Verwaltung von Familien Sicherheitseinstellungen und e-Mail-Aktivitäts Berichten konfiguriert. Die Family Safety-Website kann dann für die Remote Verwaltung eines solchen Computers verwendet werden.
-   Wenn der Drittanbieter für das Kontrollkästchen in einem Standardkonto Erstellungs Fluss vorhanden sein möchte, sollte der folgende Wert unter den Registrierungs Werten des Anbieters vorhanden sein. Weitere Informationen zu den Details der Anbieter Registrierung finden Sie im Abschnitt " [Anbieter Registrierung](what-s-new-in-windows-7-parental-controls.md) " im Thema Neuigkeiten in Windows 7-Jugend Steuerungs Themen.

    

    | Begriff                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                  |
    |------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span id="AddUserVisible"></span><span id="adduservisible"></span><span id="ADDUSERVISIBLE"></span>Adduservisible<br/> | Ein optionaler **DWORD** -Wert ungleich 0 (null), der angibt, dass die Kontrollkästchen-Option zum Aktivieren der Überwachung der Familien Sicherheit für ein neu erstelltes Konto während der Standardkonto Erstellung in Windows 8 sichtbar sein soll, nachdem der Anbieter als aktueller Familien Sicherheitsanbieter ausgewählt wurde.<br/> |

    

     

-   Da Drittanbieter so konzipiert sind, dass Sie die standardmäßige Konfigurations Benutzeroberfläche für die Steuerelemente der Familien Sicherheit ersetzen, führt die Installation und Aktivierung eines Drittanbieter-Anbieters standardmäßig dazu, dass die Option zum Aktivieren der Familien Sicherheit während der Standardkonto Erstellung nicht angezeigt wird.

## <a name="family-safety-top-level-user-interface-changes-in-windows-8"></a>Änderungen an der Benutzeroberfläche der Familien Sicherheit auf oberster Ebene in Windows 8

Windows 8 führt die folgenden Änderungen an der Systemsteuerung auf der obersten Ebene der Jugend Steuerungsebene aus:

-   Wenn für mindestens ein Standardkonto auf einem Windows 8-Computer die in-Box-Steuerelemente für die Familien Sicherheit aktiviert sind, wird der Befehls Link Einstellungen auf der Family Safety-Website verwalten angezeigt, mit dem ein Administrator die Remote Verwaltung der Sicherheitseinstellungen der Windows 8-Computerfamilie über die Family Safety-Website einrichten kann.
-   Wenn ein Windows 8-Computer für die Remote Verwaltung über die Family Safety-Website konfiguriert ist, kann ein Administrator die Remote Verwaltung eines Windows 8-Computers über die Family Safety-Website deaktivieren.
-   Der Abschnitt Steuerelemente ist nur sichtbar, wenn mindestens ein Drittanbieter bei der Familien Sicherheit registriert ist. Die Benutzeroberfläche und die Funktionalität dieses Abschnitts sind identisch mit dem Abschnitt zusätzliche Steuerelemente in Windows 7-Jugend Steuerungs Steuerelementen. Weitere Informationen finden Sie im Abschnitt übergeordneten Steuerelemente der obersten Ebene der Benutzeroberfläche des Themas [Windows 7 Jugend Steuerungs](what-s-new-in-windows-7-parental-controls.md) Themen.
-   Wenn ein Drittanbieter installiert und als aktueller Anbieter ausgewählt wird, wird die Remote Verwaltung der Sicherheitseinstellungen für die Windows 8-Computerfamilie über die Family Safety-Website deaktiviert.

## <a name="family-safety-in-box-restrictions-changes-in-windows-8"></a>Änderungen der Familien Sicherheit In-Box Einschränkungen in Windows 8

Windows 8 bringt die folgenden Änderungen an den in-Box-Einschränkungen der Familien Sicherheit:

Webeinschränkungen

-   Die Implementierung hat sich von einem LSP-Filter (geschichteter Dienstanbieter) zu einem Windows-Filter Plattform-Treiber (WFP) geändert, der mit dem in den Benutzersitzungen ausgeführt wird.

Zeit Limits

-   Die in-Box-Zeitbeschränkungen wurden durch die Möglichkeit zur Steuerung der Gesamtzeit pro Tag, mit der der Computer verwendet werden kann (Zeitkontingent), zusätzlich zur Steuerung der Zeiten, in denen der Computer verwendet werden kann (in früheren Versionen von Windows), verbessert.
-   Die Benutzeroberfläche für geschweiente Elemente ermöglicht die unabhängige Steuerung der einzelnen Wochentage mit einer halben Stunden Granularität.
-   Die Benutzeroberfläche für das Zeitlimit ermöglicht die Steuerung für Wochentage/Wochenenden oder das unabhängige Steuerelement für jeden Tag der Woche mit einer Granularität von 15 Minuten.
-   Der-Mechanismus für schnelle Benutzer Switches wird nicht mehr verwendet, um die Anmeldung des kontrollierten Benutzers zu erzwingen oder zu blockieren, wenn der blockierte Zeitraum blockiert ist. Für diese Zwecke wird ein Wechsel zu einem separaten Desktop verwendet.
-   Warn Ereignisse für die Trennung sind nicht mehr für die zu abonnierenden Anwendungen verfügbar.

## <a name="family-safety-api-changes-in-windows-8"></a>Änderungen der Family Safety-API in Windows 8

APIs, die für die Familien Sicherheit verwendet werden, machen die Richtlinien-und EinstellungenEinstellungen sowie die Protokollierungs Funktionalität verfügbar

Protokollierung

-   Benutzerdefinierte Ereignisse werden im Bericht-Viewer der Family Safety-Aktivität nicht mehr unterstützt.

WMI-API-Einstellungen schreiben/lesen

-   Wpcusersettings: zuvor wurden Zeit Geber Einschränkungen 1-Stunden-Granularität unterstützt. In Windows 8 stellt die vorhandene Eigenschaft die erste halbe Stunde für jede Stunde dar. Es wurde eine neue halbstündige Eigenschaft hinzugefügt, die die zweite Hälfte der einzelnen Stunden darstellt. Es wurde eine zusätzliche neue Eigenschaft eingeführt, die die tägliche Zeit Gewährung darstellt.

Exportieren/Importieren eines Formats für Webinhalts Filter zulassen/Blockieren von Listen

-   Die Export Funktion zum Zulassen/Blockieren von Webinhalts Filtern wird nicht mehr unterstützt.

WMI-Anbieter Schema für Familien Einstellungen

-   Die folgenden Ergänzungen wurden an der wpcusersettings-Klasse vorgenommen, um Zeit Einschränkungs Erweiterungen widerzuspiegeln:
    -   `[write: ToInstance ToSubClass, Description("Logon Half-Hours (30 minute offset) mask for this user"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 LogonHalfHours[7];`
    -   `[write: ToInstance ToSubClass, Description("Daily minute allowance"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 AllowanceMinutes[7];`

> [!Note]  
> Windows 8 verwendet einen neuen Registrierungsschlüssel, um anzugeben, dass die familiensicherheits-API für einen bestimmten Benutzer aktiviert ist.
>
> **HKLM** \\ **Microsoft** \\ **Software** \\ **Windows** \\ **CurrentVersion** \\ **Eltern Steuerelemente** \\ **Benutzer** \\ **{UserSID}** \\ **Web** \\ **Filtern nach**

 

Der folgende Registrierungsschlüssel wird nur für Windows 7 unterstützt.

**HKLM** \\ **Microsoft** \\ **Software** \\ **Windows** \\ **CurrentVersion** \\ **Eltern Steuerelemente** \\ **Benutzer** \\ **{UserSID}** \\ **Elterliche Steuerelemente**

Bei beiden Schlüsseln weist der Wert "0x00" (**DWORD**) darauf hin, dass die Funktion für den aktuellen Benutzer deaktiviert ist, und der Wert "0x01" (**DWORD**) gibt an, dass die Funktion für den aktuellen Benutzer aktiviert ist. Wenn Sie versuchen, die Werte dieser Schlüssel zu lesen, ersetzen Sie das Token "{UserSID}" durch die System-ID des Benutzers.

 

 




