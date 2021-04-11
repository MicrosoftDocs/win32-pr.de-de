---
description: Isolation ist das primäre Ziel einer appcontainer-Ausführungsumgebung.
ms.assetid: 13C579F9-7F9F-4602-9B03-08CD820C3BBA
title: Appcontainer-Isolation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82fec44fd3d6eb9495370c42e52726ceb0f63806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217313"
---
# <a name="appcontainer-isolation"></a>Appcontainer-Isolation

Isolation ist das primäre Ziel einer appcontainer-Ausführungsumgebung. Wenn Sie eine Anwendung von nicht benötigten Ressourcen und anderen Anwendungen isolieren, werden Möglichkeiten für böswillige Manipulationen minimiert. Durch das Gewähren von Zugriff auf der Grundlage der geringsten Rechte wird verhindert, dass Anwendungen und Benutzer über ihre Rechte auf Ressourcen zugreifen. Das Steuern des Zugriffs auf Ressourcen schützt den Prozess, das Gerät und das Netzwerk.

Die meisten Sicherheitsrisiken in Windows beginnen mit der Anwendung. Einige gängige Beispiele hierfür sind eine Anwendung, die aus dem Browser heraus bricht oder ein fehlerhaftes Dokument an Internet Explorer sendet, sowie die Nutzung von Plug-ins, wie z. b. Flash. Immer mehr diese Anwendungen können in einem appcontainer isoliert werden, desto sicherer ist das Gerät und die Ressourcen. Auch wenn die Sicherheits Anfälligkeit in einer APP ausgenutzt wird, kann die APP nicht auf Ressourcen zugreifen, die über die für den appcontainer gewährten Berechtigungen hinausgehen. Böswillige Apps können den restlichen Computer nicht übernehmen.

## <a name="credential-isolation"></a>Isolation von Anmelde Informationen

Verwalten von Identitäten und Anmelde Informationen: der appcontainer verhindert die Verwendung von Benutzer Anmelde Informationen, um Zugriff auf Ressourcen zu erhalten oder sich bei anderen Umgebungen anzumelden. Die AppContainer-Umgebung erstellt einen Bezeichner, der die kombinierten Identitäten des Benutzers und der Anwendung verwendet, damit die Anmeldeinformationen für jeden Benutzer und jede Anwendung eindeutig sind und die Anwendung nicht die Identität des Benutzers annehmen kann.

## <a name="device-isolation"></a>Geräte Isolation

Wenn Sie die Anwendung von Geräte Ressourcen isolieren, z. b. Passive Sensoren (Kamera, Mikrofon, GPS) und Geld Pumpen (3G/4G, Telefonnummer), verhindert die appcontainer-Umgebung, dass die Anwendung das Gerät bösartig ausnutzen kann. Diese Ressourcen werden standardmäßig blockiert und können bei Bedarf Zugriff erhalten. In einigen Fällen sind diese Ressourcen durch "Broker" weiter geschützt. Einige Ressourcen, z. b. Tastatur und Maus, sind immer für appcontainer und residente Anwendung verfügbar.

## <a name="file-isolation"></a>Datei Isolation

Wenn Sie den Datei-und Registrierungs Zugriff steuern, verhindert die appcontainer-Umgebung, dass die Anwendung Dateien nicht ändert. Lese-/Schreibzugriff kann bestimmten permanenten Dateien und Registrierungs Schlüsseln erteilt werden. Der schreibgeschützte Zugriff ist weniger eingeschränkt. Eine Anwendung hat immer Zugriff auf die Speicher Residenten Dateien, die speziell für diesen appcontainer erstellt wurden.

## <a name="network-isolation"></a>Netzwerkisolation

Durch das Isolieren der Anwendung von Netzwerkressourcen, die über die speziell zugeordneten verfügen, verhindert appcontainer, dass die Anwendung Ihre Umgebung ausstellt und die Netzwerkressourcen bösartig ausnutzen. Für den Internet Zugriff, den Intranetzugriff und das fungieren als Server kann ein granularer Zugriff gewährt werden.

## <a name="process-isolation"></a>Prozessisolation

Das Sandboxing der Anwendungs-Kernel Objekte, die appcontainer-Umgebung verhindert, dass die Anwendung andere Anwendungsprozesse beeinflusst oder beeinflusst. Dadurch wird verhindert, dass eine ordnungsgemäß enthaltene Anwendung andere Prozesse im Falle einer Ausnahme beschädigt.

## <a name="window-isolation"></a>Fenster Isolation

Wenn Sie die Anwendung von anderen Fenstern isolieren, verhindert die appcontainer-Umgebung, dass die Anwendung andere Anwendungsschnittstellen beeinträchtigt.

 

 



