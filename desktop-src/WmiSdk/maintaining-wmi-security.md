---
description: Die WMI-Sicherheit konzentriert sich auf den Schutz des Zugriffs auf Namespacedaten. WMI gewährt zunächst Zugriff auf Benutzergruppen, wie in den WMI-Steuerelement- und DCOM-Einstellungen angegeben, und dann bestimmen Anbieter, ob der Benutzer Zugriff auf Namespacedaten haben soll.
ms.assetid: 88a2538a-ae30-4a1a-9d16-f0cd9419b2ed
ms.tgt_platform: multiple
title: Verwalten der WMI-Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79467b3baffd030cae1022f65bc0b8a97242c5e8bbe2f870753a3d3794b8705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118818418"
---
# <a name="maintaining-wmi-security"></a>Verwalten der WMI-Sicherheit

Die WMI-Sicherheit konzentriert sich auf den Schutz des Zugriffs auf Namespacedaten. WMI gewährt zunächst Zugriff auf Benutzergruppen, wie in den [*WMI-Steuerelement-*](gloss-w.md) und DCOM-Einstellungen angegeben, und dann bestimmen Anbieter, ob der Benutzer Zugriff auf Namespacedaten haben soll.

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [Namespacesicherheit](#namespace-security)
-   [Distributed Component Object Model (DCOM) Security Einstellungen.](#distributed-component-object-model-dcom-security-settings)
-   [WMI, Hosts für gemeinsame Dienste und Authentifizierung](#wmi-shared-service-hosts-and-authentication)
-   [Sicherheit für WMI-Clientskripts und -Anwendungen](#security-for-wmi-client-scripts-and-applications)
-   [Zugehörige Themen](#related-topics)

## <a name="namespace-security"></a>Namespacesicherheit

Die Namespacesicherheit hängt von standard Windows [*Benutzersicherheits-IDs (SID)*](gloss-s.md) und der [*Sicherheitsbeschreibung*](gloss-s.md) für den WMI-Namespace ab.

Sie können die Namespacesicherheit festlegen, indem Sie die folgenden Aktionen ausführen:

-   Gewähren oder Verweigern von Zugriffsrechten für Namespaces für Benutzer, die das WMI-Steuerelement verwenden oder wenn der Namespace erstellt wird. Weitere Informationen finden Sie unter [Setting Namespace Security with the WMI Control (Festlegen der Namespacesicherheit mit dem WMI-Steuerelement)](setting-namespace-security-with-the-wmi-control.md) und Setting Namespace Security When the Namespace is Created [(Festlegen der Namespacesicherheit beim Erstellen des Namespace).](setting-namespace-security-when-the-namespace-is-created.md)
-   Verwenden Sie die WMI-Steuerungs-Registerkarte "Sicherheit", um die Sicherheitsüberwachung einzurichten. Die Sicherheitsüberwachung führt zu Ereignisprotokolleinträgen, wenn ein Benutzer fehlschlägt oder eine überwachte Aktion erfolgreich ausgeführt wird, z. B. das Schreiben von Daten in ein WMI-Objekt oder das Lesen des Sicherheitsdeskriptors. Weitere Informationen finden Sie unter [Zugriff auf WMI-Namespaces.](access-to-wmi-namespaces.md)
-   Verwenden Sie die MOF-Datei, die den Namespace definiert, damit ein Benutzer eine verschlüsselte Verbindung herstellen muss. Weitere Informationen finden Sie unter [Erfordern einer verschlüsselten Verbindung mit einem Namespace.](requiring-an-encrypted-connection-to-a-namespace.md)

## <a name="distributed-component-object-model-dcom-security-settings"></a>Distributed Component Object Model (DCOM) Security Einstellungen.

Die DCOM-Sicherheit erfordert eine Authentifizierungseinstellung und eine Identitätswechseleinstellung. Authentifizierung bedeutet, dass sich ein Prozess gegenüber einem anderen identifiziert. Der Identitätswechsel identifiziert die Autorität, die ein Client einem Server gewährt, um verschiedene Prozesse aufzurufen. Während einer Sicherheitsüberprüfung nimmt der Server die Identität des Clients an. Weitere Informationen finden Sie unter [Sichern von C++-Clients und -Anbietern](securing-c---clients-and-providers.md) oder [Sichern von Skriptclients.](securing-scripting-clients.md)

Skripts und C/C++/C#-Anwendungen richten entweder eine Authentifizierungs- und Identitätswechselebene ein, wenn sie eine Verbindung mit einem WMI-Namespace herstellen, oder sie verwenden die Standardeinstellungen. Für Verbindungen mit Remotecomputern sind andere Einstellungen als für die WMI-Namespaces auf dem lokalen Computer erforderlich. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md)

## <a name="wmi-shared-service-hosts-and-authentication"></a>WMI, Hosts für gemeinsame Dienste und Authentifizierung

WMI befindet sich auf einem freigegebenen Diensthost mit mehreren anderen Diensten, die unter dem NetworkService-Konto ausgeführt werden. In einem Svchost-Prozess verwendet WMI dieselbe Authentifizierung wie die anderen Prozesse auf dem Host.

Anbieter-DLLs werden in separate Diensthostprozesse von WMI geladen. Die **HostingModel-Eigenschaft** in der [**\_ \_ Win32Provider-Systemklasse,**](--win32provider.md) die einen Anbieter darstellt, gibt das Systemkonto an, unter dem der Anbieter ausgeführt wird. Das Festlegen dieser Eigenschaft bewirkt, dass der Anbieter in einen freigegebenen Hostprozess geladen wird, der über eine angegebene Berechtigungsebene verfügt. Weitere Informationen finden Sie unter [Anbieterhosting und Sicherheit.](provider-hosting-and-security.md)

## <a name="security-for-wmi-client-scripts-and-applications"></a>Sicherheit für WMI-Clientskripts und -Anwendungen

Skripts und Anwendungen müssen die richtige Sicherheit einrichten, um eine Verbindung mit WMI-Namespaces auf lokalen und Remotecomputern herzustellen. Weitere Informationen finden Sie unter [Sichern von C++-Clients und -Anbietern,](securing-c---clients-and-providers.md) [Sichern von Skriptclients](securing-scripting-clients.md)und [Sichern von WMI-Ereignissen.](securing-wmi-events.md)

In der folgenden Tabelle sind die Themen zur Aufrechterhaltung der WMI-Sicherheit aufgeführt.



| Thema                                                                                              | Beschreibung                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sichern von WMI-Namespaces](securing-wmi-namespaces.md)                                             | Sie können den Zugriff auf Namespacedaten auf autorisierte Benutzer über die WMI-Steuerung beschränken.                                                                                      |
| [Schützen Ihres Anbieters](securing-your-provider.md)                                               | Informationen zum Schreiben sicherer Anbieter.                                                                                                                           |
| [Sichern von C++-Clients und -Anbietern](securing-c---clients-and-providers.md)                       | Sowohl C++-Anbieter als auch Clientanwendungen müssen viele der gleichen Vorgänge ausführen, um die WMI-Sicherheit aufrechtzuerhalten.                                                         |
| [Sichern von Skriptclients](securing-scripting-clients.md)                                       | Skripts und Visual Basic Anwendungen (Automatisierungsclients) müssen die entsprechende Sicherheit festlegen, um Zugriff auf WMI-Daten und -Ereignisse zu erhalten.                                        |
| [Sichern von WMI-Ereignissen](securing-wmi-events.md)                                                     | WMI-Ereignisse werden vom Ereignisanbieter an einen temporären oder permanenten Consumer übermittelt. Ereignisse werden in Form einer Instanz einer Ereignisklasse übermittelt.               |
| [Ändern der Zugriffssicherheit für sicherungsfähige Objekte](changing-access-security-on-securable-objects.md) | Mit entsprechenden Berechtigungen können Sie Methoden für die WMI-Objekte aufrufen, die sicherungsfähige Objekte darstellen, die Sicherheitsbeschreibungen für sicherungsfähige Objekte lesen oder ändern. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> </dl>

 

 



