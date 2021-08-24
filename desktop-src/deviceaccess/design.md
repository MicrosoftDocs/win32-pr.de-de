---
title: Entwurfsüberlegungen für benutzerdefinierte Geräte
description: In diesem Thema werden Entwurfsüberlegungen beschrieben, mit denen Sie bestimmen können, ob Ihr Gerät einen benutzerdefinierten Treiber benötigt.
ms.assetid: 8AADE304-4841-41E2-968B-DFCB5B954FF1
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 5639cf9fd51eeadc2dfb3ba84556ce6c339b6eb699e0cfa364bdee0bb03d3867
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029092"
---
# <a name="design-considerations-for-custom-devices"></a>Entwurfsüberlegungen für benutzerdefinierte Geräte

In diesem Thema werden Entwurfsüberlegungen beschrieben, mit denen Sie bestimmen können, ob Ihr Gerät einen benutzerdefinierten Treiber benötigt.

- [Bestimmen des zu implementierenden Treibertyps](#determining-the-type-of-driver-to-implement)
- [Überlegungen zur Sicherheit](#security-considerations)
- [Zugehörige Themen](#related-topics)

## <a name="determining-the-type-of-driver-to-implement"></a>Bestimmen des zu implementierenden Treibertyps

In dieser Tabelle wird beschrieben, wann Sie einen benutzerdefinierten Treiber für Ihr Gerät entwickeln und mit ihm über die Gerätezugriffs-API kommunizieren sollten und wann Sie stattdessen Windows bereitgestellten Gerätestapel verwenden sollten.

| So unterstützen Sie | Implementierung |
|:---|:---|
| Bekannte Geräte, einschließlich: <ul><li>Sensor</li><li>Standort</li><li>Webcam</li><li>Nähe</li><li>Kurznachrichtendienst (SMS)</li><li>Mobiles Breitband</li></ul><br/> | Für viele Arten bekannter Geräte benötigen Sie keinen benutzerdefinierten Treiber, da Windows APIs und DDIs (Class-Extension Device Driver Interfaces) enthält, die die Kommunikation zwischen treiber und Windows verwalten. Sensor-, Standort- und Windows PORTABLE DEVICE-Geräte (WPD) sind einige Beispiele für Geräteklassen, die diese Unterstützung haben. Wenn Sie einen Treiber erstellen, der eine dieser Windows bereitgestellten DDIs zum Senden und Empfangen von Daten und Befehlen verwendet, ist es nicht erforderlich, dass Ihre Windows Store-App die Gerätezugriffs-API verwendet, um den Zugriff zu vermitteln oder E/A-Steuerungscodes (Input/Output) direkt an den Treiber zu senden. <br/> Wenn eine Windows Store-App den Zugriff auf ein bekanntes Gerät mithilfe der Windows Runtime-API für ihre Geräteklasse anfordert, verarbeitet Windows 8 den Gerätezugriff basierend auf dem Gerätetyp. Apps erhalten immer Zugriff auf einige bekannte Gerätetypen (z. B. Beschleunigungsmesser), die keine personenbezogenen Informationen preisgeben. Andere Bekannte Gerätetypen müssen im Anwendungsmanifest deklariert werden, bevor eine App darauf zugreifen kann. Der Benutzer muss einer App die Berechtigung für den Zugriff auf Geräte erteilen, die vertrauliche Informationen wie Standort-, Webcam- und Mikrofongeräte anzeigen, oder kann dem Benutzer Geld kosten, z. B. mobile Breitbandgeräte. <br/> |
| Ein WPD-Gerät, das MTP-Dienste implementiert.<br/> | Sie können den MTP-Klassentreiber verwenden oder einen Treiber mit der WPD DDI erstellen.<br/> Windows 8 bietet Unterstützung für MTP-Gerätedienste. Und eine App kann die [Windows verwenden. Devices.Portable](/uwp/api/Windows.Devices.Portable) Windows Runtime-API, die COM-API (Portable Device Component Object Model) oder WPD Automation für den Zugriff auf das Gerät. Ihre App muss die Gerätezugriffs-API nicht verwenden.<br/> |
| Ein Gerät, das nicht über eine Windows bereitgestellte Klassenerweiterung oder einen Klassentreiber verfügt.<br/>  | Überprüfen Sie in diesem Fall die [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) für spezialisierte Geräte, um zu bestimmen, ob Sie den benutzerdefinierten Treiberzugriff mithilfe der Gerätezugriffs-API implementieren müssen.<br/> |

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die folgenden Artikel enthalten Anleitungen zum Schreiben von sicherem C++-Code:

- [Bewährte Sicherheitsmethoden für C++](/cpp/security/security-best-practices-for-cpp)
- [Patterns & Practices Security Guidance for Applications]/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Zugehörige Themen

Beispiel für [benutzerdefinierten Treiberzugriff,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Hardware Dev Center](/windows-hardware/drivers/)
