---
title: Erstellen eines Dienstanbieters
description: Erstellen eines Dienstanbieters
ms.assetid: 7da27fe2-8a57-4adb-94b2-448b6362dc33
keywords:
- Windows Media Device Manager, Erstellen von Dienstanbietern
- Device Manager, Erstellen von Dienstanbietern
- Windows Media Device Manager, Programmier Handbuch
- Device Manager, Programmier Handbuch
- Programmier Handbuch, Dienstanbieter
- Programmier Handbuch, Windows Media Device Manager
- Programmier Handbuch, Erstellen von Dienstanbietern
- Windows Media Device Manager, Dienstanbieter
- Device Manager, Dienstanbieter
- Dienstanbieter, erstellen
- Erstellen von Dienstanbietern, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8469c3d656d151457ed818ea6b4192a3c79ed061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337226"
---
# <a name="creating-a-service-provider"></a>Erstellen eines Dienstanbieters

Ein Dienstanbieter ist eine Komponente, die als middlemann zwischen einer Anwendung und einem Gerät fungiert. Windows Media Device Manager leitet Anforderungen von der Anwendung an den Dienstanbieter weiter, der dann für die Kommunikation mit dem Gerät oder das Ausführen der angeforderten Aktion zuständig ist. Ein Dienstanbieter kommuniziert in der Regel mit einem Treiber, um die Kommunikation mit dem Gerät zu ermöglichen. Ein Dienstanbieter ist eine COM-Komponente, die die Schnittstellen implementiert, die von Windows Media Device Manager aufgerufen werden. Die Stamm Schnittstelle des Dienstanbieter Objekts ist [**imdserviceprovider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider). Nachdem Sie diese Schnittstelle erhalten haben, können Windows Media Device Manager andere Schnittstellen durch die Implementierung verschiedener Methoden des Dienstanbieters abrufen. Die Schnittstellen, die ein Dienstanbieter implementieren muss, sind in [obligatorische und optionale Schnittstellen](mandatory-and-optional-interfaces.md)aufgeführt. Die Hierarchie der Schnittstellen wird in [Schnittstellen für Dienstanbieter](interfaces-for-service-providers.md)angezeigt.

> [!Note]  
> Sie sollten nicht versuchen, einen MTP-Dienstanbieter zu erstellen; Stattdessen sollten Sie den MTP-Dienstanbieter und die von Microsoft bereitgestellten Treiber verwenden.

 

Bevor Sie versuchen, einen Dienstanbieter zu erstellen, sollten Sie gründlich verstehen, welche Aufrufe eine Anwendung für einen Dienstanbieter durchführt. Weitere Informationen zu den grundlegenden Aufgaben und aufrufen, die eine Anwendung für einen Dienstanbieter durchführt, wenn versucht wird, mit einem Gerät zu kommunizieren, finden Sie unter [Erstellen einer Windows Media Device Manager-Anwendung](creating-a-windows-media-device-manager-application.md) .

In der folgenden Liste sind die wichtigsten Schritte beim Entwickeln eines Dienstanbieters aufgeführt:

1.  Schließen Sie die erforderlichen Header-und Bibliotheksdateien für das Projekt ein (und optional auch die Kompilierung). Die Liste der erforderlichen Dateien finden Sie unter [erforderliche Bibliotheken und Header für einen Dienstanbieter](required-libraries-and-headers-for-a-service-provider.md) .
2.  Implementieren Sie alle anderen erforderlichen oder optionalen Dienstanbieter Schnittstellen (siehe [obligatorische und optionale Schnittstellen](mandatory-and-optional-interfaces.md)). Schnittstellen werden in der Regel in dieser Reihenfolge aufgerufen:
    -   [**Icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
    -   [**Imdserviceprovider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)/2
    -   [**Imdspenum Device**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)
    -   [**Imdspdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)/2
    -   [**Imdspenum Storage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)
    -   [**Imdspstorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)/2/3
3.  Stellen Sie sicher, dass der Dienstanbieter oder das Gerät während der Installation die richtigen Registrierungsschlüssel installiert. Diese Schlüssel geben Geräteparameter an, registrieren den Dienstanbieter als Plug-in und aktivieren Plug & Play Benachrichtigungen für das eintreffen und Entfernen von Geräten. Weitere Informationen finden Sie unter [Geräteparameter](device-parameters.md), [Registrieren des Dienstanbieters](registering-the-service-provider.md)und [Aktivieren von PNP für Geräte](enabling-pnp-for-devices.md).
4.  Authentifizieren Sie den Dienstanbieter bei der Instanziierung der Klasse im Konstruktor. Erstellen Sie hierzu eine [csecurechannelserver](csecurechannelserver-class.md) -Klasse, und legen Sie das Zertifikat fest. Implementieren Sie die [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) -Schnittstelle, und nennen Sie die zuvor instanziierten Methoden der csecurechannelserver-Klasse. Weitere Informationen zum Instanziieren der csecurechannelserver-Klasse und Implementieren der icomponentauthenticate-Methoden finden Sie unter [Authentifizieren des Dienstanbieters](authenticating-the-service-provider.md) .
5.  Windows Media Device Manager fragt Ihren Dienstanbieter nach einer Liste verbundener Geräte durch Aufrufen von [**IMDServiceProvider2:: createdevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) oder [**imdserviceprovider:: enumdevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices)ab, je nachdem, ob der Dienstanbieter Plug & Play Geräte verarbeitet. Der Dienstanbieter muss eine Liste von [**imdspdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice) -Objekten zurückgeben, die verbundene Geräte darstellen. Weitere Informationen finden Sie unter Auflisten von [Geräten](enumerating-devices-service-provider.md) .
6.  Vergewissern Sie sich vor der Behandlung von anrufen, dass ein sicherer Kanal eingerichtet wurde. Nennen Sie [**csecurechannelserver:: fisauthenticated**](/previous-versions/bb231600(v=vs.85)) , bevor Sie Aktionen ausführen. Wenn bei diesem Vorgang ein Fehler auftritt, geben Sie WMDM \_ E \_ notcertified zurück.
7.  Sie benötigen ein von Microsoft ausgestelltes Zertifikat-/Schlüsselpaar, um von DRM geschütztes Material verarbeiten zu können. Weitere Informationen finden Sie [unter behandeln geschützter Inhalte im Dienstanbieter](handling-protected-content-in-the-service-provider.md) .
8.  Damit Ihr Gerät automatisch mit Windows Media Player synchronisiert werden kann, muss es die unter [Aktivieren der Synchronisierung mit Windows Media Player](enabling-synchronization-with-windows-media-player.md)aufgeführten Anforderungen erfüllen.
9.  Damit Ihr Gerät in Windows-Explorer angezeigt werden kann, müssen Sie einige besondere Schritte ausführen, die unter [Anforderungen für tragbare Audioplayer in Windows-Explorer angezeigt](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md)werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 