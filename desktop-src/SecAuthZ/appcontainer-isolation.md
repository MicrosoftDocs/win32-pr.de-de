---
description: Isolation ist das Hauptziel einer AppContainer-Ausführungsumgebung.
ms.assetid: 13C579F9-7F9F-4602-9B03-08CD820C3BBA
title: AppContainer-Isolation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe42b12698983bc3a90af06be2bb45992013b52e16e6f7de37083d6c92b9422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784706"
---
# <a name="appcontainer-isolation"></a>AppContainer-Isolation

Isolation ist das Hauptziel einer AppContainer-Ausführungsumgebung. Durch die Isolierung einer Anwendung von nicht neded Resources und anderen Anwendungen werden Die Möglichkeiten für böswillige Manipulationen minimiert. Das Gewähren des Zugriffs auf der Grundlage der geringsten Rechte verhindert, dass Anwendungen und Benutzer über ihre Rechte hinaus auf Ressourcen zugreifen. Die Steuerung des Zugriffs auf Ressourcen schützt den Prozess, das Gerät und das Netzwerk.

Die meisten Sicherheitsrisiken in Windows mit der Anwendung beginnen. Einige gängige Beispiele sind das Ausbrechen einer Anwendung aus dem Browser oder das Senden eines fehlerhaften Dokuments an Internet Explorer sowie die Ausnutzung von Plug-Ins wie Flash. Wenn diese Anwendungen in einem AppContainer isoliert werden können, desto sicherer sind das Gerät und die Ressourcen. Auch wenn das Sicherheitsrisiko in einer App ausgenutzt wird, kann die App nicht auf Ressourcen zugreifen, die über die dem AppContainer gewährten Ressourcen hinausgehen. Böswillige Apps können den Rest des Computers nicht übernehmen.

## <a name="credential-isolation"></a>Isolation von Anmeldeinformationen

Durch die Verwaltung von Identität und Anmeldeinformationen verhindert AppContainer die Verwendung von Benutzeranmeldeinformationen, um Zugriff auf Ressourcen zu erhalten oder sich bei anderen Umgebungen anzumelden. Die AppContainer-Umgebung erstellt einen Bezeichner, der die kombinierten Identitäten des Benutzers und der Anwendung verwendet, damit die Anmeldeinformationen für jeden Benutzer und jede Anwendung eindeutig sind und die Anwendung nicht die Identität des Benutzers annehmen kann.

## <a name="device-isolation"></a>Geräteisolation

Durch das Isolieren der Anwendung von Geräteressourcen wie passiven Sensoren (Kamera, Mikrofon, GPS) und Geldpumpen (3G/4G, Telefonwahl) verhindert die AppContainer-Umgebung, dass die Anwendung das Gerät böswillig ausnutzen kann. Diese Ressourcen werden standardmäßig blockiert und können bei Bedarf Zugriff erhalten. In einigen Fällen werden diese Ressourcen weiter durch "Broker" geschützt. Einige Ressourcen, z. B. Tastatur und Maus, sind für appContainer und die residente Anwendung immer verfügbar.

## <a name="file-isolation"></a>Dateiisolation

Durch die Steuerung des Datei- und Registrierungszugriffs verhindert die AppContainer-Umgebung, dass die Anwendung Dateien ändert, die sie nicht ändern sollte. Lese-/Schreibzugriff kann bestimmten persistenten Dateien und Registrierungsschlüsseln gewährt werden. Der schreibgeschützte Zugriff ist weniger eingeschränkt. Eine Anwendung hat immer Zugriff auf die speichersidenten Dateien, die speziell für diesen AppContainer erstellt wurden.

## <a name="network-isolation"></a>Netzwerkisolation

Durch das Isolieren der Anwendung von Netzwerkressourcen, die über die speziell zugeordneten Ressourcen hinausgehen, verhindert AppContainer, dass die Anwendung ihre Umgebung mit "Kapselung" schützt und Netzwerkressourcen böswillig ausnutzt. Differenzierter Zugriff kann für Internetzugriff, Intranetzugriff und als Server gewährt werden.

## <a name="process-isolation"></a>Prozessisolation

Durch die Sandbox der Anwendungskernelobjekte verhindert die AppContainer-Umgebung, dass die Anwendung andere Anwendungsprozesse beeinflusst oder beeinflusst. Dadurch wird verhindert, dass eine ordnungsgemäß enthaltene Anwendung im Falle einer Ausnahme andere Prozesse beschädigt.

## <a name="window-isolation"></a>Fensterisolation

Durch das Isolieren der Anwendung von anderen Fenstern verhindert die AppContainer-Umgebung, dass die Anwendung auswirkungen auf andere Anwendungsschnittstellen hat.

 

 



