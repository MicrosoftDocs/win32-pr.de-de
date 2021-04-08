---
title: Entwurfs Überlegungen für benutzerdefinierte Geräte
description: In diesem Thema werden Entwurfs Überlegungen beschrieben, mit denen Sie bestimmen können, ob Ihr Gerät einen benutzerdefinierten Treiber benötigt.
ms.assetid: 8AADE304-4841-41E2-968B-DFCB5B954FF1
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: f503ae556009f3b4b9b88d9f895936218f402fc6
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734720"
---
# <a name="design-considerations-for-custom-devices"></a>Entwurfs Überlegungen für benutzerdefinierte Geräte

In diesem Thema werden Entwurfs Überlegungen beschrieben, mit denen Sie bestimmen können, ob Ihr Gerät einen benutzerdefinierten Treiber benötigt.

- [Bestimmen der Art des zu implementierenden Treibers](#determining-the-type-of-driver-to-implement)
- [Überlegungen zur Sicherheit](#security-considerations)
- [Zugehörige Themen](#related-topics)

## <a name="determining-the-type-of-driver-to-implement"></a>Bestimmen der Art des zu implementierenden Treibers

In dieser Tabelle wird beschrieben, wann Sie einen benutzerdefinierten Treiber für Ihr Gerät entwickeln und mit ihm kommunizieren, indem Sie die Geräte Zugriffs-API verwenden. Sie sollten stattdessen von Windows bereitgestellte Geräte Stapel verwenden.

| Zur Unterstützung von | Implementierung |
|:---|:---|
| Bekannte Geräte, einschließlich: <ul><li>Sensor</li><li>Standort</li><li>Webcam</li><li>Nähe</li><li>SMS (Short Message Service)</li><li>Mobiles Breitband</li></ul><br/> | Für viele Arten von bekannten Geräten benötigen Sie keinen benutzerdefinierten Treiber, da Windows APIs und Klassen Erweiterungs-Gerätetreiber Schnittstellen (DDIs) umfasst, die die Kommunikation zwischen dem Treiber und Windows verwalten. Die Geräte "Sensor", "Location" und "Windows Portable Device" (WPD) sind einige Beispiele für Geräteklassen, die über diese Unterstützung verfügen. Wenn Sie einen Treiber erstellen, der einen dieser von Windows bereitgestellten DDIs verwendet, um Daten und Befehle zu senden und zu empfangen, ist es nicht erforderlich, dass Ihre Windows Store-App die Geräte Zugriffs-API verwendet, um den Zugriff zu übertragen oder Eingabe-/ausgabesteuerungscodes direkt an den Treiber zu senden. <br/> Wenn eine Windows Store-App den Zugriff auf ein bekanntes Gerät mithilfe der Windows-Runtime-API für die Geräteklasse anfordert, übernimmt Windows 8 den Gerätezugriff basierend auf dem Gerätetyp. Apps erhalten stets Zugriff auf einige bekannte Gerätetypen (z. b. Beschleunigungsmesser), von denen keine personenbezogenen Informationen offengelegt werden. Andere Typen bekannter Geräte müssen im Anwendungs Manifest deklariert werden, bevor eine App darauf zugreifen kann. Der Benutzer muss eine Berechtigung für eine APP erteilen, um auf Geräte zuzugreifen, die vertrauliche Informationen wie den Speicherort, die Webcam und Mikrofon Geräte offenlegen, oder die Benutzer Geld Kosten, wie z. b. mobile Breitbandgeräte. <br/> |
| Ein WPD-Gerät, das MTP-Dienste implementiert.<br/> | Sie können den MTP-Klassen Treiber verwenden, oder Sie können einen Treiber mithilfe des WPD-DDI erstellen.<br/> Windows 8 bietet Unterstützung für MTP-Geräte Dienste. Und eine APP kann die [Windows. Devices. Portable](/uwp/api/Windows.Devices.Portable) Windows-Runtime-API, die API für portable Geräte Component Object Model (com) oder die WPD-Automatisierung verwenden, um auf das Gerät zuzugreifen. Ihre APP muss die Geräte Zugriffs-API nicht verwenden.<br/> |
| Ein Gerät, das über keine von Windows bereitgestellte Klassen Erweiterung oder einen Klassen Treiber verfügt.<br/>  | Überprüfen Sie in diesem Fall die [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) für spezialisierte Geräte, um zu bestimmen, ob Sie den benutzerdefinierten Treiber Zugriff mithilfe der Geräte Zugriffs-API implementieren müssen.<br/> |

## <a name="security-considerations"></a>Sicherheitshinweise

Die folgenden Artikel bieten Anleitungen zum Schreiben von sicherem C++-Code:

- [Bewährte Sicherheitsmethoden für C++](/cpp/security/security-best-practices-for-cpp)
- [Patterns & Practices Security Guidance for Applications]/Previous-Versions/MSP-n-p/ff650760 (v = pandp. 10))

## <a name="related-topics"></a>Zugehörige Themen

[Beispiel für benutzerdefinierten Treiber Zugriff](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware dev Center](/windows-hardware/drivers/)
