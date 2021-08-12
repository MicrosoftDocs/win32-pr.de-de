---
title: Erstellen eines Dienstanbieters
description: Erstellen eines Dienstanbieters
ms.assetid: 7da27fe2-8a57-4adb-94b2-448b6362dc33
keywords:
- Windows Medien Geräte-Manager, Erstellen von Dienstanbietern
- Geräte-Manager, Erstellen von Dienstanbietern
- Windows Media Geräte-Manager, Programmierhandbuch
- Geräte-Manager, Programmierhandbuch
- Programmierhandbuch,Dienstanbieter
- Programmierhandbuch,Windows Media Geräte-Manager
- Programmierhandbuch,Erstellen von Dienstanbietern
- Windows Medien Geräte-Manager, Dienstanbieter
- Geräte-Manager,Dienstanbieter
- Dienstanbieter, erstellen
- Erstellen von Dienstanbietern, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1f5b6abfba6b143e0a8ab7913ed1c1f53bbdeb3104a6a8450e438843349598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585854"
---
# <a name="creating-a-service-provider"></a>Erstellen eines Dienstanbieters

Ein Dienstanbieter ist eine Komponente, die als Middleman zwischen einer Anwendung und einem Gerät dient. Windows Media Geräte-Manager leitet Anforderungen von der Anwendung an den Dienstanbieter weiter, der dann für die Kommunikation mit dem Gerät oder die Durchführung der angeforderten Aktion zuständig ist. Ein Dienstanbieter kommuniziert in der Regel mit einem Treiber, um die Kommunikation mit dem Gerät zu ermöglichen. Ein Dienstanbieter ist eine COM-Komponente, die die schnittstellen implementiert, die von Windows Media Geräte-Manager aufgerufen werden. Die Stammschnittstelle des Dienstanbieterobjekts ist [**IMDServiceProvider.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) Nach dem Abrufen dieser Schnittstelle können Windows Media Geräte-Manager andere Schnittstellen über die Implementierung verschiedener Methoden des Dienstanbieters abrufen. Die Schnittstellen, die ein Dienstanbieter implementieren muss, sind unter [Obligatorische und optionale Schnittstellen](mandatory-and-optional-interfaces.md)aufgeführt. Die Hierarchie der Schnittstellen wird unter [Schnittstellen für Dienstanbieter](interfaces-for-service-providers.md)angezeigt.

> [!Note]  
> Sie sollten nicht versuchen, einen MTP-Dienstanbieter zu erstellen. Stattdessen sollten Sie den MTP-Dienstanbieter und die von Microsoft bereitgestellten Treiber verwenden.

 

Bevor Sie versuchen, einen Dienstanbieter zu erstellen, sollten Sie gründlich verstehen, welche Aufrufe eine Anwendung für einen Dienstanbieter vor sich hat. Lesen [Sie Erstellen einer Windows Media Geräte-Manager-Anwendung,](creating-a-windows-media-device-manager-application.md) um sich einen Überblick über die grundlegenden Aufgaben und Aufrufe zu verschaffen, die eine Anwendung bei einem Dienstanbieter vorstellt, wenn sie versucht, mit einem Gerät zu kommunizieren.

Die folgende Liste zeigt die wichtigsten Schritte bei der Entwicklung eines Dienstanbieters:

1.  Fügen Sie die erforderlichen Header- und Bibliotheksdateien für Ihr Projekt ein (und kompilieren Sie sie optional). Eine Liste der erforderlichen Dateien finden Sie unter [Erforderliche Bibliotheken und Header für einen Dienstanbieter.](required-libraries-and-headers-for-a-service-provider.md)
2.  Implementieren Sie alle anderen erforderlichen oder optionalen Dienstanbieterschnittstellen (siehe [Obligatorische und optionale Schnittstellen).](mandatory-and-optional-interfaces.md) Schnittstellen werden in der Regel in dieser Reihenfolge aufgerufen:
    -   [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
    -   [**IMDServiceProvider-/2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)
    -   [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)
    -   [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)/2
    -   [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)
    -   [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)/2/3
3.  Stellen Sie sicher, dass Ihr Dienstanbieter oder Gerät während der Installation die richtigen Registrierungsschlüssel installiert. Diese Schlüssel geben Geräteparameter an, registrieren den Dienstanbieter als Plug-In und aktivieren Plug & Play Benachrichtigungen für die Geräteankunft und -entfernung. Weitere Informationen finden Sie unter [Geräteparameter](device-parameters.md), [Registrieren des Dienstanbieters](registering-the-service-provider.md)und [Aktivieren von PnP für Geräte.](enabling-pnp-for-devices.md)
4.  Authentifizieren Sie bei der Instanziierung Ihrer Klasse den Dienstanbieter im Konstruktor. Erstellen Sie hierzu eine [CSecureChannelServer-Klasse,](csecurechannelserver-class.md) und legen Sie das Zertifikat fest. Implementieren Sie die [**IComponentAuthenticate-Schnittstelle,**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) und rufen Sie die Methoden der zuvor instanziierten CSecureChannelServer-Klasse auf. Unter [Authentifizieren des Dienstanbieters](authenticating-the-service-provider.md) erfahren Sie, wie Sie die CSecureChannelServer-Klasse instanziieren und die IComponentAuthenticate-Methoden implementieren.
5.  Windows Media Device Manager will query your service provider for a list of connected devices by calling [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) or [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices), depending on whether the service provider handles Plug and Play devices. Der Dienstanbieter muss eine Liste von [**IMDSPDevice-Objekten**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice) zurückgeben, die verbundene Geräte darstellen. Weitere Informationen finden Sie unter [Aufzählen von Geräten.](enumerating-devices-service-provider.md)
6.  Überprüfen Sie vor der Verarbeitung eines Aufrufs, ob ein sicherer Kanal eingerichtet wurde. Rufen Sie [**CSecureChannelServer::fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) auf, bevor Sie Aktionen ausführen. Wenn dieser Aufruf fehlschlägt, geben Sie WMDM \_ E \_ NOTCERTIFIED zurück.
7.  Sie benötigen ein von Microsoft ausgestelltes Zertifikat-/Schlüsselpaar, um DRM-geschütztes Material verarbeiten zu können. Weitere Informationen finden Sie [unter Behandeln von geschützten Inhalten im Dienstanbieter.](handling-protected-content-in-the-service-provider.md)
8.  Damit Ihr Gerät automatisch mit Windows Media Player synchronisiert werden kann, muss es die unter Aktivieren der [Synchronisierung mit Windows Media Player](enabling-synchronization-with-windows-media-player.md)aufgeführten Anforderungen erfüllen.
9.  Damit Ihr Gerät in Windows Explorer angezeigt werden kann, müssen Sie einige spezielle Schritte ausführen, die unter Anforderungen für portable Audioplayer in [Windows Explorer beschrieben sind.](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 