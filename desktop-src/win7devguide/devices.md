---
title: Geräte (Entwicklerhandbuch zu Windows 7)
description: Geräte sind ein grundlegender Bestandteil des PC-Erlebnisses, und Windows 7 ermöglicht Entwicklern von Anwendungen, die mit Geräten interagieren, neue Möglichkeiten.
ms.assetid: faed8ec8-2f12-4090-a003-b14b3d26e02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cbfa699d129fd6d8343a0645fc6ed22aa9618ee
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391451"
---
# <a name="devices-windows-7-developer-guide"></a>Geräte (Entwicklerhandbuch zu Windows 7)

Geräte sind ein grundlegender Bestandteil des PC-Erlebnisses, und Windows 7 ermöglicht Entwicklern von Anwendungen, die mit Geräten interagieren, neue Möglichkeiten. Die Plattform für die Geräte Darstellung ermöglicht die Zuordnung von Anwendungen und Diensten zu einem bestimmten Gerät, sodass Benutzer den maximalen Vorteil von ihren Peripheriegeräten sofort nach der Verbindung erhalten können. Die Sensorplattform bietet eine Reihe von APIs für die Ermittlung von und die Kommunikation mit Sensorgeräten, die eine neue Generation von Anwendungen ermöglichen, die ihre Umgebungen kennen. Die Location-Plattform bietet neue APIs für die Verwendung von Standortdaten von einem GPS-Empfänger (Global Positionierungs Systems) oder von anderen Diensten, die Standort spezifisches Anwendungsverhalten für mobile Benutzer ermöglichen. (Weitere Informationen finden Sie unter [Geräte Grundlagen: Übersicht](https://www.microsoft.com/whdc/device/default.mspx).)

## <a name="device-experience-platform"></a>Plattform für Gerätefunktionen

Windows 7 kombiniert Software und Dienste, um interessante neue Erfahrungen für Mobiltelefone, tragbare Medien Player, Kameras und Drucker zu schaffen. Windows 7 erleichtert die Verwendung dieser Geräte direkt vom Windows-Desktop aus. Außerdem bietet es Geräteherstellern eine deutliche Platzierung auf dem Windows-Desktop mit Brandingmöglichkeiten und einer einfachen Oberfläche für die Darstellung der Funktionen und Dienste, die das Gerät unterstützt.

Über die Plattform für die Geräte Darstellung wird jede Windows-Sitzung zu einem Portal, in dem Kunden von ihren Geräten mehr nutzen können. Die Plattform für die Geräte Darstellung ermöglicht Benutzern das Herstellen einer Verbindung mit dem Gerätehersteller, das ermitteln und verwenden verwandter Dienste und das Erlernen von Zubehör. Da das Gerät mit den Microsoft-Webdiensten verbunden ist, können Geräte Unternehmen die Benutzeroberflächen auch dann aktualisieren, wenn Geräte an Consumer ausgeliefert wurden. Die Plattform für die Geräte Darstellung kann eine Anwendungs ähnliche Darstellung für Windows-*Logo* -Geräte, z. b. Mobiltelefone, generieren.

Die Plattform für die Geräte Darstellung ermöglicht Anwendungen den Zugriff auf Geräte wie Mobiltelefone und Medien Player, die Dienste über das *Media Transfer Protocol (MTP)* oder das Treibermodell für [tragbare Windows-Geräte](https://www.bing.com/search?q=Windows+Portable+Devices) implementieren.

Um die Synchronisierung persönlicher Informationen zwischen einem PC und einem Gerät zu ermöglichen, hostet die Plattform für die Geräteoberfläche eine neue Synchronisierungs Plattform für verbundene Geräte und bietet eine Benutzeroberfläche für die Auswahl von Zielanwendungen für die Datensynchronisierung, z. b. **Kontakte**, **Kalender** und **Aufgaben**. (Siehe [Windows-Geräte](https://www.microsoft.com/whdc/device/DeviceExperience/default.mspx)Darstellung.)

## <a name="windows-biometric-framework"></a>Windows-Biometrieframework

Der Windows-Biometrieframework (WBF) bietet eine API, mit der Anwendungen Fingerabdruck Geräte verwenden können, um Benutzer Identitäten zu registrieren, zu identifizieren und zu überprüfen, ohne direkten Zugriff auf biometrische Fingerabdruck Hardware oder-Beispiele zu erhalten. Sie können WBF mit Fingerabdruck Geräten verwenden, die über Windows-wbdi-Treiber (biometrische Geräteschnittstelle) verfügen. WBF ist durch Plug-in-Adapter erweiterbar, die die Sensor Kommunikation, den biometrischen Abgleich und den Vorlagen Speicher verwalten. Dadurch wird sichergestellt, dass WBF mit einer breiten Palette von Fingerabdrucksensoren verwendet werden kann. In Windows 7 können Fingerabdruckleser bei der *UAC* -und Windows-Anmeldung WBF für die Authentifizierung verwenden. (Weitere Informationen finden Sie unter [Windows-Biometrieframework API](../secbiomet/biometric-service-api-portal.md).)

 

 
