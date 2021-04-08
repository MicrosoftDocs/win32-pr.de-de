---
title: Zertifizierung Ihrer Desktop Anwendung
description: Führen Sie die folgenden Schritte aus, um Ihre Desktop-App für Windows 7, Windows 8, Windows 8.1 und Windows 10 zu zertifizieren. Wenn Sie Ihre Desktop-App so konvertieren möchten, dass Sie mit der universelle Windows-Plattform und dem Windows Store kompatibel ist, verwenden Sie die Windows-Desktop Bridge. in diesem Fall sollten Sie die Desktop Bridge Anleitung für die Zertifizierungs Schritte befolgen. Wenn Sie eine UWP-APP von Anfang an entwickeln und zertifizieren, finden Sie unter Leitfaden zur Zertifizierung von Windows-apps in UWP Weitere Informationen zur Zertifizierung.
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734560"
---
# <a name="certify-your-desktop-application"></a>Zertifizierung Ihrer Desktop Anwendung

> [!IMPORTANT]
> Die Zertifizierung für Win32-Desktop-Apps ist [veraltet](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920). Senden Sie stattdessen Dateien an dieser [Stelle](https://www.microsoft.com/wdsi/filesubmission/).

Führen Sie die folgenden Schritte aus, um Ihre Desktop-App für Windows 7, Windows 8, Windows 8.1 und Windows 10 zertifizieren zu lassen.

Wenn Sie Ihre Desktop-App so konvertieren möchten, dass Sie mit dem universelle Windows-Plattform und Windows Store kompatibel ist, verwenden Sie die [Windows-Desktop Bridge](https://developer.microsoft.com/windows/bridges/desktop). in diesem Fall sollten Sie die Anleitungen für die [Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root) für die Zertifizierungs Schritte befolgen.

Wenn Sie eine UWP-APP von Anfang an entwickeln und zertifizieren, finden Sie unter [Leitfaden zur Zertifizierung von Windows-apps in UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) Weitere Informationen zur Zertifizierung.

## <a name="step-1-prepare-for-certification"></a>Schritt 1: Vorbereiten der Zertifizierung



| Thema                                                                                       | BESCHREIBUNG                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Was sind die Vorteile?](what-are-the-benefits-.md)<br/>                             | Die Zertifizierung Ihrer Desktop-App bietet Ihnen und ihren Kunden eine Reihe von Vorteilen.              |
| [Lesen der Anforderungen](certification-requirements-for-windows-desktop-apps.md)<br/> | Überprüfen Sie die technischen Anforderungen und Berechtigungs Qualifizierungen, die eine Desktop-App erfüllen muss. |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a>Schritt 2: Testen der APP mit dem zertifizierungskit für Windows-apps



| Thema                                                          | BESCHREIBUNG                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Holen Sie sich das Kit](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | Um die APP zu zertifizieren, müssen Sie das zertifizierungskit für Windows-apps installieren und ausführen (enthalten im Windows SDK).                                                                     |
| [Verwenden des Kits](using-the-windows-app-certification-kit.md)   | Bevor Sie Ihre APP übermitteln können, müssen Sie Sie auf Bereitschaft testen. Sie können auch eine Kopie des [Whitepaper zur Zertifizierung der APP](https://www.microsoft.com/download/details.aspx?id=27414)herunterladen. |
| [Testdetails prüfen](windows-app-certification-kit-tests.md) | Holen Sie sich die Liste der Tests, die Ihre APP durchlaufen muss, um die Kompatibilität mit dem neuesten Windows-Betriebssystem zu qualifizieren.                                                               |



 

Hinweis: Filter Treiber müssen auch das [hardwarezertifizierungskit](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe)bestehen. (Siehe [Zertifizierungsanforderungen für Windows-Desktop-Apps, Abschnitt 6,2](certification-requirements-for-windows-desktop-apps.md).)

## <a name="step-3-use-the-windows-certification-dashboard"></a>Schritt 3: Verwenden des Windows-Zertifizierungs Dashboards

Um Ihre APP zur Zertifizierung zu übermitteln, müssen Sie sich auf dem [Windows-zertifizierungdashboard](/previous-versions/hh833792(v=msdn.10))anmelden oder ein Unternehmens Konto registrieren. Wenn Sie dies tun, können Sie nicht nur Ihre APP zertifizieren, sondern erhalten auch Zugriff auf Tools, mit denen Sie Ihre APP in allen Phasen des Prozesses überprüfen und verwalten können.



| Thema                                                                                                                   | BESCHREIBUNG                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Einrichten Ihres Kontos](/windows-hardware/drivers/dashboard/)                 | Wenn Ihr Unternehmen nicht bereits registriert ist, müssen Sie es über das Windows-zertifizierungsdashboard registrieren.                                        |
| [Abrufen eines Codesignaturzertifikats](/windows-hardware/drivers/dashboard/)      | Bevor Sie ein Windows-zertifizierungdashboard einrichten können, müssen Sie ein Code Signaturzertifikat erhalten, um Ihre digitalen Informationen zu sichern. |
| [Lokales Testen und Hochladen der Ergebnisse](/windows-hardware/drivers/dashboard/) | Laden Sie die Ergebnisse nach dem Ausführen der Tests für Windows-zertifizierungskit auf das Windows-zertifizierungskit hoch                                 |
| [Verwalten Ihrer Übermittlung](/windows-hardware/drivers/dashboard/)              | Nachdem Sie Ihre APP zur Zertifizierung eingereicht haben, können Sie Ihre Übermittlung über das Windows-zertifizierungsdashboard überprüfen.                           |



 

## <a name="step-4-promote-your-desktop-app"></a>Schritt 4: herauf Stufen ihrer Desktop-App



| Thema                                                                      | BESCHREIBUNG                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [APP-Kompatibilität überprüfen](/windows/compatibility/windows-8-1-introduction) | Wenn Sie eine APP für Windows 8.1 entwickeln, untersuchen Sie Kompatibilitätsprobleme.                                           |
| [Verwenden Sie das Logo mit Ihrer APP.](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | Zeigen Sie das Logo auf Verpacken und Werbematerialien entsprechend den Richtlinien an. Nur für Windows 7. |



 

## <a name="see-also"></a>Weitere Informationen:

[App-Kompatibilitäts Forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): finden Sie Unterstützung von der Community zur Kompatibilität und Logo Zertifizierung.

[Windows SDK Blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Hier finden Sie Tipps und Neuigkeiten im Zusammenhang mit der APP-Zertifizierung.

[Windows Server-Forum]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): Besuchen Sie das Zertifizierungs Forum, um Antworten zu erhalten.

[Compatibility Cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Hier erhalten Sie Informationen zu Neuerungen oder Änderungen in der neuesten Version von Windows.

 

