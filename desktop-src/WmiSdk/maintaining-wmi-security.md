---
description: WMI-Sicherheit konzentriert sich auf den Schutz des Zugriffs auf Namespace Daten. WMI gewährt zunächst den Benutzern, die durch das WMI-Steuerelement und DCOM-Einstellungen angegeben werden, Zugriff auf Gruppen von Benutzern, und dann ermitteln die Anbieter, ob der Benutzer Zugriff auf Namespace Daten haben sollte.
ms.assetid: 88a2538a-ae30-4a1a-9d16-f0cd9419b2ed
ms.tgt_platform: multiple
title: Verwalten der WMI-Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25cbf4a29567b263d6bd279aac9e2e6e21c523e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352417"
---
# <a name="maintaining-wmi-security"></a>Verwalten der WMI-Sicherheit

WMI-Sicherheit konzentriert sich auf den Schutz des Zugriffs auf Namespace Daten. WMI gewährt zunächst den Benutzern, die durch das [*WMI-Steuer*](gloss-w.md) Element und DCOM-Einstellungen angegeben werden, Zugriff auf Gruppen von Benutzern, und dann ermitteln die Anbieter, ob der Benutzer Zugriff auf Namespace Daten haben sollte.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Namespace Sicherheit](#namespace-security)
-   [DCOM-Sicherheitseinstellungen (verteiltes Component Object Model).](#distributed-component-object-model-dcom-security-settings)
-   [WMI, gemeinsame Dienst Hosts und Authentifizierung](#wmi-shared-service-hosts-and-authentication)
-   [Sicherheit für WMI-Client Skripts und-Anwendungen](#security-for-wmi-client-scripts-and-applications)
-   [Zugehörige Themen](#related-topics)

## <a name="namespace-security"></a>Namespace Sicherheit

Die Namespace Sicherheit hängt von den standardmäßigen Windows-Benutzer Sicherheits-IDs [*(SID)*](gloss-s.md) und der [*Sicherheits Beschreibung*](gloss-s.md) für den WMI-Namespace ab.

Sie können die Namespace Sicherheit festlegen, indem Sie die folgenden Aktionen ausführen:

-   Gewähren oder verweigern Sie Zugriffsrechte für Namespaces für Benutzer, die das WMI-Steuerelement verwenden, oder wenn der Namespace erstellt wird. Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md) Element und [Festlegen der Namespace Sicherheit, wenn der Namespace erstellt wird](setting-namespace-security-when-the-namespace-is-created.md).
-   Verwenden Sie die Registerkarte WMI-Steuerungs Sicherheit, um die Sicherheitsüberwachung einzurichten. Die Sicherheitsüberwachung führt zu Ereignisprotokoll Einträgen, wenn ein Benutzer in einer überwachten Aktion fehlschlägt oder erfolgreich ist, wie z. b. das Schreiben von Daten in ein WMI-Objekt oder das Lesen der Sicherheits Beschreibung. Weitere Informationen finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md).
-   Verwenden Sie die MOF-Datei, die den Namespace definiert, damit ein Benutzer eine verschlüsselte Verbindung herstellen muss. Weitere Informationen finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="distributed-component-object-model-dcom-security-settings"></a>DCOM-Sicherheitseinstellungen (verteiltes Component Object Model).

Die DCOM-Sicherheit erfordert eine Authentifizierungs Einstellung und eine Identitätswechsel Einstellung. Die Authentifizierung bedeutet, dass sich ein Prozess bei einem anderen Prozess selbst identifiziert. Identitätswechsel gibt die Autorität an, die ein Client einem Server zuweist, verschiedene Prozesse aufzurufen. Während einer Sicherheitsüberprüfung nimmt der Server die Identität des Clients an. Weitere Informationen finden Sie unter [Sichern von C++-Clients und-Anbietern](securing-c---clients-and-providers.md) oder [Sichern von Skript Clients](securing-scripting-clients.md).

Skripts und C/C++/C #-Anwendungen stellen entweder eine Authentifizierungs-und Identitätswechsel Ebene her, wenn Sie eine Verbindung mit einem WMI-Namespace herstellen oder die Standardeinstellungen verwenden. Für Verbindungen mit Remote Computern sind andere Einstellungen erforderlich als für die WMI-Namespaces auf dem lokalen Computer. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).

## <a name="wmi-shared-service-hosts-and-authentication"></a>WMI, gemeinsame Dienst Hosts und Authentifizierung

WMI befindet sich in einem gemeinsamen Dienst Host mit mehreren anderen Diensten, die unter dem Network Service-Konto ausgeführt werden. In einem Svchost-Prozess hat WMI dieselbe Authentifizierung wie die anderen Prozesse im Host.

Anbieter-DLLs werden von WMI in separate Dienst Host Prozesse geladen. Die **hostingmodel** -Eigenschaft in der [**\_ \_ Win32Provider**](--win32provider.md) -System Klasse, die einen Anbieter darstellt, gibt das Systemkonto an, unter dem der Anbieter ausgeführt wird. Das Festlegen dieser Eigenschaft bewirkt, dass der Anbieter in einen freigegebenen Host Prozess geladen wird, der über eine bestimmte Berechtigungsebene verfügt. Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).

## <a name="security-for-wmi-client-scripts-and-applications"></a>Sicherheit für WMI-Client Skripts und-Anwendungen

Skripts und Anwendungen müssen über die richtige Sicherheit verfügen, um eine Verbindung mit WMI-Namespaces auf lokalen Computern und Remote Computern herzustellen. Weitere Informationen finden Sie unter [Sichern von C++-Clients und-Anbietern](securing-c---clients-and-providers.md), [Sichern von Skript Clients](securing-scripting-clients.md)und [Sichern von WMI-Ereignissen](securing-wmi-events.md).

In der folgenden Tabelle sind die Themen zum Verwalten der WMI-Sicherheit aufgelistet.



| Thema                                                                                              | BESCHREIBUNG                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sichern von WMI-Namespaces](securing-wmi-namespaces.md)                                             | Sie können den Zugriff auf den Namespace-Datenzugriff auf autorisierte Benutzer über das WMI-Steuerelement einschränken.                                                                                      |
| [Sichern Ihres Anbieters](securing-your-provider.md)                                               | Informationen zum Schreiben von sicheren Anbietern.                                                                                                                           |
| [Sichern von C++-Clients und-Anbietern](securing-c---clients-and-providers.md)                       | Sowohl C++-Anbieter als auch Client Anwendungen müssen viele der gleichen Vorgänge ausführen, um die WMI-Sicherheit aufrechtzuerhalten.                                                         |
| [Sichern von Skript Clients](securing-scripting-clients.md)                                       | Skripts und Visual Basic Anwendungen (Automatisierungs Clients) müssen die entsprechende Sicherheit festlegen, um Zugriff auf WMI-Daten und-Ereignisse zu erhalten.                                        |
| [Sichern von WMI-Ereignissen](securing-wmi-events.md)                                                     | WMI-Ereignisse werden vom Ereignis Anbieter an einen temporären oder permanenten Consumer übermittelt. Ereignisse werden in Form einer Instanz einer Ereignisklasse übermittelt.               |
| [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md) | Mit den entsprechenden Berechtigungen können Sie Methoden für die WMI-Objekte abrufen, die Sicherungs fähige Objekte darstellen, die Sicherheits Deskriptoren für Sicherungs fähige Objekte lesen oder ändern. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> </dl>

 

 



